---
description: Solicita un extremo que se utiliza para conectarse a un servicio.
ms.assetid: 4C02EA78-AD77-42CD-B94F-C8C3ED26CB4C
title: 'IUpdateEndpointProvider:: GetServiceEndpoint (método) (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider.GetServiceEndpoint
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bddb77237d6d5edabab41eefe1931514fd6aed42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686856"
---
# <a name="iupdateendpointprovidergetserviceendpoint-method"></a>IUpdateEndpointProvider:: GetServiceEndpoint (método)

Solicita un extremo que se utiliza para conectarse a un servicio.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetServiceEndpoint(
  [in]  GUID                        ServiceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  BOOL                        fRefreshOnline,
  [out] BSTR                        *pbstrEndpointLoc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ServiceId* \[ de\]
</dt> <dd>

Identifica el servicio que se va a actualizar.

</dd> <dt>

*endpointType* \[ de\]
</dt> <dd>

Identifica el tipo de extremo implementado por el servicio.

La enumeración [**UpdateEndpointType**](updateendpointtype.md) define las siguientes constantes.

<dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**


</dt> <dd>

Un punto de conexión cliente-servidor que se utiliza para conectarse al servicio de actualización.

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**


</dt> <dd>

Un punto de conexión de informes que se utiliza cuando el cliente informa de los resultados de los análisis, las descargas y vuelve a instalarse en el servicio de actualización.

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**


</dt> <dd>

Un punto de conexión de Self-Update que se utiliza cuando el equipo cliente se pone en contacto con un servicio de actualización para comprobar si hay una nueva versión del software cliente del agente de Windows Update.

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**


</dt> <dd>

Un punto de conexión de Reglamento que se utiliza cuando el equipo cliente se pone en contacto con el servicio de Reglamento para actuar sobre una actualización determinada que es aplicable al equipo de destino.

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**


</dt> <dd>

Un Simple-Targeting endoint que solo se usa con servicios privados (servidores WSUS en entornos corporativos).

</dd> </dl> </dd> <dt>

*proxySettings* \[ de\]
</dt> <dd>

Identifica la configuración que se usa al conectarse a un servidor proxy.

</dd> <dt>

*hUserToken* \[ de\]
</dt> <dd>

Contiene un objeto de identificador de token que representa al usuario. El proveedor de puntos de conexión usa este token para determinar qué configuración de proxy y credenciales usar.

</dd> <dt>

*fRefreshOnline* \[ de\]
</dt> <dd>

Indica que el WUA meteorológico solicita un nuevo token. True indica que se solicita un token nuevo. False indica que se solicita un token nuevo o almacenado en caché. Vea Comentarios para obtener más información.

</dd> <dt>

*pbstrEndpointLoc* \[ enuncia\]
</dt> <dd>

Especifique la dirección URL que se usa para comunicarse con el servicio. Por ejemplo, para un punto de conexión de cliente-Server sería la dirección URL del servicio de servidor de cliente. Vea Comentarios para obtener más información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ correcto** si se realiza correctamente. De lo contrario, devuelve un código de error COM o Windows.

## <a name="remarks"></a>Observaciones

WUA normalmente establece el parámetro *fRefreshOnline* en false cuando se llama por primera vez a este método y, después, si se produce un error de conexión, WUA establece ese parámetro en true cuando se llama de nuevo al método. Sin embargo, la implementación de este método puede solicitar un nuevo token de un servicio de token de seguridad (STS) o proporcionar un token almacenado en caché en cualquier momento.

Si el extremo no necesita autenticación, el autor de la llamada puede conectarse al servicio usando solo la dirección URL especificada por el parámetro *pbstrEndpointLoc* .

Si el extremo requiere autenticación, el autor de la llamada puede usar la dirección URL especificada por el parámetro *pbstrEndpointLoc* y los datos proporcionados por los demás parámetros.

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

[**IUpdateEndpointProvider**](iupdateendpointprovider.md)
</dt> </dl>

 

 




