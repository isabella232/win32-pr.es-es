---
description: Alterna el suavizado de contorno de línea.
ms.assetid: 9c212823-2dc6-40dd-b1aa-9fc4a2c540f4
title: 'ID3DXLine:: SetAntialias (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetAntialias
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893e2061beedb6d45dc86e87903613984e3d1785
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698438"
---
# <a name="id3dxlinesetantialias-method"></a>ID3DXLine:: SetAntialias (método)

Alterna el suavizado de contorno de línea.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetAntialias(
  [in] BOOL bAntiAlias
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bAntiAlias* \[ de\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Activa y desactiva el suavizado de contorno. **True** activa el suavizado de contorno y **false** desactiva el suavizado de contorno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine::GetAntialias**](id3dxline--getantialias.md)
</dt> </dl>

 

 
