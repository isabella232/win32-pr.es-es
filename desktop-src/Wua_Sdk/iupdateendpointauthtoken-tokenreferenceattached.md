---
description: Obtiene el formato XML de una referencia adjunta al token.
ms.assetid: F4329A2E-61FD-40E0-9E24-87C9A4585E55
title: Método IUpdateEndpointAuthToken::TokenReferenceAttached (UpdateEndpointAuth.h)
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
ms.openlocfilehash: eae5e616e8583e2a1da8f8aa0882ea25160faad3f064734620466a0353736efe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793865"
---
# <a name="iupdateendpointauthtokentokenreferenceattached-method"></a>IUpdateEndpointAuthToken::TokenReferenceAttached (método)

Obtiene el formato XML de una referencia adjunta al token.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT TokenReferenceAttached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszTokenReference* \[ out\]
</dt> <dd>

Puntero a la referencia de token adjunta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** se realiza correctamente. De lo contrario, devuelve un código com Windows error.

## <a name="remarks"></a>Comentarios

Una referencia adjunta hace referencia a una referencia (como la firma que usa el token) que se encuentra en el mismo mensaje donde reside el token.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio SP3 \[\]<br/>                   |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>                |
| Header<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>UpdateEndpointAuth.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




