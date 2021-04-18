---
title: Interfaces del sombreador (gráficos de Direct3D 12)
description: D3d12shader. h declara las siguientes interfaces.
ms.assetid: 791d2c91-3791-47fe-b887-8117ecc798ba
keywords:
- interfaces, sombreador de Direct3D 12
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f111572aacca36f12600b0cf334895684064e5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105720206"
---
# <a name="shader-interfaces-direct3d-12-graphics"></a>Interfaces del sombreador (gráficos de Direct3D 12)

d3d12shader. h declara las siguientes interfaces.

## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection"><strong>ID3D12FunctionParameterReflection</strong></a><br/></td>
<td>Una interfaz de función-parámetro-reflexión obtiene acceso a la información de parámetros de función. <br/>
<blockquote>
[!Note]<br />
Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 12 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection"><strong>ID3D12FunctionReflection</strong></a><br/></td>
<td>Una interfaz de reflexión de funciones obtiene acceso a la información de la función. <br/>
<blockquote>
[!Note]<br />
Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 12 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection"><strong>ID3D12LibraryReflection</strong></a><br/></td>
<td>Una interfaz de reflexión de biblioteca obtiene acceso a la información de la biblioteca. <br/>
<blockquote>
[!Note]<br />
Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 12 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection"><strong>ID3D12ShaderReflection</strong></a><br/></td>
<td>Una interfaz de reflexión del sombreador obtiene acceso a la información del sombreador. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer"><strong>ID3D12ShaderReflectionConstantBuffer</strong></a><br/></td>
<td>Esta interfaz de reflexión del sombreador proporciona acceso a un búfer de constantes. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype"><strong>ID3D12ShaderReflectionType</strong></a><br/></td>
<td>Esta interfaz de reflexión del sombreador proporciona acceso al tipo de variable. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable"><strong>ID3D12ShaderReflectionVariable</strong></a><br/></td>
<td>Esta interfaz de reflexión del sombreador proporciona acceso a una variable. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct3D 12](direct3d-12-reference.md)
</dt> <dt>

[Referencia de los sombreadores](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 





