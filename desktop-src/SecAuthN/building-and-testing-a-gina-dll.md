---
description: Todas las funciones, prototipos, estructuras y constantes se definen en el archivo de encabezado Winwlx. h.
ms.assetid: 13b5bc92-583d-4031-94f9-f84dbfbf7ee7
title: Compilar y probar un archivo DLL de GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e6e4a00f15e6ced4827bbc3efeb3c459f5d6a8
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362008"
---
# <a name="building-and-testing-a-gina-dll"></a>Compilar y probar un archivo DLL de GINA

Todas las funciones, prototipos, estructuras y constantes se definen en el archivo de encabezado Winwlx. h.

> [!Note]  
> Los archivos dll de GINA se omiten en Windows Vista.

 

Para probar un archivo dll de [*Gina*](/windows/desktop/SecGloss/g-gly) , use el Winlogon.exe de una versión comprobada del sistema operativo, que está disponible en el kit de desarrollo de controladores de Microsoft Windows (DDK). La versión comprobada de [*Winlogon*](/windows/desktop/SecGloss/w-gly) admite la depuración de Gina de la siguiente manera:

-   Puede usar la siguiente sintaxis para crear una sección en Win.ini para especificar las opciones de depuración de Winlogon.

    ``` syntax
    [WinlogonDebug]
    LogFile=C:\Winlogon.log
    DebugFlags=Flag1 [, Flag2 ...]
    ```

    Si se especifica, **logfile** debe contener el nombre completo del archivo que se utilizará para registrar la información de depuración. Si el archivo no existe, se creará.

    Las opciones **DebugFlags** especifican los tipos de información de depuración que se van a escribir en el archivo de registro o el depurador. **DebugFlags** puede contener una o varias de las marcas siguientes.

    

    | Marca de depuración | Descripción                                                                                                                                                                |
    |----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | CoolSwitch     | La combinación de teclas CTRL + ALT + MAYÚS + TAB producirá una interrupción de depuración en Winlogon.                                                                                               |
    | Error          | Errores de impresión.                                                                                                                                                              |
    | Init           | Imprimir mensajes de inicialización y progreso.                                                                                                                                |
    | Notificar         | Mensajes de paquete de notificación de impresión.                                                                                                                                       |
    | SAS            | Imprime información sobre las notificaciones de [*secuencia de atención segura*](/windows/desktop/SecGloss/s-gly) (SAS). |
    | Estado          | Imprime mensajes cuando Winlogon cambia el estado.                                                                                                                                |
    | Tiempo de espera        | Imprime los mensajes cuando se establece un límite de tiempo o se alcanza un límite de tiempo.                                                                                                        |
    | Seguimiento          | Imprime información de seguimiento detallada.                                                                                                                                           |
    | Warn (Advertencia)           | Imprimir advertencias.                                                                                                                                                            |

    

     

-   Para iniciar la versión comprobada de Winlogon en un depurador, agregue la entrada siguiente al registro:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows NT
                CurrentVersion
                   Image File Execution Options
                      winlogon.exe
                         Debugger = ntsd -d<dl>
    <dt>

                     Data type
</dt>
    <dd>                     REG_SZ</dd>
    </dl>
    ```

> [!NOTE]
> Debe usar el depurador simbólico de Windows (NTSD) para depurar Winlogon.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cargar y ejecutar un archivo DLL de GINA](loading-and-running-a-gina-dll.md)
</dt> <dt>

[Funciones de exportación de GINA](authentication-functions.md)
</dt> <dt>

[Estructuras GINA](authentication-structures.md)
</dt> <dt>

[Terminal Services funciones GINA](terminal-services-gina-functions.md)
</dt> </dl>

 

 
