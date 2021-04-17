---
description: La interfaz ITTime es una interfaz específica del proveedor para un objeto de BLOB de conferencia del Protocolo de descriptor de sesión (SDP).
ms.assetid: 24d33259-dcbe-47e4-9c71-fcc25f6e9a76
title: Interfaz ITTime (Sdpblb. h)
ms.topic: interface
ms.date: 05/31/2018
ms.openlocfilehash: 964fa197318d8cbe9614beb97c5bea0db94f242b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679372"
---
# <a name="ittime-interface"></a>Interfaz ITTime

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La interfaz **ITTime** es una interfaz específica del proveedor para un objeto de BLOB de conferencia del Protocolo de descriptor de sesión (SDP). Proporciona acceso a un conjunto de tiempos de activación para la sesión. Los métodos [**IEnumTime:: Next**](ienumtime-next.md) y [**ITTimeCollection:: Create**](ittimecollection-create.md) crean la interfaz **ITTime** .

## <a name="members"></a>Miembros

La interfaz **ITTime** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITTime** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITTime** tiene estos métodos.



| Método                                         | Descripción                                                                 |
|:-----------------------------------------------|:----------------------------------------------------------------------------|
| [**obtener \_ startTime**](ittime-get-starttime.md) | Obtiene el valor de hora de inicio del NTP de 32 bits (Protocolo de tiempo de red).<br/> |
| [**obtener \_ StopTime**](ittime-get-stoptime.md)   | Obtiene el valor de hora de finalización de NTP.<br/>                                  |
| [**Put \_ startTime**](ittime-put-starttime.md) | Establece el valor de hora de inicio de NTP de 32 bits.<br/>                         |
| [**Put \_ StopTime**](ittime-put-stoptime.md)   | Establece el valor de hora de finalización de NTP.<br/>                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

