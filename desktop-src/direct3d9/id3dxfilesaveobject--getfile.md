---
description: Obtiene la interfaz ID3DXFile del objeto que creó este objeto ID3DXFileSaveObject.
ms.assetid: 79249d17-cae3-43d9-9ccb-fa804b02a353
title: Método ID3DXFileSaveObject::GetFile (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3f46344244405aca80789ae45db172e7693c6a01f77a014737a90080c1e3f21c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121199"
---
# <a name="id3dxfilesaveobjectgetfile-method"></a>Método ID3DXFileSaveObject::GetFile

Obtiene la [**interfaz ID3DXFile**](id3dxfile.md) del objeto que creó este [**objeto ID3DXFileSaveObject.**](id3dxfilesaveobject.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFile(
  [in] ID3DXFile ppFile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppFile* \[ En\]
</dt> <dd>

Tipo: **[ **ID3DXFile**](id3dxfile.md)**

Dirección de un puntero a un [**objeto ID3DXFile.**](id3dxfile.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DXFERR \_ BADVALUE, E \_ NOINTERFACE, E \_ POINTER.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 




