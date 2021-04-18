---
description: Obtiene los datos XML (enviados a través de la conexión) que representa el token.
ms.assetid: 52EC991A-0499-4182-AC4F-512BAFB4F896
title: 'IUpdateEndpointAuthToken:: TokenData (método) (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenData
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: e75df7f5b13eaf36854cf7ed9abc5988b02462ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715281"
---
# <a name="iupdateendpointauthtokentokendata-method"></a>IUpdateEndpointAuthToken:: TokenData (método)

Obtiene los datos XML (enviados a través de la conexión) que representa el token.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT TokenData(
  [out] BSTR *pszTokenData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszTokenData* \[ enuncia\]
</dt> <dd>

Datos XML (enviados a través de la conexión) que representa el token. Por ejemplo, los datos de un token WS-Security SAML (Lenguaje de marcado de aserción de seguridad) 1,1 es el código SAML que se agrega a la solicitud.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ correcto** si se realiza correctamente. De lo contrario, devuelve un código de error COM o Windows.

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

 

 




