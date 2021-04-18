---
description: Devuelve el nombre del perfil de lenguaje de sombreado de alto nivel (HLSL) más alto compatible con un dispositivo determinado.
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: Función D3DXGetVertexShaderProfile (D3DX9Shader. h)
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
ms.openlocfilehash: 34f7ccaeba60bdd1d7c512cee3fb4da29289408a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717755"
---
# <a name="d3dxgetvertexshaderprofile-function"></a>D3DXGetVertexShaderProfile función)

Devuelve el nombre del perfil de lenguaje de sombreado de alto nivel (HLSL) más alto compatible con un dispositivo determinado.

## <a name="syntax"></a>Sintaxis


```C++
LPCSTR D3DXGetVertexShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero al dispositivo. Vea [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nombre del perfil de HLSL.

Si el dispositivo no admite sombreadores de vértices, la función devuelve **null**.

## <a name="remarks"></a>Observaciones

Un perfil de sombreador especifica la versión del sombreador de ensamblado que se va a usar y las capacidades disponibles para el compilador de HLSL al compilar un sombreador. En la tabla siguiente se enumeran los perfiles del sombreador de vértices que se admiten.



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
<td>Compilar para vs_1_1 versión.</td>
</tr>
<tr class="even">
<td>vs_2_0</td>
<td>Compilar para vs_2_0 versión.</td>
</tr>
<tr class="odd">
<td>vs_2_a</td>
<td>Igual que el perfil de vs_2_0, con las siguientes funcionalidades adicionales disponibles para que el compilador tenga como destino:
<ul>
<li>El número de registros temporales (r #) es mayor o igual a 13.</li>
<li>Instrucción de control de flujo dinámico.</li>
<li>Predication.</li>
</ul></td>
</tr>
<tr class="even">
<td>vs_3_0</td>
<td>Compilar para vs_3_0 versión.</td>
</tr>
</tbody>
</table>



 

Para obtener más información sobre las diferencias entre las versiones del sombreador, vea [diferencias del sombreador de vértices](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones del sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
