---
description: .
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: Solo 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d3178a15ec0a138a73789233dd2d787964a96b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279302"
---
# <a name="64-bit-only"></a>Solo 64 bits

## <a name="affected-platforms"></a>Plataformas afectadas

**Servidores** : Windows Server 2008 R2  



## <a name="feature-impact"></a>Impacto en las características

 **Gravedad** baja  
**Frecuencia** : alta  






## <a name="description"></a>Descripción

Windows Server 2008 R2 se incluye solo con una SKU de 64 bits; no hay disponible ninguna SKU de 32 bits para la versión de servidor del sistema operativo. Sin embargo, una SKU de 32 bits sigue estando disponible para el cliente de Windows 7.

## <a name="manifestation-of-impact"></a>Manifiesto de impacto

Esto afectará a tres áreas:

-   Controladores de 32 bits
-   Complementos de 32 bits
-   ejecutables de 16 bits

## <a name="solution-for-32-bit-drivers"></a>Solución para los controladores de 32 bits

Vuelva a compilar los controladores de 32 bits como controladores de 64 bits firmados.

## <a name="solution-for-32-bit-plug-ins"></a>Solución para complementos de 32 bits

WoW64, un emulador de x86, permite que las aplicaciones basadas en Windows de 32 bits se ejecuten sin problemas en Windows de 64 bits. WoW64 es ahora una característica opcional que se debe instalar si es necesario ejecutar código de 32 bits.

El sistema aísla las aplicaciones de 32 bits de las aplicaciones de 64 bits, lo que incluye evitar colisiones de archivos y del registro. Se admiten las aplicaciones de consola, GUI y servicio. El sistema proporciona interoperabilidad en el límite de 32/64 para escenarios como cortar y pegar y COM. Sin embargo, los procesos de 32 bits no pueden cargar archivos dll de 64 bits y los procesos de 64 bits no pueden cargar archivos dll de 32 bits. Normalmente vemos esto en los complementos de Shell escritos para el explorador de Windows.

Una aplicación de 32 bits puede detectar si se ejecuta bajo WOW64 mediante una llamada a la función IsWow64Process. La aplicación puede obtener información adicional sobre el procesador mediante la función GetNativeSystemInfo

Tenga en cuenta que Windows de 64 bits no admite la ejecución de aplicaciones basadas en Windows de 16 bits. La razón principal es que los identificadores tienen 32 bits significativos en Windows de 64 bits. Por lo tanto, los identificadores no se pueden truncar y pasar a las aplicaciones de 16 bits sin pérdida de datos. Los intentos de iniciar las aplicaciones de 16 bits producen el siguiente error: ERROR de \_ \_ formato exe incorrecto \_ .

## <a name="solution-for-16-bit-executables"></a>Solución para archivos ejecutables de 16 bits

Windows de 64 bits reconoce un número limitado de programas de instalador de 16 bits específicos y sustituye una versión de 32 bits por puerto. La lista de sustituciones se almacena en el registro en la siguiente clave: HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64 hay compatibilidad integrada para varios motores de instalación, incluidos los instaladores de InstallShield 5. x. Tenga en cuenta que la Windows Installer de 64 bits puede instalar sin problemas aplicaciones basadas en MSI de 32 bits en Windows de 64 bits.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Ejecutar aplicaciones de 32 bits](/windows/desktop/WinProg64/running-32-bit-applications)
-   [Rendimiento y consumo de memoria](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [Detalles de la implementación de WOW64](/windows/desktop/WinProg64/wow64-implementation-details)
-   [Redirector del registro](/windows/desktop/WinProg64/registry-redirector)
-   [Redirector del sistema de archivos](/windows/desktop/WinProg64/file-system-redirector)
-   [Administración de memoria](/windows/desktop/WinProg64/memory-management)
-   [Afinidad del procesador](/windows/desktop/WinProg64/processor-affinity)
-   [Comunicación entre procesos](/windows/desktop/WinProg64/interprocess-communication)
-   [Instalación de aplicaciones en sistemas de 64 bits](/windows/desktop/WinProg64/application-installation)
-   [Depurar WOW64](/windows/desktop/WinProg64/debugging-wow64)
-   [**IsWow64Process función)**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [**GetNativeSystemInfo función)**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
