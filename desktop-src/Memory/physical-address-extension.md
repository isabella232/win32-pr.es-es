---
description: La extensión de dirección física (PAE) es una característica de procesador que permite que los procesadores x86 accedan a más de 4 GB de memoria física en versiones compatibles de Windows.
ms.assetid: 1aec2414-cc93-4a86-955d-2433360c9125
title: Extensión de dirección física
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2fd9193a19d228f26a09865086c59b65c0019b3cee42142dfd27188eff30169
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979725"
---
# <a name="physical-address-extension"></a>Extensión de dirección física

La extensión de dirección física (PAE) es una característica de procesador que permite que los procesadores x86 accedan a más de 4 GB de memoria física en versiones compatibles de Windows. Algunas versiones de 32 bits de Windows Server que se ejecutan en sistemas basados en x86 pueden usar PAE para acceder a hasta 64 GB o 128 GB de memoria física, según el tamaño de la dirección física del procesador. Para obtener más información, [vea Límites de memoria Windows versiones](memory-limits-for-windows-releases.md)de .

Las arquitecturas de procesador Intel Itanium y x64 pueden acceder a más de 4 GB de memoria física de forma nativa y, por tanto, no proporcionan el equivalente de PAE. PAE solo se usa en versiones de 32 bits de Windows que se ejecutan en sistemas basados en x86.

Con PAE, el sistema operativo pasa de la traducción de direcciones lineales de dos niveles a la traducción de direcciones de tres niveles. En lugar de dividir una dirección lineal en tres campos independientes para la indexación en tablas de memoria, se divide en cuatro campos independientes: un campo de bits de 2 bits, dos campos de bits de 9 bits y un campo de bits de 12 bits que corresponde al tamaño de página implementado por la arquitectura intel (4 KB). El tamaño de las entradas de tabla de página (PTE) y las entradas de directorio de página (PSE) en modo PAE aumenta de 32 a 64 bits. Los bits adicionales permiten que un PTE o PDE del sistema operativo haga referencia a la memoria física por encima de 4 GB.

En los Windows de 32 bits que se ejecutan en sistemas basados en x64, [](data-execution-prevention.md) PAE también habilita varias características avanzadas del sistema y del procesador, como la prevención de ejecución de datos (DEP) habilitada para hardware, el acceso no uniforme a memoria [(NUMA)](../procthread/numa-support.md)y la capacidad de agregar memoria a un sistema mientras se ejecuta (agregar memoria activa).

PAE no cambia la cantidad de espacio de direcciones virtuales disponible para un proceso. Cada proceso que se ejecuta en un Windows de 32 bits todavía se limita a un espacio de direcciones virtuales de 4 GB.

## <a name="system-support-for-pae"></a>Compatibilidad del sistema con PAE

PAE solo se admite en las siguientes versiones de 32 bits de Windows que se ejecutan en sistemas basados en x86:

-   Windows 7 (solo 32 bits)
-   Windows Server 2008 (solo 32 bits)
-   Windows Vista (solo 32 bits)
-   Windows Server 2003 (solo 32 bits)
-   Windows XP (solo 32 bits)

## <a name="enabling-pae"></a>Habilitación de PAE

Windows habilita automáticamente PAE si DEP está habilitado en un equipo que admite DEP habilitado para hardware, o si el equipo está configurado para dispositivos de memoria de adición activa en intervalos de memoria superiores a 4 GB. Si el equipo no admite DEP habilitado para hardware o no está configurado para dispositivos de memoria de adición activa en intervalos de memoria superiores a 4 GB, pae debe habilitarse explícitamente.

Para habilitar explícitamente PAE, use el siguiente comando [**BCDEdit /set**](/windows-hardware/drivers/devtest/bcdedit--set) para establecer la opción de entrada de arranque **pae:**

 **bcdedit /set \[ {ID} \] pae ForceEnable**  


Si DEP está habilitado, no se puede deshabilitar pae. Use los siguientes [**comandos BCDEdit /set**](/windows-hardware/drivers/devtest/bcdedit--set) para deshabilitar DEP y PAE:

 **bcdedit /set \[ {ID} \] nx AlwaysOff**  
**bcdedit /set \[ {ID} \] pae ForceDisable**  


**Windows Server 2003 y Windows XP:** Para habilitar PAE, use el **modificador /PAE** en el [boot.ini](/windows-hardware/drivers/devtest/overview-of-the-boot-ini-file) archivo. Para deshabilitar PAE, use el **modificador /NOPAE.** Para deshabilitar DEP, use el **modificador /EXECUTE.**

## <a name="comparing-pae-and-other-large-memory-support"></a>Comparación de PAE y otra compatibilidad con memoria grande

Pae, [ajuste de 4 gigabytes](4-gigabyte-tuning.md) (4GT) y extensiones de ventana de direcciones (AWE) sirven para [distintos propósitos](address-windowing-extensions.md) y se pueden usar de forma independiente entre sí:

-   PAE permite que el sistema operativo acceda y use más de 4 GB de memoria física.
-   4GT aumenta la parte del espacio de direcciones virtuales que está disponible para un proceso de 2 GB a hasta 3 GB.
-   AWE es un conjunto de API que permite a un proceso asignar memoria física no superada y, a continuación, asignar dinámicamente partes de esta memoria al espacio de direcciones virtuales del proceso.

Cuando no se usan 4GT ni AWE, la cantidad de memoria física que puede usar un único proceso de 32 bits está limitada por el tamaño de su espacio de direcciones (2 GB). En este caso, un sistema habilitado para PAE puede seguir utilizando más de 4 GB de RAM para ejecutar varios procesos al mismo tiempo o para almacenar en caché los datos de archivo en memoria.

4GT se puede usar con o sin PAE. Sin embargo, algunas versiones de Windows limitar la cantidad máxima de memoria física que se puede admite cuando se usa 4GT. En estos sistemas, el arranque con 4GT habilitado hace que el sistema operativo ignore cualquier memoria que supere el límite.

AWE no requiere PAE ni 4GT, pero a menudo se usa junto con PAE para asignar más de 4 GB de memoria física desde un único proceso de 32 bits.

## <a name="related-topics"></a>Temas relacionados



[**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent)
</dt> <dt>

[Referencia técnica de PAE X86](/previous-versions/windows/it-pro/windows-server-2003/cc728455(v=ws.10))
</dt> </dl>

 

 
