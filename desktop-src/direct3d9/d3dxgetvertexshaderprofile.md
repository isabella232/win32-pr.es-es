---
description: 'Función D3DXGetVertexShaderProfile: devuelve el nombre del perfil de lenguaje de sombreador de alto nivel (HLSL) más alto admitido por un dispositivo determinado.'
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: Función D3DXGetVertexShaderProfile (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetVertexShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 70d6cdf79fdd91e819d54702682515aa3e4810b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114463"
---
# <a name="d3dxgetvertexshaderprofile-function"></a>Función D3DXGetVertexShaderProfile

Devuelve el nombre del perfil de lenguaje de sombreador de alto nivel (HLSL) más alto admitido por un dispositivo determinado.

## <a name="syntax"></a>Sintaxis


```C++
LPCSTR D3DXGetVertexShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero al dispositivo. Vea [**IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nombre del perfil HLSL.

Si el dispositivo no admite sombreadores de vértices, la función devuelve **NULL.**

## <a name="remarks"></a>Comentarios

Un perfil de sombreador especifica la versión del sombreador de ensamblados que se usará y las funcionalidades disponibles para el compilador HLSL al compilar un sombreador. En la tabla siguiente se enumeran los perfiles de sombreador de vértices que se admiten.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Perfil de sombreador</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>vs_1_1</td>
<td>Compile para vs_1_1 versión.</td>
</tr>
<tr class="even">
<td>vs_2_0</td>
<td>Compile para vs_2_0 versión.</td>
</tr>
<tr class="odd">
<td>vs_2_a</td>
<td>Igual que el perfil vs_2_0, con las siguientes funcionalidades adicionales disponibles para que el compilador lo deba tener como destino:
<ul>
<li>El número de registros temporales (r#) es mayor o igual que 13.</li>
<li>Instrucción de control de flujo dinámico.</li>
<li>Predicación.</li>
</ul></td>
</tr>
<tr class="even">
<td>vs_3_0</td>
<td>Compile para vs_3_0 versión.</td>
</tr>
</tbody>
</table>



 

Para obtener más información sobre las diferencias entre las versiones del sombreador, vea [Diferencias de sombreador de vértices.](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
