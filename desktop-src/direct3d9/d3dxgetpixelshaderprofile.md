---
description: 'Función D3DXGetPixelShaderProfile: devuelve el nombre del perfil hlsl (lenguaje de sombreador de alto nivel) más alto admitido por un dispositivo determinado.'
ms.assetid: a6c1be4e-f6f5-4f08-b6a7-b9c621e5f19b
title: Función D3DXGetPixelShaderProfile (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetPixelShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d24e19d49a8a96f91847892f519ef6c06d25ef5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114443"
---
# <a name="d3dxgetpixelshaderprofile-function"></a>Función D3DXGetPixelShaderProfile

Devuelve el nombre del perfil de lenguaje de sombreador de alto nivel (HLSL) más alto admitido por un dispositivo determinado.

## <a name="syntax"></a>Sintaxis


```C++
LPCSTR D3DXGetPixelShaderProfile(
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

Si el dispositivo no admite sombreadores de píxeles, la función devuelve **NULL.**

## <a name="remarks"></a>Comentarios

Un perfil de sombreador especifica la versión del sombreador de ensamblados que se usará y las funcionalidades disponibles para el compilador HLSL al compilar un sombreador. En la tabla siguiente se enumeran los perfiles de sombreador de píxeles que se admiten.



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
<td>ps_1_1</td>
<td>Compile para ps_1_1 versión.</td>
</tr>
<tr class="even">
<td>ps_1_2</td>
<td>Compile para ps_1_2 versión.</td>
</tr>
<tr class="odd">
<td>ps_1_3</td>
<td>Compile para ps_1_3 versión.</td>
</tr>
<tr class="even">
<td>ps_1_4</td>
<td>Compile para ps_1_4 versión.</td>
</tr>
<tr class="odd">
<td>ps_2_0</td>
<td>Compile para ps_2_0 versión.</td>
</tr>
<tr class="even">
<td>ps_2_a</td>
<td>Igual que el perfil ps_2_0, con las siguientes funcionalidades adicionales disponibles para que el compilador sea el destino:
<ul>
<li>El número de registros temporales (r#) es mayor o igual que 22.</li>
<li>Swzzle de origen arbitrario.</li>
<li>Instrucciones de degradado: dsx, dsy.</li>
<li>Predicación.</li>
<li>No hay límite de lectura de textura dependiente.</li>
<li>No hay límite para el número de instrucciones de textura.</li>
</ul></td>
</tr>
<tr class="odd">
<td>ps_2_b</td>
<td>Igual que el perfil ps_2_0, con las siguientes funcionalidades adicionales disponibles para que el compilador sea el destino:
<ul>
<li>El número de registros temporales (r#) es mayor o igual que 32.</li>
<li>No hay límite para el número de instrucciones de textura.</li>
</ul></td>
</tr>
<tr class="even">
<td>ps_3_0</td>
<td>Compile para ps_3_0 versión.</td>
</tr>
</tbody>
</table>



 

Para obtener más información sobre las diferencias entre las versiones del sombreador, vea [Diferencias del sombreador de píxeles.](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
