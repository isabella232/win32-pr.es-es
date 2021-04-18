---
description: Obtiene el identificador del servicio que se va a autenticar con el token del extremo.
ms.assetid: FE110B8E-F8FB-4CC8-BDD8-6427BA8B7920
title: 'IUpdateEndpointAuthToken:: ServiceID (método) (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.ServiceID
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 8384baa0a4f8bb48e603e0f2f8bed417e783b7f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715282"
---
# <a name="iupdateendpointauthtokenserviceid-method"></a>IUpdateEndpointAuthToken:: ServiceID (método)

Obtiene el identificador del servicio que se va a autenticar con el token del extremo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ServiceID(
  [out] GUID *pServiceID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pServiceID* \[ enuncia\]
</dt> <dd>

Identificador del servicio.

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

 

 




