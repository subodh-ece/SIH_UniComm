## 🔄 Workflow Architecture

```mermaid
graph TD
    A[Helmet Geometry] -->|Scan/Define| B(3D Helmet Modelling)
    B -->|Surface Extraction| C{Antenna Design}
    C -->|Parametric Setup| D[EM Simulation & Optimization]
    D -->|Performance Validation| E[S-Parameter + Radiation + SAR Analysis]
    E -->|Design Finalization| F[Direct-Write Fabrication<br><i>Conductive ink on conformal substrate</i>]
    F -->|Assembly| G(Prototype Integration)
    G -->|VNA & Chamber Tests| H((RF Measurement & Optimization))

    classDef phase1 fill:#e1f5fe,stroke:#01579b,stroke-width:2px,color:#000;
    classDef phase2 fill:#fff3e0,stroke:#e65100,stroke-width:2px,color:#000;
    classDef phase3 fill:#e8f5e9,stroke:#1b5e20,stroke-width:2px,color:#000;

    class A,B phase1;
    class C,D,E phase2;
    class F,G,H phase3;
