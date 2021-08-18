---
title: Comparación de Windows 2000 frente a RRAS Redistributable
description: La API ras se distribuye como una característica de los sistemas operativos Windows 2000 y versiones posteriores y está disponible como redistribuible para Windows NT 4.0 con Service Pack 3 (SP3) y versiones anteriores.
ms.assetid: fd6c76b9-52e2-405e-b62e-055cfbdb5ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 027c120133573b1d0c452b74dd02ab8fa0aa6f3367eb1a5fc9668a2de089c758
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995345"
---
# <a name="function-comparison-windows-2000-vs-rras-redistributable"></a>Comparación de funciones: Windows 2000 frente a RRAS Redistributable

La API ras se distribuye como una característica de los sistemas operativos Windows 2000 y versiones posteriores y está disponible como redistribuible para Windows NT 4.0 con Service Pack 3 (SP3) y versiones anteriores. RAS proporciona la misma funcionalidad en ambos formatos, pero la convención de nomenclatura que se usa es diferente para los elementos de referencia de cada versión de la API ras.

Las funciones ras para Windows NT 4.0 con SP3 y versiones anteriores suelen comenzar con el prefijo "RasAdmin". Las funciones análogas para el servicio de enrutamiento y acceso remoto (RRAS) comienzan con el prefijo "MprAdmin". Por ejemplo, RAS proporciona una función denominada [**RasAdminPortGetInfo**](rasadminportgetinfo.md). La función análoga de RRAS se denomina [**MprAdminPortGetInfo.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) Como ejemplo similar, RAS proporciona la función de devolución de llamada [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md). RRAS proporciona una función de devolución de llamada similar denominada [**MprAdminGetIpAddressForUser.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) Las excepciones a esta regla son [**RasAdminPortClearStatistics,**](rasadminportclearstatistics.md)que en RRAS es [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)y [**RasAdminFreeBuffer,**](rasadminfreebuffer.md)que en RRAS es [**MprAdminBufferFree.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)

En la tabla siguiente se enumeran Windows funciones RAS de NT 4.0 SP3 y las funciones RRAS correspondientes.



| Windows NT 4.0 RAS                                                                   | Rras                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)                   | [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection)                   |
| [**RasAdminConnectionConexiónAdminupNotification**](rasadminconnectionhangupnotification.md) | [**MprAdminConnectionConnectionConnectionupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) |
| [**RasAdminFreeBuffer**](rasadminfreebuffer.md)                                     | [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)                                     |
| [**RasAdminGetErrorString**](rasadmingeterrorstring.md)                             | [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)                             |
| [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md)                   | [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser)                   |
| [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md)                   | [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)                             |
| [**RasAdminPortDisconnect**](rasadminportdisconnect.md)                             | [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)                             |
| [**RasAdminPortEnum**](rasadminportenum.md)                                         | [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)                                         |
| [**RasAdminPortGetInfo**](rasadminportgetinfo.md)                                   | [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)                                   |
| [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md)                         | [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)                         |
| [**RasAdminUserGetInfo**](rasadminusergetinfo.md)                                   | [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)                                   |
| [**RasAdminUserSetInfo**](rasadminusersetinfo.md)                                   | [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)                                   |



 

Aunque las funciones RRAS son similares a su Windows NT 4.0 con SP3 y sus equivalentes ras anteriores en la funcionalidad, las funciones de RRAS suelen tomar un conjunto diferente de parámetros. Consulte la página de referencia de una función determinada para obtener información completa sobre la lista de parámetros de esa función.

El RRAS redistribuible para Windows NT 4.0 con SP3 y versiones anteriores agrega las siguientes funciones, que no tienen equivalentes ras:

[**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[**MprAdminConnectionClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)

[**MprAdminConnectionEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)

[**MprAdminConnectionGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)

[**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)

[**MprAdminIsServiceRunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)

[**MprAdminLinkLinkLinkupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[**MprAdminPortReset**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

[**MprAdminServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)

[**MprAdminServerDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

Además de las funciones anteriores, Windows 2000 y sistemas operativos posteriores agregan las siguientes funciones:

[**MprAdminSendUserMessage**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)

[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)

[**MprAdminConnectionConnectionConexiónNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

 

 




