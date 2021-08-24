---
description: 'Función D3DXGetPixelShaderProfile: devuelve el nombre del perfil de lenguaje de sombreador de alto nivel (HLSL) más alto admitido por un dispositivo determinado.'
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
ms.openlocfilehash: dc609e742a4f780f3cb8c34e4dbc4cc40842ee51
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473661"
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




| Perfil de sombreador | Descripción | 
|----------------|-------------|
| ps_1_1 | Compile para ps_1_1 versión. | 
| ps_1_2 | Compile para ps_1_2 versión. | 
| ps_1_3 | Compile para ps_1_3 versión. | 
| ps_1_4 | Compile para ps_1_4 versión. | 
| ps_2_0 | Compile para ps_2_0 versión. | 
| ps_2_a | Igual que el ps_2_0, con las siguientes funcionalidades adicionales disponibles para el compilador de destino:<ul><li>El número de registros temporales (r#) es mayor o igual que 22.</li><li>Swzzle de origen arbitrario.</li><li>Instrucciones de degradado: dsx, dsy.</li><li>Predicación.</li><li>No hay límite de lectura de textura dependiente.</li><li>No hay límite para el número de instrucciones de textura.</li></ul> | 
| ps_2_b | Igual que el ps_2_0, con las siguientes funcionalidades adicionales disponibles para el compilador de destino:<ul><li>El número de registros temporales (r#) es mayor o igual que 32.</li><li>No hay límite para el número de instrucciones de textura.</li></ul> | 
| ps_3_0 | Compile para ps_3_0 versión. | 




 

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

 

 
