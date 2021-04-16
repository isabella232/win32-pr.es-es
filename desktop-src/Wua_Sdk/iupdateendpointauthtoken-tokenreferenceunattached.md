---
description: Obtiene el formato XML de una referencia no adjunta al token.
ms.assetid: D5D61ED7-68FB-4FC0-9C2A-90D3B1219351
title: 'IUpdateEndpointAuthToken:: TokenReferenceUnattached (método) (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceUnattached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 7f9a25c444cf1ba8421d3787a9ead242750e5756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705725"
---
# <a name="iupdateendpointauthtokentokenreferenceunattached-method"></a>IUpdateEndpointAuthToken:: TokenReferenceUnattached (método)

Obtiene el formato XML de una referencia no adjunta al token.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT TokenReferenceUnattached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszTokenReference* \[ enuncia\]
</dt> <dd>

Puntero a la referencia de token no adjunta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ correcto** si se realiza correctamente. De lo contrario, devuelve un código de error COM o Windows.

## <a name="remarks"></a>Observaciones

Una referencia no adjunta hace referencia a un referece (como el signiture que usa el token) que no está en el mensaje en el que reside el token.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]<br/>                   |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]<br/>                |
| Encabezado<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




