---
description: La interfaz ITSdp proporciona métodos para la manipulación de un protocolo de descriptor de sesión (SDP, consulte RFC 2327).
ms.assetid: 77c1e302-6290-4eeb-b7c9-462a13b29dcd
title: Interfaz ITSdp (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401dbe2548375227be2ca024ee75de3054fa6f6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681302"
---
# <a name="itsdp-interface"></a>Interfaz ITSdp

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La interfaz **ITSdp** proporciona métodos para la manipulación de un protocolo de descriptor de sesión (SDP, consulte RFC 2327). Proporciona la siguiente funcionalidad:

-   Proporciona acceso a algunas de las propiedades que son comunes a todos los elementos multimedia. Estos incluyen atributos relacionados con la información personal del creador, la descripción de la sesión y la información del tipo de dirección.
-   Proporciona el punto de partida para tener acceso a las colecciones de tiempo y multimedia mediante propiedades.

La interfaz **ITSdp** se crea llamando a **QueryInterface** en [**ITConferenceBlob**](itconferenceblob.md).

## <a name="members"></a>Miembros

La interfaz **ITSdp** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITSdp** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITSdp** tiene estos métodos.



| Método                                                    | Descripción                                                                                         |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**obtener \_ Descripción**](itsdp-get-description.md)         | Obtiene la descripción de la sesión.<br/>                                                            |
| [**obtener \_ IsValid**](itsdp-get-isvalid.md)                 | Valida el BLOB SDP para los valores de estructura y campo.<br/>                                   |
| [**obtener \_ MachineAddress**](itsdp-get-machineaddress.md)   | Obtiene la dirección de la máquina del host de origen.<br/>                                        |
| [**obtener \_ MediaCollection**](itsdp-get-mediacollection.md) | Obtiene un puntero a la interfaz [**ITMediaCollection**](itmediacollection.md) para la Conferencia.<br/> |
| [**obtener \_ nombre**](itsdp-get-name.md)                       | Obtiene el nombre de la sesión.<br/>                                                                   |
| [**obtener \_ autor**](itsdp-get-originator.md)           | Obtiene el autor de la Conferencia.<br/>                                                              |
| [**obtener \_ ProtocolVersion**](itsdp-get-protocolversion.md) | Obtiene la versión del protocolo SDP.<br/>                                                           |
| [**obtener \_ SessionID**](itsdp-get-sessionid.md)             | Obtiene el valor NTP (Protocolo de tiempo de red) de 32 bits que actúa como identificador de sesión.<br/> |
| [**obtener \_ SessionVersion**](itsdp-get-sessionversion.md)   | Obtiene el valor de 32 bits (idealmente NTP) que actúa como versión de la sesión.<br/>                  |
| [**obtener \_ TimeCollection**](itsdp-get-timecollection.md)   | Obtiene un puntero a la interfaz [**ITTimeCollection**](ittimecollection.md) para la Conferencia.<br/>   |
| [**obtener \_ dirección URL**](itsdp-get-url.md)                         | Obtiene la dirección URL.<br/>                                                                            |
| [**GetEmailNames**](itsdp-getemailnames.md)              | Obtiene la matriz de nombres y direcciones de correo electrónico asociada con el BLOB de la Conferencia.<br/>                |
| [**GetPhoneNumbers**](itsdp-getphonenumbers.md)          | Obtiene los números de teléfono.<br/>                                                                  |
| [**poner \_ Descripción**](itsdp-put-description.md)         | Establece la descripción de la sesión.<br/>                                                            |
| [**Put \_ MachineAddress**](itsdp-put-machineaddress.md)   | Establece la dirección de la máquina del host de origen.<br/>                                        |
| [**\_nombre Put**](itsdp-put-name.md)                       | Establece el nombre de la sesión.<br/>                                                                   |
| [**\_originador Put**](itsdp-put-originator.md)           | Obtiene el autor de la Conferencia.<br/>                                                              |
| [**Put \_ SessionVersion**](itsdp-put-sessionversion.md)   | Establece la versión de la sesión.<br/>                                                                    |
| [**\_dirección URL de put**](itsdp-put-url.md)                         | Establece la dirección URL.<br/>                                                                            |
| [**SetEmailNames**](itsdp-setemailnames.md)              | Establece la matriz de nombres de correo electrónico y direcciones asociadas al BLOB de la Conferencia.<br/>                 |
| [**SetPhoneNumbers**](itsdp-setphonenumbers.md)          | Establece los números de teléfono.<br/>                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

