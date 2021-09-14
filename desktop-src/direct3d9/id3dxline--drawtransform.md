---
description: Dibuja una franja de líneas en el espacio de pantalla con una matriz de transformación de entrada especificada.
ms.assetid: 869dc705-8162-4cd9-ac6a-c0ce32f430c3
title: Método ID3DXLine::D rawTransform (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.DrawTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 52407a8c92e626f8fe4d2df817017f81806cbae9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060582"
---
# <a name="id3dxlinedrawtransform-method"></a>Método ID3DXLine::D rawTransform

Dibuja una franja de líneas en el espacio de pantalla con una matriz de transformación de entrada especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DrawTransform(
  [in] const D3DXVECTOR3 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in] const D3DXMATRIX  *pTransform,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVertexList* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Matriz de vértices que forma la línea. Vea [**D3DXVECTOR3**](d3dxvector3.md).

</dd> <dt>

*dwVertexListCount* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices en la lista de vértices.

</dd> <dt>

*pTransform* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matriz de escala, rotación y traducción (SRT) para transformar los puntos. Vea [**D3DXMATRIX.**](d3dxmatrix.md) Si esta matriz es una matriz de proyección, se dibujarán las líneas con un patrón de ppling correcto para la perspectiva. O bien, puede transformar los vértices y usar [**ID3DXLine::D raw**](id3dxline--draw.md) para dibujar la línea con un patrón de estippla no especificado y correcto.

</dd> <dt>

*Color* \[ En\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Color de la línea. Vea [**D3DCOLOR**](d3dcolor.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
