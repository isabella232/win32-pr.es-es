---
description: Los proveedores de hora usan las siguientes funciones.
ms.assetid: 05687a67-4e0b-4a44-9c2d-7e097be9008c
title: Funciones de proveedor de hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a24f15bd67751dc09a689078a8a518224267c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668149"
---
# <a name="time-provider-functions"></a>Funciones de proveedor de hora

Los proveedores de hora usan las siguientes funciones.



| Función                                                               | Descripción                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)                     | Notifica al sistema que hay nuevas muestras disponibles.                                              |
| [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)                           | Recupera la información de estado de hora del sistema.                                                           |
| [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)                       | Registra un evento de proveedor de hora en el registro de eventos.                                                           |
| [**SetProviderStatusFunc**](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusfunc)                 | Establece la información de estado del proveedor de hora.                                                           |
| [**SetProviderStatusInfoFreeFunc**](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusinfofreefunc) | Libera una estructura [**SetProviderStatusInfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) .                          |
| [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)                                 | Función de devolución de llamada a la que llama el administrador de proveedores de hora para cerrar el proveedor de hora.        |
| [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)                             | Función de devolución de llamada a la que llama el administrador de proveedores de hora para enviar comandos al proveedor de hora. |
| [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)                                   | Función de devolución de llamada a la que llama el administrador de proveedores de hora cuando se carga el archivo DLL del proveedor de hora.  |



 

 

 



