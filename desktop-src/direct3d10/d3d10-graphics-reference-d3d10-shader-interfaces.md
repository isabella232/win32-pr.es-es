---
description: 'Esta sección contiene información sobre las siguientes interfaces de sombreador:'
ms.assetid: d8770b45-a05c-4dd8-9fa7-08fb4330d734
title: Interfaces de sombreador (gráficos de Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96962407492f5fc6b6f7bbacd155c265ffd03e11eff31f2b012a2d1c644d3f9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409155"
---
# <a name="shader-interfaces-direct3d-10-graphics"></a>Interfaces de sombreador (gráficos de Direct3D 10)

Esta sección contiene información sobre las siguientes interfaces de sombreador:

Cada una de estas interfaces de sombreador administra un sombreador compilado. La interfaz se crea cuando se compila un sombreador y, a continuación, se pasa a varias API que necesitan acceso a un sombreador compilado. por ejemplo, al enlazar un sombreador a una fase de canalización u obtener una firma de sombreador.



| Pipeline-Stage interfaces                                      | Descripción                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interfaz ID3D10GeometryShader**](/windows/win32/api/d3d10/nn-d3d10-id3d10geometryshader) | Un sombreador de geometría implementa el procesamiento por primitiva en la fase [del sombreador de geometría.](d3d10-graphics-programming-guide-pipeline-stages.md) |
| [**Interfaz ID3D10PixelShader**](/windows/win32/api/d3d10/nn-d3d10-id3d10pixelshader)       | Un sombreador de píxeles implementa el procesamiento por píxel en la fase [del sombreador de píxeles](d3d10-graphics-programming-guide-pipeline-stages.md).           |
| [**Interfaz ID3D10VertexShader**](/windows/win32/api/d3d10/nn-d3d10-id3d10vertexshader)     | Un sombreador de vértices implementa el procesamiento por vértice en la fase [del sombreador de vértices](d3d10-graphics-programming-guide-pipeline-stages.md).        |



 

Las interfaces de reflexión de sombreador permiten a una aplicación inspeccionar el contenido de un sombreador en tiempo de diseño o creación. La reflexión del sombreador no es útil para establecer variables en tiempo de ejecución, ya que es un reflejo de los datos del sombreador y, por tanto, no admite ningún método para establecer datos.



| Shader-Reflection interfaces                                                                   | Descripción                                                                        |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Interfaz ID3D10ShaderReflection**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)                             | Interfaz COM para leer información de un sombreador compilado en tiempo de creación.     |
| [**Interfaz ID3D10ShaderReflectionConstantBuffer**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer) | Interfaz auxiliar para obtener una interfaz de búfer constante de reflexión de sombreador.      |
| [**Interfaz ID3D10ShaderReflectionType**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectiontype)                     | Interfaz auxiliar para obtener una interfaz de tipo de reflexión de sombreador.                 |
| [**Interfaz ID3D10ShaderReflectionVariable**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionvariable)             | Interfaz auxiliar para obtener una interfaz de variable de reflexión de sombreador.             |
| [**Interfaz ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)                         | Interfaz de reflexión de sombreador para leer información de una vista de recursos de sombreador. |



 

Las API de reflexión de sombreador implementan una interfaz de reflexión de sombreador COM [**(interfaz ID3D10ShaderReflection)**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)y varias interfaces auxiliares que no son COM (el resto de las interfaces). **La interfaz ID3D10ShaderReflection** se crea cuando se crea un objeto de reflexión de sombreador. Sigue las reglas COM estándar; La creación de la interfaz aumenta un recuento de referencias y la interfaz debe liberarse cuando ya no sea necesaria. Las interfaces restantes de reflexión de sombreador son interfaces auxiliares que no heredan de IUnknown. Esto significa que no cambian ningún recuento de referencias cuando se crean y no es necesario destruirlos cuando haya terminado con ellos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de los sombreadores](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 
