# SAGE-VLM

<p align="center">
  <img src="image/1.png" alt="SAGE-VLM Pipeline" width="100%">
</p>

**SAGE-VLM** is a highly efficient vision-language model framework tailored for autonomous system perception in highly dynamic and complex urban environments. It addresses the critical demands for real-time inference on edge devices by overcoming severe coordinate aliasing and the destructive collapse of rigid spatial topologies found in existing architectures.

## 1. Project Features

*   **Multi-View Decoupled 2D Rotary Positional Encoding (MVD-RoPE)**
   <p align="center">
  <img src="image/2d.png" alt="SAGE-VLM Pipeline" width="100%">
</p>

Explicitly injects fine-grained spatial inductive biases natively into the attention layers. It strictly decouples continuous view boundaries, successfully eliminating multi-camera spatial confusion.

*   **Semantic-Conditioned Visual Residual (SCVR)**
  <p align="center">
  <img src="image/ronghe.png" alt="SAGE-VLM Pipeline" width="100%">
</p>

Extracts an adaptive pure text query to serve as a non-destructive semantic gate. It dynamically filters task-irrelevant background noise while strictly preserving the underlying spatial topology through a residual pathway.

*   **Extreme Parameter Efficiency**

Built upon a highly condensed language backbone of exactly 20.3 million parameters, SAGE-VLM strikes an optimal balance between inference throughput and topological fidelity for edge deployment. The framework operates under extreme hardware bottlenecks, consuming only 0.19 GB of continuous memory while sustaining 19.90 GFLOPs.

## 2. Main Contributions

*   **MVD-RoPE Innovation**: Introduction of a spatial encoding scheme tailored for multi-camera arrays, restoring precise 2D topological inductive biases without introducing cross-view coordinate aliasing.
*   **SCVR Architecture**: Proposal of a novel module leveraging a fail-safe residual pathway to isolate critical visual structures from redundant background noise without erasing unprompted safety-critical obstacles.
*   **Comprehensive SAGE-VLM Framework**: Development of a complete pipeline that outpaces standard baseline architectures in larger configurations across advanced semantic alignment metrics on the DriveLM benchmark.

## 3. Related Visualizations

### 3.1 Comprehensive Pipeline Overview

SAGE-VLM processes multi-view continuous frame sequences through a decoupled lightweight backbone, preserving structural spatial relations via MVD-RoPE and purifying features using the SCVR non-destructive gate.

### 3.2 MVD-RoPE Technical Architecture

Illustration of the spatial encoding scheme where the input feature matrix is split to enable independent Y-axis and X-axis orthogonal rotary transformations on continuous shot grids.

### 3.3 SCVR Prior Fusion Framework

Internal design depicting the distillation of an adaptive pure text query to drive the non-destructive residual gate, amplifying text-aligned driving cues while maintaining baseline spatial topologies.

### 3.4 Qualitative Validation and Safety Assurance

Visual comparison demonstrating how SAGE-VLM prevents semantic blindness by amplifying task-aligned vehicle tokens while structurally preserving unprompted safety-critical visual tokens, such as pedestrians, which traditional hard-dropping methods erroneously eradicate.
