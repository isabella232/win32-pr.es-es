---
description: Un proveedor de hora se implementa como un archivo DLL. Cada archivo DLL puede admitir varios proveedores de tiempo. Cada proveedor es responsable de su propia configuración y sincronización.
ms.assetid: 04f523d7-7e99-4bf5-941f-ae67f4b9df0a
title: Creación de un proveedor de hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac5a12e19651d88c3328ac72280c486a54c4d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068894"
---
# <a name="creating-a-time-provider"></a>Creación de un proveedor de hora

Un proveedor de hora se implementa como un archivo DLL. Cada archivo DLL puede admitir varios proveedores de tiempo. Cada proveedor es responsable de su propia configuración y sincronización.

Los proveedores de hora deben implementar las siguientes funciones de devolución de llamada:

-   [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)
-   [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)
-   [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)

Después de cargar el archivo DLL del proveedor, el administrador del proveedor de hora llama a [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)y pasa el nombre del proveedor y los punteros a las funciones siguientes:

-   [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)
-   [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)
-   [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

Estas funciones son para que las use el proveedor de hora. El proveedor de hora usa [**TimeProvOpen para**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) devolver un identificador de proveedor que el administrador del proveedor de hora usa al enviar comandos al proveedor de hora. El proveedor de hora define el valor del identificador y se usa principalmente para distinguir entre distintos proveedores implementados en el mismo archivo DLL. El proveedor de hora puede registrar eventos significativos [**mediante LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc).

El administrador del proveedor de hora [**usa TimeProvCommand para**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) enviar comandos al proveedor de hora. Cuando el proveedor de hora necesita notificar al administrador del proveedor de hora que tiene ejemplos de hora disponibles, llama a [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc). A continuación, el administrador del proveedor de hora llama a **TimeProvCommand** con el comando GetSamples de TPC \_ para recuperar los ejemplos de hora. El administrador del proveedor de tiempo puede tardar hasta 16 segundos en solicitar el ejemplo. Por lo tanto, la aplicación no debe esperar a la solicitud.

Para garantizar la precisión, el proveedor de hora debe recuperar toda la información relacionada con el tiempo mediante [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc).

Cuando es el momento de apagar el proveedor de hora, el administrador del proveedor de hora llama a [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).

 

 



