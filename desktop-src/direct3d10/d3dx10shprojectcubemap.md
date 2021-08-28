---
description: Proyecta una función representada en un mapa de cubo en armónicas esféricas.
ms.assetid: de8bc4bd-cb29-44ab-8806-33d3ffd10a7b
title: Función D3DX10SHProjectCubeMap (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SHProjectCubeMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4fa30724bed56e86d16626133ab32e3494d3c71d6ffa839be1520518c97a77fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990465"
---
# <a name="d3dx10shprojectcubemap-function"></a>Función D3DX10SHProjectCubeMap

Proyecta una función representada en un mapa de cubo en armónicas esféricas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10SHProjectCubeMap(
   UINT            Order,
   ID3D10Texture2D *pCubeMap,
   FLOAT           *pROut,
   FLOAT           *pGOut,
   FLOAT           *pBOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pedido* 
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

El orden de la evaluación de SH genera Order^2 coefs, degree es Order-1.

</dd> <dt>

*pCubeMap* 
</dt> <dd>

Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Mapa de cubo que se va a proyectar en armónicos esféricos. Vea [**ID3D10Texture2D.**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)

</dd> <dt>

*Prout* 
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Vector SH de salida para rojo.

</dd> <dt>

*pGOut* 
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Vector SH de salida para verde.

</dd> <dt>

*pBOut* 
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Vector SH de salida para azul.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
