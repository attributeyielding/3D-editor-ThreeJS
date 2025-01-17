# Advanced Three.js Sculpting Editor

This project is a basic 3D sculpting editor built using Three.js. It allows users to manipulate a 3D sphere mesh using various sculpting tools, adjust brush settings, apply symmetry, and import/export models in OBJ and STL formats.

---

## **Key Features**

1. **3D Scene Setup**:
   - A `THREE.Scene` with a default sphere mesh.
   - A `THREE.PerspectiveCamera` and `THREE.WebGLRenderer` for rendering.
   - `OrbitControls` for camera manipulation (rotate, zoom, pan).

2. **Sculpting Tools**:
   - **Brush Types**: "Push/Pull" and "Inflate/Deflate".
   - **Brush Size and Strength**: Adjustable via sliders.
   - **Symmetry**: Vertical and horizontal symmetry for mirrored sculpting.

3. **Smoothing**:
   - A "Smooth" button applies a basic smoothing algorithm to the mesh.

4. **Undo/Redo**:
   - Maintains a history of mesh states for undo/redo functionality.

5. **Import/Export**:
   - **Import**: Supports OBJ and STL file formats.
   - **Export**: Exports the current mesh as an OBJ file.

6. **Event Handling**:
   - Tracks mouse movements and clicks for sculpting.

---

## **Code Structure**

- **Initialization**:
  - The `init()` function sets up the scene, camera, renderer, lights, and default mesh.
  - Event listeners are added for UI controls and mouse interactions.

- **Sculpting Logic**:
  - The `onMouseDown()` function detects clicks and applies the selected brush effect.
  - The `sculptVertex()` function modifies vertex positions based on brush type and strength.
  - Symmetry is handled by finding mirrored vertices and applying the same effect.

- **Smoothing**:
  - The `smoothMesh()` function averages vertex positions to smooth the mesh.

- **Undo/Redo**:
  - The `saveState()` function stores the current mesh state in a history array.
  - The `undo()` and `redo()` functions navigate through the history array.

- **Import/Export**:
  - The `importModel()` function reads OBJ or STL files and adds them to the scene.
  - The `exportModel()` function exports the current mesh as an OBJ file.

- **Animation**:
  - The `animate()` function continuously renders the scene and updates the camera controls.

---

## **Potential Improvements**

1. **Performance Optimization**:
   - Use a spatial hash or other efficient data structures for faster vertex lookups.

2. **Additional Brush Types**:
   - Add brushes like flatten, pinch, or crease for advanced sculpting.

3. **UI Enhancements**:
   - Add a color picker or material editor.
   - Include a grid or ground plane for better spatial reference.

4. **Error Handling**:
   - Add error handling for invalid file imports.

5. **Mobile Support**:
   - Add touch event handling for mobile devices.

6. **Export Formats**:
   - Support additional formats like STL or GLTF.

---

## **Usage**

1. Open the HTML file in a modern web browser.
2. Use the right mouse button to sculpt the mesh.
3. Adjust brush settings and symmetry options in the UI.
4. Use the "Smooth" button to refine the mesh.
5. Import or export models using the respective buttons.

---

This editor provides a solid foundation for a 3D sculpting tool and can be extended with additional features and optimizations.
