---
description: 'Ajuste de 4 gigabytes: BCDEdit y Boot.ini'
ms.assetid: 991eb86f-9e6f-4084-8b6f-f979e42104b5
title: 'Ajuste de 4 gigabytes: BCDEdit y Boot.ini'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f997ae09748370d5ec8ec246da80b6440d7aaf45
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159904"
---
# <a name="4-gigabyte-tuning-bcdedit-and-bootini"></a>Ajuste de 4 gigabytes: BCDEdit y Boot.ini

En las ediciones de 32 bits de Windows, las aplicaciones tienen 4 gigabytes (GB) de espacio de direcciones virtuales disponible. El espacio de direcciones virtuales se divide para que 2 GB estén disponibles para la aplicación y los otros 2 GB solo estén disponibles para el sistema. La característica de ajuste de 4 gigabytes (ajuste de RAM de 4GT o 4GT), habilitada con el comando *BCDEdit /set increaseuserva,* aumenta el espacio de direcciones virtuales que está disponible para la aplicación hasta 3 GB y reduce la cantidad disponible para el sistema a entre 1 y 2 GB.

En el caso de las aplicaciones que consumen mucha memoria, como los sistemas de administración de bases de datos (DBMS), el uso de un espacio de direcciones virtual mayor puede proporcionar considerables ventajas de rendimiento y escalabilidad. Sin embargo, la caché de archivos, el grupo paginado y el grupo no paginado son más pequeños, lo que puede afectar negativamente a las aplicaciones con redes o E/S pesadas. Por lo tanto, puede probar la aplicación bajo carga y examinar los contadores de rendimiento para determinar si la aplicación se beneficia del mayor espacio de direcciones.

Para habilitar 4GT, use el comando [BCDEdit /set](/windows-hardware/drivers/devtest/bcdedit--set) para establecer la opción de entrada de arranque **increaseuserva** en un valor entre 2048 (2 GB) y 3072 (3 GB).

**Windows Server 2003 y versiones anteriores:** Para habilitar 4GT, agregue el modificador **/3GB** al Boot.ini archivo. El **modificador /3GB** se admite en los sistemas siguientes:

-   Windows Server 2003
-   Windows XP Professional

El **modificador /3GB** hace que un espacio de direcciones virtuales completo de 3 GB esté disponible para las aplicaciones y reduce la cantidad disponible para el sistema a 1 GB. En Windows Server 2003, la cantidad de espacio de direcciones disponible para las aplicaciones se puede ajustar estableciendo el modificador **/USERVA** en Boot.ini en un valor entre 2048 y 3072, lo que aumenta la cantidad de espacio de direcciones disponible para el sistema. Esto puede ayudar a mantener el rendimiento general del sistema cuando la aplicación requiere más de 2 GB pero menos de 3 GB de espacio de direcciones.

Para permitir que una aplicación use el espacio de direcciones más grande, establezca la marca [**IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) en el encabezado de imagen. El vinculador incluido con Microsoft Visual C++ admite el modificador **/LARGEADDRESSAWARE** para establecer esta marca. Establecer esta marca y, a continuación, ejecutar la aplicación en un sistema que no tenga compatibilidad con 4GT no debería afectar a la aplicación.

En las ediciones de 64 bits de Windows, las aplicaciones de 32 bits marcadas con la marca [**IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) tienen 4 GB de espacio de direcciones disponible.

**Ediciones Itanium de Windows Server 2003:** Antes de SP1, los procesos de 32 bits solo tienen 2 GB de espacio de direcciones disponible.

Use las siguientes directrices para admitir 4GT en aplicaciones:

-   Las direcciones cerca del límite de 2 GB suelen usarse en varios archivos DLL del sistema. Por lo tanto, un proceso de 32 bits no puede asignar más de 2 GB de memoria contigua, aunque todo el espacio de direcciones de 4 GB esté disponible.
-   Para recuperar la cantidad total de espacio virtual del usuario, use la [**función GlobalMemoryStatusEx.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) Para recuperar la dirección de usuario más alta posible, use [**la función GetSystemInfo.**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) Detecte siempre el valor real en tiempo de ejecución y evite el uso de definiciones de constantes cableadas de forma permanente como: `#define HIGHEST_USER_ADDRESS 0xC0000000` .
-   Evite las comparaciones firmadas con punteros, ya que pueden hacer que las aplicaciones se bloquean en un sistema habilitado para 4GT. Una condición como la siguiente es false para un puntero que está por encima de 2 GB: `if (pointer > 40000000)` .
-   Se producirá un error en el código que usa el bit más alto de un puntero para un propósito definido por la aplicación cuando 4GT está habilitado. Por ejemplo, una palabra de 32 bits podría considerarse una dirección en modo de usuario si está por debajo de 0x80000000 y un código de error si es anterior. Esto no es cierto con 4GT.

[**VirtualAlloc normalmente**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) devuelve direcciones bajas antes que las direcciones altas. Por lo tanto, es posible que el proceso no use direcciones muy altas a menos que asigne mucha memoria o tenga un espacio de direcciones virtual fragmentado. Para forzar que las asignaciones se asignen desde direcciones superiores antes de las direcciones inferiores con fines de prueba, especifique **\_ TOP \_ DOWN** de MEM al llamar a **VirtualAlloc** o establezca el siguiente valor del Registro en 0x100000:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager Memory** \\ **Management** \\ **AllocationPreference**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Límites de memoria para Windows versiones](memory-limits-for-windows-releases.md)
</dt> <dt>

[Extensión de dirección física](physical-address-extension.md)
</dt> <dt>

[Referencia técnica de 4GT](/previous-versions/windows/it-pro/windows-server-2003/cc778496(v=ws.10))
</dt> </dl>

 

 
