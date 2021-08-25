---
description: Todas las funciones, prototipos, estructuras y constantes se definen en el archivo de encabezado Winwlx.h.
ms.assetid: 13b5bc92-583d-4031-94f9-f84dbfbf7ee7
title: Compilar y probar un archivo DLL de GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31df8597ca9ad78b8c94efb5610e3c899f7834cb14c9112b15a410c72705a0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883535"
---
# <a name="building-and-testing-a-gina-dll"></a>Compilar y probar un archivo DLL de GINA

Todas las funciones, prototipos, estructuras y constantes se definen en el archivo de encabezado Winwlx.h.

> [!Note]  
> Los archivos DLL de GINA se omiten Windows Vista.

 

Para probar un archivo DLL [*de GINA,*](/windows/desktop/SecGloss/g-gly) use el Winlogon.exe de una versión comprobada del sistema operativo, que está disponible con el Kit de desarrollo de controladores (DDK) de Microsoft Windows. La versión activada de [*Winlogon admite*](/windows/desktop/SecGloss/w-gly) la depuración de EBAA como se muestra a continuación:

-   Puede usar la sintaxis siguiente para crear una sección en Win.ini especificar las opciones de depuración de Winlogon.

    ``` syntax
    [WinlogonDebug]
    LogFile=C:\Winlogon.log
    DebugFlags=Flag1 [, Flag2 ...]
    ```

    Si se especifica, **LogFile** debe contener el nombre completo del archivo que se usará para registrar la información de depuración. Si el archivo no existe, se creará.

    Las **opciones DebugFlags** especifican qué tipos de información de depuración se escriben en el archivo de registro o el depurador. **DebugFlags** puede contener una o varias de las marcas siguientes.

    

    | Marca de depuración | Descripción                                                                                                                                                                |
    |----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | CoolSwitch     | La combinación de teclas CTRL+ALT+MAYÚS+TAB provocará una interrupción de depuración en Winlogon.                                                                                               |
    | Error          | Errores de impresión.                                                                                                                                                              |
    | Init           | Imprima mensajes de inicialización y progreso.                                                                                                                                |
    | Notificar         | Imprimir mensajes del paquete de notificación.                                                                                                                                       |
    | SAS            | Imprima información sobre [*las notificaciones de secuencia de*](/windows/desktop/SecGloss/s-gly) atención segura (SAS). |
    | Estado          | Imprima mensajes cuando Winlogon cambie de estado.                                                                                                                                |
    | Tiempo de espera        | Imprima mensajes cuando se establezca un límite de tiempo o se alcance un límite de tiempo.                                                                                                        |
    | Seguimiento          | Imprima información de seguimiento detallada.                                                                                                                                           |
    | Warn (Advertencia)           | Imprima advertencias.                                                                                                                                                            |

    

     

-   Para iniciar la versión activada de Winlogon en un depurador, agregue la siguiente entrada al Registro:

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
> Debe usar el depurador Windows simbólico (NTSD) para depurar Winlogon.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Carga y ejecución de un archivo DLL de GINA](loading-and-running-a-gina-dll.md)
</dt> <dt>

[Funciones de exportación de GINA](authentication-functions.md)
</dt> <dt>

[Estructuras de GINA](authentication-structures.md)
</dt> <dt>

[Funciones GINA de Terminal Services](terminal-services-gina-functions.md)
</dt> </dl>

 

 
