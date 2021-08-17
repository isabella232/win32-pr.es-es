---
description: Alterna el suavizado de contorno de línea.
ms.assetid: 9c212823-2dc6-40dd-b1aa-9fc4a2c540f4
title: Método ID3DXLine::SetAntialias (D3dx9core.h)
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
ms.openlocfilehash: 1214b4c045494d3f7ec7f72e94570231b2b84c430759a619491cf8f34869c942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120889"
---
# <a name="id3dxlinesetantialias-method"></a>Método ID3DXLine::SetAntialias

Alterna el suavizado de contorno de línea.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetAntialias(
  [in] BOOL bAntiAlias
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bAntiAlias* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Activa y desactiva el suavizado de contorno. **TRUE** activa el suavizado de contorno y **FALSE** desactiva el suavizado de contorno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine::GetAntialias**](id3dxline--getantialias.md)
</dt> </dl>

 

 
