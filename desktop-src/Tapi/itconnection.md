---
description: A continuación se muestra la funcionalidad de la interfaz ITConnection.
ms.assetid: 44dc39cf-3222-41ed-b29c-df2d32615500
title: Interfaz ITConnection (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00da80631c0ef4e8186aa36425f18e4d2a62bfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681140"
---
# <a name="itconnection-interface"></a>Interfaz ITConnection

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La interfaz **ITConnection** proporciona la funcionalidad siguiente:

-   Proporciona acceso a la información de la dirección y el período de vida (TTL) de la sesión.
-   Proporciona acceso a la información de ancho de banda.
-   Habilita la manipulación de la clave de cifrado.

La interfaz **ITConnection** se crea llamando a **QueryInterface** en [**ITConferenceBlob**](itconferenceblob.md).

## <a name="members"></a>Miembros

La interfaz **ITConnection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITConnection** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITConnection** tiene estos métodos.



| Método                                                               | Descripción                                                                                                                                    |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ AddressType**](itconnection-get-addresstype.md)             | Obtiene el tipo de dirección.<br/>                                                                                                              |
| [**obtener \_ ancho de banda**](itconnection-get-bandwidth.md)                 | Obtiene el valor de ancho de banda.<br/>                                                                                                               |
| [**obtener \_ BandwidthModifier**](itconnection-get-bandwidthmodifier.md) | Obtiene el modificador de ancho de banda.<br/>                                                                                                        |
| [**obtener \_ NetworkType**](itconnection-get-networktype.md)             | Obtiene el tipo de red.<br/>                                                                                                              |
| [**obtener \_ NumAddresses**](itconnection-get-numaddresses.md)           | Obtiene el número de direcciones que se van a utilizar para la sesión.<br/>                                                                            |
| [**obtener \_ StartAddress**](itconnection-get-startaddress.md)           | Obtiene la primera dirección que se va a utilizar para la sesión.<br/>                                                                                  |
| [**obtener \_ TTL**](itconnection-get-ttl.md)                             | Obtiene el ámbito del [*período*](t-tapgloss.md) de vida (TTL) para las transmisiones en las direcciones.<br/> |
| [**GetEncryptionKey**](itconnection-getencryptionkey.md)            | Obtiene la clave de cifrado.<br/>                                                                                                            |
| [**Put \_ AddressType**](itconnection-put-addresstype.md)             | Establece el tipo de dirección.<br/>                                                                                                              |
| [**Put \_ NetworkType**](itconnection-put-networktype.md)             | Establece el tipo de red.<br/>                                                                                                              |
| [**SetAddressInfo**](itconnection-setaddressinfo.md)                | Establece la información de dirección.<br/>                                                                                                           |
| [**SetBandwidthInfo**](itconnection-setbandwidthinfo.md)            | Establece el valor de ancho de banda.<br/>                                                                                                           |
| [**SetEncryptionKey**](itconnection-setencryptionkey.md)            | Establece la clave de cifrado necesaria para descifrar la sesión o una indicación de un mecanismo para obtener una clave utilizable de forma externa.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

