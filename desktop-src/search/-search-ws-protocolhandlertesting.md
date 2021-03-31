---
description: La parte entera de la prueba y depuración de las implementaciones del controlador de protocolo es entender cómo se inician los controladores de protocolo.
ms.assetid: 33c99620-7381-4719-9fc6-4c8284481411
title: Controladores de protocolo de depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321d59c0c7915f9bbf84a80091408ba88a9a75ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153945"
---
# <a name="debugging-protocol-handlers"></a>Controladores de protocolo de depuración

La parte entera de la prueba y depuración de las implementaciones del controlador de protocolo es entender cómo se inician los controladores de protocolo.

Este tema se organiza de la siguiente manera:

-   [Acerca de los controladores de protocolo de depuración](#about-debugging-protocol-handlers)
-   [Configuración de la depuración](#setting-up-debugging)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="about-debugging-protocol-handlers"></a>Acerca de los controladores de protocolo de depuración

El proceso SearchIndexer (searchindexer.exe) inicia una copia del proceso SearchProtocolHost (SearchProtocolHost.exe) en el contexto del sistema y otra copia en el contexto del usuario. A continuación, los controladores de protocolo se cargan en el proceso SearchProtocolHost según sea necesario. No se descargan hasta que se detiene el servicio de búsqueda. Se reutiliza la misma instancia de un controlador de protocolo cualquier número de veces que se esté ejecutando el servicio.

Los procesos SearchIndexer y SearchProtocolHost se comunican con frecuencia durante la indexación. Si pausa o detiene el proceso SearchProtocolHost para depurar, el SearchIndexer iniciará un nuevo proceso SearchProtocolHost, invalidando la sesión de depuración. Además, si asocia el depurador directamente al proceso SearchProtocolHost, puede interrumpir la herencia de identificador de searchindexer.exe a searchprotocolhost.exe y los dos procesos no podrán comunicarse.

Para evitar estos problemas, debe notificar al servicio de búsqueda que está depurando y debe adjuntar el depurador al proceso SearchIndexer con instrucciones para depurar procesos secundarios, tal y como se describe a continuación.

## <a name="setting-up-debugging"></a>Configuración de la depuración

Siga estos pasos para configurar la depuración para el controlador de protocolo.

1.  Notifique al servicio de búsqueda que está depurando estableciendo el valor de DebugFilters en 1 en el registro:

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft
       Windows Search
          Gathering Manager
             DebugFilters = 1
    ```

2.  Adjunte un depurador mediante la clave del registro opciones de ejecución del archivo de imagen:

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion
       Image File Execution Options
          SearchIndexer.exe
             Debugger = <path to debugger> <debugger options> 
    ```

    En la tabla siguiente se describen las opciones de un depurador de ejemplo.

    

    **Ejemplo de uso del** depurador NTSD Debugger *= C: \\ debuggers \\ntsd.exe-odGx-C: "sxe LD mydll.dll; g"*   <br/>

3.  Reinicie searchindexer.exe en el depurador con compmgmt. msc, Services. msc o una ventana de comandos con comandos similares a los siguientes:
    ```
    net stop wsearch
    <copy new DLLs for debugging>
    net start wsearch
            
    ```

    

Para distinguir entre un proceso SearchProtocolHost que se ejecuta en el contexto del sistema y otro que se ejecuta en el contexto de usuario, puede revisar las cadenas de entorno. Con ntsd.exe, por ejemplo, puede usar el comando de extensión **! PEB** para mostrar una vista con formato de la información en el bloque de entorno de proceso (PEB).

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener información sobre cómo crear controladores, consulte [registrar extensiones de Shell](../shell/reg-shell-exts.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>**Conceptos**</dt> básicos del <dt><a href="-search-3x-wds-phaddins.md">desarrollo de controladores</a></dt> <dt><a href="-search-3x-wds-extidx-prot-implementing.md">Descripción</a></dt> <dt><a href="-search-3x-wds-notifyingofchanges.md">de los controladores de protocolo notificación del índice de cambios</a></dt> <dt><a href="-search-3x-wds-ph-ui-extensions.md">Agregar iconos y menús contextuales</a></dt> <dt><a href="-search-3x-wds-ph-ui-samplecode.md">ejemplo de código: extensiones de Shell para controladores de protocolo</a></dt> <dt><a href="-search-3x-wds-ph-search-connector.md">crear un conector de búsqueda para un controlador de protocolo</a></dt> <dt><a href="-search-3x-wds-ph-install-registration.md">instalar y registrar controladores</a></dt> de protocolo </dl>

 

 
