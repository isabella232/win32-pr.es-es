---
description: Obtiene la clave que se usa para cifrar los mensajes salientes que protege el token.
ms.assetid: 1ADBDFC8-E4D9-440B-B310-913213086283
title: Método IUpdateEndpointAuthToken::SigningKey (UpdateEndpointAuth.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.SigningKey
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 45e513483db561ad27e9f1c2f7e18457b039d4bd7eaa1aaa61194443c8ccc78e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855745"
---
# <a name="iupdateendpointauthtokensigningkey-method"></a>IUpdateEndpointAuthToken::SigningKey (Método)

Obtiene la clave que se usa para cifrar los mensajes salientes que protege el token.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SigningKey(
  [in, out, unique] BYTE  *pbKey,
  [in, out]         ULONG *pcbKeySize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbKey* \[ in, out\]
</dt> <dd>

Clave usada para cifrar el mensaje saliente.

</dd> <dt>

*pwKeySize* \[ in, out\]
</dt> <dd>

Tamaño de la clave a la que hace referencia el *parámetro pbkey.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** se realiza correctamente. De lo contrario, devuelve un código de error COM Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio sp3 \[\]<br/>                   |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>                |
| Header<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>UpdateEndpointAuth.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




