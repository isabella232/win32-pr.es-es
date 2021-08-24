---
description: A continuación se muestra la funcionalidad de la interfaz ITConnection.
ms.assetid: 44dc39cf-3222-41ed-b29c-df2d32615500
title: Interfaz ITConnection (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a64758f6a5cf7bcd9106504412f4cf7f39e6fb7ca0b76e35b38e19dc3f815ccf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140348"
---
# <a name="itconnection-interface"></a>Interfaz ITConnection

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz ITConnection** proporciona la siguiente funcionalidad:

-   Proporciona acceso a la dirección y la información de período de vida (TTL) de la sesión.
-   Proporciona acceso a la información de ancho de banda.
-   Habilita la manipulación de la clave de cifrado.

La **interfaz ITConnection** se crea llamando **a QueryInterface** [**en ITConferenceBlob.**](itconferenceblob.md)

## <a name="members"></a>Miembros

La **interfaz ITConnection** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITConnection** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITConnection** tiene estos métodos.



| Método                                                               | Descripción                                                                                                                                    |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ AddressType**](itconnection-get-addresstype.md)             | Obtiene el tipo de dirección.<br/>                                                                                                              |
| [**obtener ancho \_ de banda**](itconnection-get-bandwidth.md)                 | Obtiene el valor de ancho de banda.<br/>                                                                                                               |
| [**get \_ BandwidthModifier**](itconnection-get-bandwidthmodifier.md) | Obtiene el modificador de ancho de banda.<br/>                                                                                                        |
| [**get \_ NetworkType**](itconnection-get-networktype.md)             | Obtiene el tipo de red.<br/>                                                                                                              |
| [**get \_ NumAddresses**](itconnection-get-numaddresses.md)           | Obtiene el número de direcciones que se usarán para la sesión.<br/>                                                                            |
| [**get \_ StartAddress**](itconnection-get-startaddress.md)           | Obtiene la primera dirección que se usará para la sesión.<br/>                                                                                  |
| [**get \_ Ttl**](itconnection-get-ttl.md)                             | Obtiene el [*ámbito de período de*](t-tapgloss.md) vida (TTL) para las transmisiones en las direcciones.<br/> |
| [**GetEncryptionKey**](itconnection-getencryptionkey.md)            | Obtiene la clave de cifrado.<br/>                                                                                                            |
| [**put \_ AddressType**](itconnection-put-addresstype.md)             | Establece el tipo de dirección.<br/>                                                                                                              |
| [**put \_ NetworkType**](itconnection-put-networktype.md)             | Establece el tipo de red.<br/>                                                                                                              |
| [**SetAddressInfo**](itconnection-setaddressinfo.md)                | Establece la información de dirección.<br/>                                                                                                           |
| [**SetBandwidthInfo**](itconnection-setbandwidthinfo.md)            | Establece el valor de ancho de banda.<br/>                                                                                                           |
| [**SetEncryptionKey**](itconnection-setencryptionkey.md)            | Establece la clave de cifrado necesaria para descifrar la sesión o una indicación a un mecanismo para obtener una clave utilizable por medios externos.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

