---
description: La interfaz ITSdp proporciona métodos para la manipulación de un componente de blob de conferencia del Protocolo de descriptor de sesión (SDP, consulte RFC 2327).
ms.assetid: 77c1e302-6290-4eeb-b7c9-462a13b29dcd
title: Interfaz ITSdp (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401dbe2548375227be2ca024ee75de3054fa6f6f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073487"
---
# <a name="itsdp-interface"></a>Interfaz ITSdp

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz ITSdp** proporciona métodos para la manipulación de un componente de blob de conferencia del Protocolo de descriptor de sesión (SDP, consulte RFC 2327). Proporciona la siguiente funcionalidad:

-   Proporciona acceso a algunas de las propiedades que son comunes a todos los medios. Estos incluyen atributos que pertenecen a la información personal del creador, la descripción de la sesión y la información del tipo de dirección.
-   Proporciona el punto de partida para acceder a las colecciones de tiempo y medios a través de propiedades.

La **interfaz ITSdp** se crea mediante una llamada **a QueryInterface** en [**ITConferenceBlob**](itconferenceblob.md).

## <a name="members"></a>Members

La **interfaz ITSdp** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITSdp** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITSdp** tiene estos métodos.



| Método                                                    | Descripción                                                                                         |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**get \_ Description**](itsdp-get-description.md)         | Obtiene la descripción de la sesión.<br/>                                                            |
| [**get \_ IsValid**](itsdp-get-isvalid.md)                 | Valida el blob SDP para los valores de estructura y campo.<br/>                                   |
| [**get \_ MachineAddress**](itsdp-get-machineaddress.md)   | Obtiene la dirección del equipo del host de origen.<br/>                                        |
| [**get \_ MediaCollection**](itsdp-get-mediacollection.md) | Obtiene el puntero a [**la interfaz ITMediaCollection**](itmediacollection.md) para la conferencia.<br/> |
| [**get \_ Name**](itsdp-get-name.md)                       | Obtiene el nombre de la sesión.<br/>                                                                   |
| [**get \_ Originator**](itsdp-get-originator.md)           | Obtiene el originador de la conferencia.<br/>                                                              |
| [**get \_ ProtocolVersion**](itsdp-get-protocolversion.md) | Obtiene la versión del protocolo SDP.<br/>                                                           |
| [**get \_ SessionId**](itsdp-get-sessionid.md)             | Obtiene el valor NTP (Protocolo de tiempo de red) de 32 bits que actúa como identificador de sesión.<br/> |
| [**get \_ SessionVersion**](itsdp-get-sessionversion.md)   | Obtiene el valor de 32 bits (idealmente NTP) que actúa como versión de sesión.<br/>                  |
| [**get \_ TimeCollection**](itsdp-get-timecollection.md)   | Obtiene el puntero a [**la interfaz ITTimeCollection**](ittimecollection.md) para la conferencia.<br/>   |
| [**get \_ Url**](itsdp-get-url.md)                         | Obtiene la dirección URL.<br/>                                                                            |
| [**GetEmailNames**](itsdp-getemailnames.md)              | Obtiene la matriz de nombres de correo electrónico y direcciones asociadas con el blob en conferencias.<br/>                |
| [**GetPhoneNumbers**](itsdp-getphonenumbers.md)          | Obtiene los números de teléfono.<br/>                                                                  |
| [**put \_ Description**](itsdp-put-description.md)         | Establece la descripción de la sesión.<br/>                                                            |
| [**put \_ MachineAddress**](itsdp-put-machineaddress.md)   | Establece la dirección del equipo del host de origen.<br/>                                        |
| [**put \_ Name**](itsdp-put-name.md)                       | Establece el nombre de la sesión.<br/>                                                                   |
| [**put \_ Originator**](itsdp-put-originator.md)           | Obtiene el originador de la conferencia.<br/>                                                              |
| [**put \_ SessionVersion**](itsdp-put-sessionversion.md)   | Establece la versión de la sesión.<br/>                                                                    |
| [**Put \_ Url**](itsdp-put-url.md)                         | Establece la dirección URL.<br/>                                                                            |
| [**SetEmailNames**](itsdp-setemailnames.md)              | Establece la matriz de nombres de correo electrónico y direcciones asociadas con el blob en conferencias.<br/>                 |
| [**SetPhoneNumbers**](itsdp-setphonenumbers.md)          | Establece los números de teléfono.<br/>                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

