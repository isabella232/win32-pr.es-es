---
title: Ejecución de aplicaciones de 32 bits
description: Ejecute aplicaciones basadas en Windows de 32 bits sin problemas en Windows de 64 bits con el emulador WOW64 x86. Obtenga también información sobre el director del Registro, el redirector del sistema de archivos, la instalación de aplicaciones en sistemas de 64 bits y la depuración wow64.
ms.assetid: ac75c5af-86e8-4282-9a8e-8db3c22cbda0
keywords:
- Wow64 64-bit Windows programación
- WOW64 de 64 bits Windows programación , acerca de
- Aplicaciones de 32 bits en programación de 64 Windows de 64 Windows bits
- Guía de programación de Windows de 64 bits de 64 Windows programación , WOW64 Vea WOW64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39872be28da0853f0cff62a9a0ab82065105c687
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127581312"
---
# <a name="running-32-bit-applications"></a>Ejecución de aplicaciones de 32 bits

WOW64 es el emulador x86 que permite que las aplicaciones basadas en Windows de 32 bits se ejecuten sin problemas en aplicaciones de 64 Windows. Esto permite que las aplicaciones de Windows de 32 bits (x86) se ejecuten sin problemas en aplicaciones de Windows de 64 bits (x64 Windows), así como para aplicaciones de Windows de 32 bits (x86) y 32 bits (ARM) para que se ejecuten sin problemas en aplicaciones de 64 bits (ARM64) Windows. WOW64 se proporciona con el sistema operativo y no tiene que habilitarse explícitamente. Para obtener más información, vea [Detalles de implementación de WOW64](wow64-implementation-details.md).

El sistema aísla las aplicaciones de 32 bits de las aplicaciones de 64 bits, lo que incluye la prevención de colisiones entre archivos y registros. Se admiten aplicaciones de consola, GUI y servicio. El sistema proporciona interoperabilidad a través del límite 32/64 para escenarios como cortar y pegar y COM. Sin embargo, los procesos de 32 bits no pueden cargar archivos DLL de 64 bits para su ejecución y los procesos de 64 bits no pueden cargar archivos DLL de 32 bits para su ejecución. Esta restricción no se aplica a los archivos DLL cargados como archivos de datos o archivos de recursos de imagen; Para obtener más información, [**vea LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa).

Una aplicación de 32 bits puede detectar si se ejecuta en WOW64 llamando a la función [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) (use [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2) si el destino es Windows 10). La aplicación puede obtener información adicional sobre el procesador mediante la [**función GetNativeSystemInfo.**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

Tenga en cuenta que los Windows de 64 bits no admiten la ejecución de aplicaciones basadas Windows de 16 bits. La razón principal es que los identificadores tienen 32 bits significativos en 64 bits Windows. Por lo tanto, los identificadores no se pueden truncar y pasar a aplicaciones de 16 bits sin pérdida de datos. Los intentos de iniciar aplicaciones de 16 bits producirán el siguiente error: **ERROR \_ BAD EXE \_ \_ FORMAT**.

## <a name="in-this-section"></a>En esta sección

-   [Rendimiento y consumo de memoria en WOW64](performance-and-memory-consumption.md)
-   [Detalles de implementación de WOW64](wow64-implementation-details.md)
-   [Redirector del Registro](registry-redirector.md)
-   [Redirector del sistema de archivos](file-system-redirector.md)
-   [Administración de memoria](memory-management.md)
-   [Afinidad del procesador](processor-affinity.md)
-   [Comunicación entre procesos](interprocess-communication.md)
-   [Instalación de la aplicación](application-installation.md)
-   [Depuración wow64](debugging-wow64.md)

 

 