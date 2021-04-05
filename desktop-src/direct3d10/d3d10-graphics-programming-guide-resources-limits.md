---
description: Esta tabla contiene una lista de los recursos mínimos que admite Direct3D 10.
ms.assetid: 79c13aed-87bd-4875-9810-c3e078f58753
title: Límites de recursos (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ea3e3a181605e548c4e9f0a8b69691564163799
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080299"
---
# <a name="resource-limits-direct3d-10"></a>Límites de recursos (Direct3D 10)

Esta tabla contiene una lista de los recursos mínimos que admite Direct3D 10.



| Recurso                                                                                               | Límite                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| Número de elementos en un búfer de constantes                                                                | 4096                                                 |
| Número de textura (independiente del tamaño de la estructura) en un búfer                                              | 227 textura                                           |
| Dimensión U de Texture1D                                                                                  | 8192                                                 |
| Dimensión Texture1DArray                                                                               | 512 segmentos de matriz                                     |
| Texture2D dimensión de U/V                                                                                | 8192                                                 |
| Dimensión Texture2DArray                                                                               | 512 segmentos de matriz                                     |
| Texture3D dimensión U/V/W                                                                              | 2048                                                 |
| Dimensión TextureCube                                                                                  | 8192                                                 |
| Tamaño del recurso (en MB)                                                                                  | 128 MB ¹                                              |
| Maxanisotropy de filtrado anisotrópico                                                                    | 16                                                   |
| Dimensión de recursos direccionable mediante el filtrado de hardware                                                   | 8192 por dimensión                                   |
| Tamaño de recurso (en MB) direccionable por IA (datos de entrada o de vértice) o VS/GS/PS (ejemplo de punto)              | 128 MB ¹                                              |
| Número total de vistas de recursos por contexto (cada matriz cuenta como 1) (todos los tipos de vista tienen límite compartido) | 220                                                  |
| Tamaño de la estructura de búfer (varios elementos)                                                                  | 2048 bytes                                           |
| Tamaño de salida de flujo                                                                                     | Igual que el número de textura en un búfer (vea más arriba) |
| Recuento de vértices Draw o DrawInstanced (incluida la creación de instancias)                                              | 232                                                  |
| \[Recuento de \] vértices de DrawIndexed () con instancias (incl. Instancing)                                             | 232                                                  |
| Datos de salida de invocación GS ( \* vértices de componentes)                                                     | 1024                                                 |
| Número total de objetos de muestra por contexto                                                            | 4096                                                 |
| Número total de objetos viewport/tijeras por canalización                                                  | 16                                                   |
| Número total de distancias de clip/selección por vértice                                                         | 8                                                    |
| Número total de objetos de Blend por contexto                                                              | 4096                                                 |
| Número total de objetos de profundidad/estarcido por contexto                                                      | 4096                                                 |
| Número total de objetos de estado de rasterización por contexto                                                   | 4096                                                 |
| Número máximo de muestras por píxel durante el muestreo múltiple                                                    | 32                                                   |
| Elemento Vertex del sombreador de recursos: recuento de elementos (componentes de 4 32 bits)                                          | 16                                                   |
| Common-Shader Core (componentes de 4 32 bits) Temp-Register Count (r \# + indexable x \# \[ n \] )             | 4096                                                 |
| Common-Shader Core-ranuras de búfer de constantes                                                               | 14                                                   |
| E//-ranuras de recursos principales del sombreador común                                                                | 128                                                  |
| Ranuras de muestra principales del sombreador común                                                                       | 16                                                   |
| Subrutina principal de sombreador común: límite de anidamiento                                                            | 32                                                   |
| Límite de anidamiento de control de flujo principal de sombreador común                                                          | 64                                                   |
| Entrada de sombreador de vértices: recuento de registros (componentes de 4 32 bits)                                            | 16                                                   |
| Salida del sombreador de vértices: recuento de registros (componentes de 4 32 bits)                                           | 16                                                   |
| Entrada del sombreador de geometría: recuento de registros (componentes de 4 32 bits)                                          | 16                                                   |
| Salida del sombreador de geometría: recuento de registros (componentes de 4 32 bits)                                         | 32                                                   |
| Entrada del sombreador de píxeles: recuento de registros (componentes de 4 32 bits)                                             | 32                                                   |
| Salida del sombreador de píxeles: recuento de registros (componentes de 4 32 bits)                                            | 8                                                    |
| Recuento de registros de profundidad de salida del sombreador de píxeles ( \* componente 1 de 32 bits)                                          | 1                                                    |
| Espacios de recursos de entrada de índice del ensamblador de entrada                                                             | 1                                                    |
| Espacios de recursos de entrada de vértice del ensamblador de entrada                                                            | 16                                                   |



 

¹ las aplicaciones pueden crear recursos mayores que el tamaño máximo de los recursos en el hardware de gráficos. Sin embargo, se recomienda que las aplicaciones mantengan los recursos más pequeños que el tamaño máximo de los recursos para obtener la máxima compatibilidad entre los proveedores de gráficos. El tiempo de ejecución solo garantiza que las asignaciones dentro del tamaño máximo de los recursos son compatibles con todo el hardware de Direct3D 10. Si una aplicación intenta asignar memoria para un recurso dentro del tamaño máximo de recursos, el tiempo de ejecución no podrá realizar el intento solo si el sistema operativo se queda sin recursos. Si una aplicación intenta asignar memoria para un recurso por encima del tamaño máximo de recursos, el tiempo de ejecución puede producir un error en el intento debido a que el sistema operativo está sobreextendido o a que el hardware no admite las asignaciones por encima del tamaño máximo de los recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



