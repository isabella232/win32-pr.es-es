---
description: Un proveedor de hora se implementa como un archivo DLL. Cada archivo DLL puede admitir varios proveedores de hora. Cada proveedor es responsable de su propia configuración y sincronización.
ms.assetid: 04f523d7-7e99-4bf5-941f-ae67f4b9df0a
title: Creación de un proveedor de hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac5a12e19651d88c3328ac72280c486a54c4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669974"
---
# <a name="creating-a-time-provider"></a>Creación de un proveedor de hora

Un proveedor de hora se implementa como un archivo DLL. Cada archivo DLL puede admitir varios proveedores de hora. Cada proveedor es responsable de su propia configuración y sincronización.

Los proveedores de tiempo deben implementar las siguientes funciones de devolución de llamada:

-   [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)
-   [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)
-   [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)

Una vez cargado el archivo DLL del proveedor, el administrador de proveedores de hora llama a [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen), pasando el nombre del proveedor y punteros a las siguientes funciones:

-   [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)
-   [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)
-   [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

Estas funciones son para su uso por parte del proveedor de hora. El proveedor de hora usa [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) para devolver un identificador de proveedor que utiliza el administrador de proveedores de hora al enviar comandos al proveedor de hora. El proveedor de hora define el valor del identificador y se usa principalmente para distinguir entre los distintos proveedores implementados en el mismo archivo DLL. El proveedor de hora puede registrar eventos importantes mediante [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc).

El administrador de proveedores de hora usa [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) para enviar comandos al proveedor de hora. Cuando el proveedor de hora debe notificar a la hora en que el administrador de proveedores tiene ejemplos de tiempo disponibles, llama a [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc). A continuación, el administrador de proveedores de hora llama a **TimeProvCommand** con el \_ comando TPC GetSamples para recuperar los ejemplos de tiempo. El administrador de proveedores de tiempo puede tardar hasta 16 segundos en solicitar el ejemplo. Por lo tanto, la aplicación no debe esperar a la solicitud.

Para garantizar la precisión, el proveedor de hora debe recuperar toda la información relacionada con el tiempo mediante [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc).

Cuando es el momento de apagar el proveedor de hora, el administrador de proveedores de hora llama a [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).

 

 



