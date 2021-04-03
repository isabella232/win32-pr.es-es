---
description: La extensión de dirección física (PAE) es una característica del procesador que permite a los procesadores x86 tener acceso a más de 4 GB de memoria física en versiones compatibles de Windows.
ms.assetid: 1aec2414-cc93-4a86-955d-2433360c9125
title: Extensión de dirección física
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd313c1025eaaf4859436aebef90288c6d3fe49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083473"
---
# <a name="physical-address-extension"></a>Extensión de dirección física

La extensión de dirección física (PAE) es una característica del procesador que permite a los procesadores x86 tener acceso a más de 4 GB de memoria física en versiones compatibles de Windows. Ciertas versiones de 32 bits de Windows Server que se ejecutan en sistemas basados en x86 pueden usar PAE para tener acceso a hasta 64 GB o 128 GB de memoria física, en función del tamaño de la dirección física del procesador. Para obtener más información, consulte [límites de memoria para las versiones de Windows](memory-limits-for-windows-releases.md).

Las arquitecturas de procesador Intel Itanium y x64 pueden tener acceso de forma nativa a más de 4 GB de memoria física y, por tanto, no proporcionan el equivalente de PAE. PAE solo se usa en las versiones de 32 de Windows que se ejecutan en sistemas basados en x86.

Con PAE, el sistema operativo pasa de la traducción de direcciones lineales de dos niveles a la traducción de direcciones de tres niveles. En lugar de dividir una dirección lineal en tres campos independientes para la indexación en tablas de memoria, se divide en cuatro campos independientes: un campo de bits de 2 bits, campos de bits de 2 9 bits y un campo de bits de 12 bits que corresponde al tamaño de página implementado por la arquitectura de Intel (4 KB). El tamaño de las entradas de la tabla de páginas (PTE) y las entradas del directorio de páginas (PDEs) en modo PAE se incrementa de 32 a 64 bits. Los bits adicionales permiten que un sistema operativo PTE o PDE haga referencia a la memoria física por encima de 4 GB.

En Windows de 32 bits que se ejecuta en sistemas basados en x64, PAE también habilita varias características avanzadas del sistema y el procesador, como la [prevención de ejecución de datos](data-execution-prevention.md) (DEP) habilitada para hardware, el acceso a [memoria no uniforme (Numa)](../procthread/numa-support.md)y la capacidad de agregar memoria a un sistema mientras se ejecuta (agregar memoria en caliente).

PAE no cambia la cantidad de espacio de direcciones virtuales disponible para un proceso. Cada proceso que se ejecuta en Windows de 32 bits sigue estando limitado a un espacio de direcciones virtuales de 4 GB.

## <a name="system-support-for-pae"></a>Compatibilidad del sistema con PAE

PAE solo se admite en las siguientes versiones de 32 bits de Windows que se ejecutan en sistemas basados en x86:

-   Windows 7 (solo 32 bits)
-   Windows Server 2008 (solo 32 bits)
-   Windows Vista (solo 32 bits)
-   Windows Server 2003 (solo 32 bits)
-   Windows XP (solo 32 bits)

## <a name="enabling-pae"></a>Habilitar PAE

Windows habilita automáticamente PAE Si DEP está habilitado en un equipo que admita DEP habilitada para el hardware o si el equipo está configurado para dispositivos de memoria de adición en caliente en intervalos de memoria superiores a 4 GB. Si el equipo no es compatible con DEP habilitado para hardware o no está configurado para dispositivos de memoria de adición en caliente en intervalos de memoria superiores a 4 GB, PAE debe estar habilitado explícitamente.

Para habilitar de forma explícita PAE, use el siguiente comando de [**bcdedit/Set**](/windows-hardware/drivers/devtest/bcdedit--set) para establecer la opción de entrada de arranque **PAE** :

 **bcdedit/set \[ {ID} \] PAE ForceEnable**  


Si DEP está habilitado, PAE no se puede deshabilitar. Use los siguientes comandos de [**bcdedit/Set**](/windows-hardware/drivers/devtest/bcdedit--set) para deshabilitar DEP y PAE:

 **bcdedit/set \[ {ID} \] NX AlwaysOff**  
**bcdedit/set \[ {ID} \] PAE ForceDisable**  


**Windows Server 2003 y Windows XP:** Para habilitar PAE, use el modificador **/PAE** en el archivo de [boot.ini](/windows-hardware/drivers/devtest/overview-of-the-boot-ini-file) . Para deshabilitar PAE, use el conmutador **/NOPAE** . Para deshabilitar DEP, use el modificador **/Execute** .

## <a name="comparing-pae-and-other-large-memory-support"></a>Comparar PAE y otra compatibilidad con memoria grande

PAE, [la optimización de 4 gigabytes](4-gigabyte-tuning.md) (4GT) y [las extensiones de ventana de dirección](address-windowing-extensions.md) (AWE) sirven para distintos propósitos y se pueden usar de forma independiente entre sí:

-   PAE permite que el sistema operativo tenga acceso y use más de 4 GB de memoria física.
-   4GT aumenta la parte del espacio de direcciones virtuales que está disponible para un proceso de 2 GB a hasta 3 GB.
-   AWE es un conjunto de API que permite a un proceso asignar memoria física no paginada y, después, asignar de forma dinámica partes de esta memoria en el espacio de direcciones virtuales del proceso.

Cuando no se utilizan 4GT ni AWE, la cantidad de memoria física que puede usar un único proceso de 32 bits está limitada por el tamaño de su espacio de direcciones (2 GB). En este caso, un sistema habilitado para PAE puede seguir usando más de 4 GB de RAM para ejecutar varios procesos al mismo tiempo o almacenar en caché los datos de archivos en la memoria.

4GT se puede usar con o sin PAE. Sin embargo, algunas versiones de Windows limitan la cantidad máxima de memoria física que se puede admitir cuando se usa 4GT. En estos sistemas, el arranque con 4GT habilitado hace que el sistema operativo ignore cualquier memoria que supere el límite.

AWE no requiere PAE o 4GT, pero se suele usar junto con PAE para asignar más de 4 GB de memoria física desde un único proceso de 32 bits.

## <a name="related-topics"></a>Temas relacionados



[**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent)
</dt> <dt>

[Referencia técnica de PAE x86](/previous-versions/windows/it-pro/windows-server-2003/cc728455(v=ws.10))
</dt> </dl>

 

 
