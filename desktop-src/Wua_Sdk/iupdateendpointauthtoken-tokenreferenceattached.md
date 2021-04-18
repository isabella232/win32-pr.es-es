---
description: Obtiene el formato XML de una referencia adjunta al token.
ms.assetid: F4329A2E-61FD-40E0-9E24-87C9A4585E55
title: 'IUpdateEndpointAuthToken:: TokenReferenceAttached (método) (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceAttached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 9582c54c42e2416d5d7a98e85eba3151fd6769a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686854"
---
# <a name="iupdateendpointauthtokentokenreferenceattached-method"></a>IUpdateEndpointAuthToken:: TokenReferenceAttached (método)

Obtiene el formato XML de una referencia adjunta al token.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT TokenReferenceAttached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszTokenReference* \[ enuncia\]
</dt> <dd>

Puntero a la referencia de token adjunta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ correcto** si se realiza correctamente. De lo contrario, devuelve un código de error COM o Windows.

## <a name="remarks"></a>Observaciones

Una referencia adjunta hace referencia a un referece (como el signiture que usa el token) que está en el mismo mensaje en el que reside el token.

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

 

 




