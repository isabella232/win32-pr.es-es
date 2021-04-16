---
description: Proyecta una función representada en un mapa de cubo en armónicos esféricos.
ms.assetid: de8bc4bd-cb29-44ab-8806-33d3ffd10a7b
title: Función D3DX10SHProjectCubeMap (D3DX10Tex. h)
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
ms.openlocfilehash: fd991e2207f1ad556d9f9b5e648e296b857e884b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689888"
---
# <a name="d3dx10shprojectcubemap-function"></a>D3DX10SHProjectCubeMap función)

Proyecta una función representada en un mapa de cubo en armónicos esféricos.

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

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Orden de la evaluación de SH, genera el orden ^ 2 coefs, Degree es el orden 1.

</dd> <dt>

*pCubeMap* 
</dt> <dd>

Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Mapa que se va a proyectar en armónicos esféricos. Vea [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).

</dd> <dt>

*pROut* 
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Salida SH vector para rojo.

</dd> <dt>

*pGOut* 
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Salida SH vector para verde.

</dd> <dt>

*pBOut* 
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Salida SH vector para azul.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
