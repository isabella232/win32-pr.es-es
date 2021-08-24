---
description: Solo 64 bits
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: Solo 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29da3d00b457c7fe95ed7fe614991bc272968ad042b9c0360a14d48b1bf3461
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680265"
---
# <a name="64-bit-only"></a>Solo 64 bits

## <a name="affected-platforms"></a>Plataformas afectadas

**Servidores:** Windows Server 2008 R2  



## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** baja  
**Frecuencia:** alta  






## <a name="description"></a>Descripción

Windows Server 2008 R2 se distribuye solo con una SKU de 64 bits; no hay ninguna SKU de 32 bits disponible para la versión de servidor del sistema operativo. Sin embargo, una SKU de 32 bits sigue estando disponible para el Windows 7.

## <a name="manifestation-of-impact"></a>Demostración de impacto

Esto afectará a tres áreas:

-   Controladores de 32 bits
-   Complementos de 32 bits
-   Ejecutables de 16 bits

## <a name="solution-for-32-bit-drivers"></a>Solución para controladores de 32 bits

Vuelva a compilar controladores de 32 bits como controladores de 64 bits firmados.

## <a name="solution-for-32-bit-plug-ins"></a>Solución para complementos de 32 bits

WoW64, un emulador x86, permite que las aplicaciones basadas en Windows de 32 bits se ejecuten sin problemas en aplicaciones de 64 Windows. WoW64 es ahora una característica opcional que debe instalar si es necesario ejecutar código de 32 bits.

El sistema aísla las aplicaciones de 32 bits de las aplicaciones de 64 bits, lo que incluye la prevención de colisiones entre archivos y registros. Se admiten aplicaciones de consola, GUI y servicio. El sistema proporciona interoperabilidad a través del límite 32/64 para escenarios como cortar y pegar y COM. Sin embargo, los procesos de 32 bits no pueden cargar archivos DLL de 64 bits y los procesos de 64 bits no pueden cargar archivos DLL de 32 bits. Normalmente lo vemos en los complementos de shell escritos para Windows Explorer.

Una aplicación de 32 bits puede detectar si se ejecuta en WOW64 llamando a la función IsWow64Process. La aplicación puede obtener información adicional sobre el procesador mediante la función GetNativeSystemInfo

Tenga en cuenta que los Windows de 64 bits no admiten la ejecución de aplicaciones basadas en Windows de 16 bits. La razón principal es que los identificadores tienen 32 bits significativos en 64 bits Windows. Por lo tanto, los identificadores no se pueden truncar y pasar a aplicaciones de 16 bits sin pérdida de datos. Los intentos de iniciar aplicaciones de 16 bits producirán el siguiente error: ERROR \_ BAD \_ EXE \_ FORMAT.

## <a name="solution-for-16-bit-executables"></a>Solución para ejecutables de 16 bits

El Windows de 64 bits reconoce un número limitado de programas específicos del instalador de 16 bits y sustituye una versión de 32 bits porteada. La lista de sustituciones se almacena en el Registro con la siguiente clave: HKEY LOCAL MACHINE Software Microsoft Windows NT CurrentVersion NtVdm64 Hay compatibilidad integrada con varios motores de instalador, incluidos los instaladores de \_ \_ \\ \\ \\ \\ \\ InstallShield 5.x. Tenga en cuenta que el instalador de Windows de 64 bits puede instalar sin problemas aplicaciones basadas en MSI de 32 bits en aplicaciones de 64 Windows.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Ejecución de aplicaciones de 32 bits](/windows/desktop/WinProg64/running-32-bit-applications)
-   [Rendimiento y consumo de memoria](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [Detalles de implementación de WOW64](/windows/desktop/WinProg64/wow64-implementation-details)
-   [Redirector del Registro](/windows/desktop/WinProg64/registry-redirector)
-   [Redirector del sistema de archivos](/windows/desktop/WinProg64/file-system-redirector)
-   [Administración de memoria](/windows/desktop/WinProg64/memory-management)
-   [Afinidad del procesador](/windows/desktop/WinProg64/processor-affinity)
-   [Comunicación entre procesos](/windows/desktop/WinProg64/interprocess-communication)
-   [Instalación de aplicaciones en sistemas de 64 bits](/windows/desktop/WinProg64/application-installation)
-   [Depuración wow64](/windows/desktop/WinProg64/debugging-wow64)
-   [**Función IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [**GetNativeSystemInfo (Función)**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
