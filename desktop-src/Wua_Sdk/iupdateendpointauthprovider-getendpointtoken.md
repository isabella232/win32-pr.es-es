---
description: Solicite un token para el extremo del servicio con las credenciales especificadas.
ms.assetid: 2CA0F826-9A05-4385-AF1A-A8C05B3DAFE2
title: 'IUpdateEndpointAuthProvider:: GetEndpointToken (método) (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetEndpointToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 55efe38ce9782b691e1ad32f7a21f6124e1f0bf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810208"
---
# <a name="iupdateendpointauthprovidergetendpointtoken-method"></a>IUpdateEndpointAuthProvider:: GetEndpointToken (método)

Solicite un token para el extremo del servicio con las credenciales especificadas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetEndpointToken(
  [in]  GUID                        serviceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  UpdateEndpointAuthTokenType tokenType,
  [in]  BOOL                        fRefreshOnline,
  [out] IUnknown                    **ppEndpointToken
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*serviceId* \[ de\]
</dt> <dd>

Identifica el servicio que se va a actualizar.

</dd> <dt>

*endpointType* \[ de\]
</dt> <dd>

Identifica el tipo de extremo que implementa el servicio.

</dd> <dt>

*proxySettings* \[ de\]
</dt> <dd>

La configuración que se utilizará al conectarse a un servidor proxy. Para obtener más información, vea la estructura [**UpdateEndpointProxySettings**](updateendpointproxysettings.md) .

</dd> <dt>

*hUserToken* \[ de\]
</dt> <dd></dd> <dt>

*tokenType* \[ de\]
</dt> <dd>

Identifica el tipo de token de autenticación que se utiliza para la autenticación.

</dd> <dt>

*fRefreshOnline* \[ de\]
</dt> <dd>

Indica que el WUA meteorológico solicita un nuevo token. True indica que se solicita un token nuevo. False indica que se solicita un token nuevo o almacenado en caché. Vea Comentarios para obtener más información.

</dd> <dt>

*ppEndpointToken* \[ enuncia\]
</dt> <dd>

Especifique el token del punto de conexión que se va a usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto si se realiza correctamente. De lo contrario, devuelve un código de error COM o Windows.

## <a name="remarks"></a>Observaciones

WUA normalmente establece el parámetro fRefreshOnline en false cuando se llama por primera vez a este método y, después, si se produce un error de conexión, WUA establece ese parámetro en true cuando se llama de nuevo al método. Sin embargo, la implementación de este método puede solicitar un nuevo token de un servicio de token de seguridad (STS) o proporcionar un token almacenado en caché en cualquier momento.

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

[**IUpdateEndpointAuthProvider**](iupdateendpointauthprovider.md)
</dt> </dl>

 

 




