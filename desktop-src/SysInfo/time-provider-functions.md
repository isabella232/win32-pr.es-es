---
description: Los proveedores de hora usan las siguientes funciones.
ms.assetid: 05687a67-4e0b-4a44-9c2d-7e097be9008c
title: Funciones del proveedor de hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c0647574aaa807788e9cf510ce9293460c0394bcdaa794e243009ad6710bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884820"
---
# <a name="time-provider-functions"></a>Funciones del proveedor de hora

Los proveedores de hora usan las siguientes funciones.



| Función                                                               | Descripción                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)                     | Notifica al sistema que hay nuevos ejemplos disponibles.                                              |
| [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)                           | Recupera la información de estado de hora del sistema.                                                           |
| [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)                       | Registra un evento de proveedor de hora en el registro de eventos.                                                           |
| [**SetProviderStatusFunc**](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusfunc)                 | Establece la información de estado del proveedor de hora.                                                           |
| [**SetProviderStatusInfoFreeFunc**](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusinfofreefunc) | Libera una [**estructura SetProviderStatusInfo.**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo)                          |
| [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)                                 | Función de devolución de llamada a la que llama el administrador del proveedor de hora para apagar el proveedor de hora.        |
| [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)                             | Función de devolución de llamada a la que llama el administrador del proveedor de hora para enviar comandos al proveedor de hora. |
| [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)                                   | Función de devolución de llamada a la que llama el administrador del proveedor de hora cuando se carga el archivo DLL del proveedor de hora.  |



 

 

 



