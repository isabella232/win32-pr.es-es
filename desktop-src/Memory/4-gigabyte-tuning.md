---
description: 'Optimización de 4 gigabytes: BCDEdit y Boot.ini'
ms.assetid: 991eb86f-9e6f-4084-8b6f-f979e42104b5
title: 'Optimización de 4 gigabytes: BCDEdit y Boot.ini'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f997ae09748370d5ec8ec246da80b6440d7aaf45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276720"
---
# <a name="4-gigabyte-tuning-bcdedit-and-bootini"></a>Optimización de 4 gigabytes: BCDEdit y Boot.ini

En las ediciones de 32 bits de Windows, las aplicaciones tienen 4 gigabytes (GB) de espacio de direcciones virtuales disponibles. El espacio de direcciones virtuales se divide de forma que 2 GB esté disponible para la aplicación y los otros 2 GB solo están disponibles para el sistema. La característica de optimización de 4 gigabytes (optimización de RAM 4GT o 4GT), habilitada con el comando *bcdedit/Set increaseuserva* , aumenta el espacio de direcciones virtuales que está disponible para la aplicación hasta 3 GB, y reduce la cantidad disponible para el sistema entre 1 y 2 GB.

En el caso de las aplicaciones que consumen mucha memoria, como los sistemas de administración de bases de datos (DBMS), el uso de un espacio de direcciones virtuales mayor puede proporcionar ventajas de rendimiento y escalabilidad considerables. Sin embargo, la caché de archivos, el bloque paginado y el bloque no paginado son más pequeños, lo que puede afectar negativamente a las aplicaciones con una gran cantidad de redes o e/s. Por lo tanto, es posible que desee probar la aplicación bajo carga y examinar los contadores de rendimiento para determinar si la aplicación se beneficia del espacio de direcciones más grande.

Para habilitar 4GT, use el comando [bcdedit/Set](/windows-hardware/drivers/devtest/bcdedit--set) para establecer la opción de entrada de arranque **increaseuserva** en un valor entre 2048 (2 GB) y 3072 (3 GB).

**Windows Server 2003 y versiones anteriores:** Para habilitar 4GT, agregue el modificador **/3GB** al archivo Boot.ini. El modificador **/3GB** es compatible con los siguientes sistemas:

-   Windows Server 2003
-   Windows XP Professional

El modificador **/3GB** hace que los 3 GB de espacio de direcciones virtuales estén disponibles para las aplicaciones y reduce la cantidad disponible para el sistema a 1 GB. En Windows Server 2003, la cantidad de espacio de direcciones disponible para las aplicaciones se puede ajustar estableciendo el modificador **/USERVA** en Boot.ini en un valor entre 2048 y 3072, lo que aumenta la cantidad de espacio de direcciones disponible para el sistema. Esto puede ayudar a mantener el rendimiento general del sistema cuando la aplicación requiere más de 2 GB, pero inferior a 3 GB de espacio de direcciones.

Para permitir que una aplicación use el espacio de direcciones más grande, establezca la marca [**\_ \_ \_ \_ reconocimiento de direcciones grandes del archivo de imagen**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) en el encabezado de la imagen. El vinculador incluido con Microsoft Visual C++ admite el modificador **/LARGEADDRESSAWARE** para establecer esta marca. La configuración de esta marca y la ejecución de la aplicación en un sistema que no tenga compatibilidad con 4GT no debe afectar a la aplicación.

En las ediciones de 64 bits de Windows, las aplicaciones de 32 bits marcadas con la marca [**\_ \_ \_ \_ reconocimiento de direcciones grandes de archivos de imagen**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) tienen 4 GB de espacio de direcciones disponible.

**Ediciones de Itanium de Windows Server 2003:** Antes de SP1, los procesos de 32 bits solo tienen 2 GB de espacio de direcciones disponible.

Use las directrices siguientes para admitir 4GT en aplicaciones:

-   Las direcciones que están cerca del límite de 2 GB suelen usarse en varios archivos DLL del sistema. Por lo tanto, un proceso de 32 bits no puede asignar más de 2 GB de memoria contigua, aunque esté disponible todo el espacio de direcciones de 4 GB.
-   Para recuperar la cantidad total de espacio virtual de usuario, use la función [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) . Para recuperar la dirección de usuario más alta posible, utilice la función [**GetSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) . Detecte siempre el valor real en tiempo de ejecución y evite usar definiciones de constantes cableadas de forma rígida, como: `#define HIGHEST_USER_ADDRESS 0xC0000000` .
-   Evite comparaciones firmadas con punteros, ya que pueden hacer que las aplicaciones se bloqueen en un sistema habilitado para 4GT. Una condición como la siguiente es falsa para un puntero que está por encima de 2 GB: `if (pointer > 40000000)` .
-   El código que usa el bit más alto de un puntero para un propósito definido por la aplicación producirá un error si se habilita 4GT. Por ejemplo, una palabra de 32 bits podría considerarse como una dirección de modo de usuario si está por debajo de 0x80000000 y un código de error si se trata de una versión anterior. Esto no es cierto con 4GT.

[**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) normalmente devuelve direcciones bajas antes de las direcciones altas. Por lo tanto, es posible que el proceso no use direcciones muy altas a menos que asigne una gran cantidad de memoria o que tenga un espacio de direcciones virtuales fragmentado. Para forzar las asignaciones para que se asignen desde direcciones superiores antes que las más bajas con fines de prueba, especifique **MEM en \_ \_ sentido descendente** al llamar a **VirtualAlloc** o establezca el siguiente valor del registro en 0x100000:

**HKEY \_ \_** \\ **Sistema del** equipo local \\ **CurrentControlSet** \\ **control** \\ **Session Manager** \\ **Administración de memoria** \\ **AllocationPreference**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Límites de memoria para las versiones de Windows](memory-limits-for-windows-releases.md)
</dt> <dt>

[Extensión de dirección física](physical-address-extension.md)
</dt> <dt>

[Referencia técnica de 4GT](/previous-versions/windows/it-pro/windows-server-2003/cc778496(v=ws.10))
</dt> </dl>

 

 
