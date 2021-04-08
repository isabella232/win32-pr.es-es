---
title: Ejecutar aplicaciones de 32 bits
description: Ejecute aplicaciones basadas en Windows de 32 bits sin problemas en Windows de 64 bits con el emulador WOW64 x86. Obtenga también información sobre el director del registro, el redirector del sistema de archivos, la instalación de aplicaciones en sistemas de 64 bits y la depuración de WOW64.
ms.assetid: ac75c5af-86e8-4282-9a8e-8db3c22cbda0
keywords:
- Programación de Windows de 64 de bits WOW64
- WOW64 de 64 bits programación de Windows, acerca de
- aplicaciones de 32 bits en la programación de Windows de Windows 64 de 64 bits
- Guía de programación de Windows de 64 bits (programación de Windows de 64 bits, WOW64; véase WOW64)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39872be28da0853f0cff62a9a0ab82065105c687
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995308"
---
# <a name="running-32-bit-applications"></a>Ejecutar aplicaciones de 32 bits

WOW64 es el emulador de x86 que permite que las aplicaciones basadas en Windows de 32 bits se ejecuten sin problemas en Windows de 64 bits. Esto permite que las aplicaciones Windows de 32 bits (x86) se ejecuten sin problemas en Windows de 64 bits (x64), así como para las aplicaciones Windows de 32 bits (x86) y 32 bits (ARM) para que se ejecuten sin problemas en Windows de 64 bits (ARM64). WOW64 se proporciona con el sistema operativo y no es necesario habilitarlo explícitamente. Para obtener más información, consulte detalles de la [implementación de WOW64](wow64-implementation-details.md).

El sistema aísla las aplicaciones de 32 bits de las aplicaciones de 64 bits, lo que incluye evitar colisiones de archivos y del registro. Se admiten las aplicaciones de consola, GUI y servicio. El sistema proporciona interoperabilidad en el límite de 32/64 para escenarios como cortar y pegar y COM. Sin embargo, los procesos de 32 bits no pueden cargar archivos dll de 64 bits para su ejecución y los procesos de 64 bits no pueden cargar archivos dll de 32 bits para su ejecución. Esta restricción no se aplica a las DLL cargadas como archivos de datos o archivos de recursos de imagen; para obtener más información, vea [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa).

Una aplicación de 32 bits puede detectar si se ejecuta bajo WOW64 mediante una llamada a la función [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) (use [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2) si el destino es Windows 10). La aplicación puede obtener información adicional sobre el procesador mediante la función [**GetNativeSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo) .

Tenga en cuenta que Windows de 64 bits no admite la ejecución de aplicaciones basadas en Windows de 16 bits. La razón principal es que los identificadores tienen 32 bits significativos en Windows de 64 bits. Por lo tanto, los identificadores no se pueden truncar y pasar a las aplicaciones de 16 bits sin pérdida de datos. Los intentos de iniciar las aplicaciones de 16 bits producen el siguiente error: **error de \_ \_ \_ formato exe incorrecto**.

## <a name="in-this-section"></a>En esta sección

-   [Rendimiento y consumo de memoria en WOW64](performance-and-memory-consumption.md)
-   [Detalles de la implementación de WOW64](wow64-implementation-details.md)
-   [Redirector del registro](registry-redirector.md)
-   [Redirector del sistema de archivos](file-system-redirector.md)
-   [Administración de memoria](memory-management.md)
-   [Afinidad del procesador](processor-affinity.md)
-   [Comunicación entre procesos](interprocess-communication.md)
-   [Instalación de la aplicación](application-installation.md)
-   [Depurar WOW64](debugging-wow64.md)

 

 