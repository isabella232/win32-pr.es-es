---
description: La parte integral de las pruebas y depuración de las implementaciones del controlador de protocolos es comprender cómo se inician los controladores de protocolo.
ms.assetid: 33c99620-7381-4719-9fc6-4c8284481411
title: Depuración de controladores de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8946b0203c7bc56dd16606ca28e4811bc6328d0cfa87ae55eb2e752657e7da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944495"
---
# <a name="debugging-protocol-handlers"></a>Depuración de controladores de protocolo

La parte integral de las pruebas y depuración de las implementaciones del controlador de protocolos es comprender cómo se inician los controladores de protocolo.

Este tema se organiza de la siguiente manera:

-   [Acerca de los controladores de protocolo de depuración](#about-debugging-protocol-handlers)
-   [Configuración de la depuración](#setting-up-debugging)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="about-debugging-protocol-handlers"></a>Acerca de los controladores de protocolo de depuración

El proceso SearchIndexer (searchindexer.exe) inicia una copia del proceso SearchProtocolHost (SearchProtocolHost.exe) en el contexto del sistema y otra copia en el contexto del usuario. A continuación, los controladores de protocolo se cargan en el proceso SearchProtocolHost según sea necesario. No se descargan hasta que se detiene el servicio de búsqueda. La misma instancia de un controlador de protocolo se reutiliza varias veces mientras se ejecuta el servicio.

Los procesos SearchIndexer y SearchProtocolHost se comunican con frecuencia durante la indexación. Si pausa o detiene el proceso SearchProtocolHost para depurar, SearchIndexer iniciará un nuevo proceso SearchProtocolHost, invalidando la sesión de depuración. Además, si adjunta el depurador directamente al proceso SearchProtocolHost, puede interrumpir la herencia de identificadores de searchindexer.exe a searchprotocolhost.exe y los dos procesos no se podrán comunicar.

Para evitar estos problemas, debe notificar al servicio de búsqueda que está depurando y debe adjuntar el depurador al proceso SearchIndexer con instrucciones para depurar los procesos secundarios, como se describe a continuación.

## <a name="setting-up-debugging"></a>Configuración de la depuración

Siga estos pasos para configurar la depuración para el controlador de protocolos.

1.  Notifique al servicio de búsqueda que está depurando estableciendo el valor debugFilters en 1 en el Registro:

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft
       Windows Search
          Gathering Manager
             DebugFilters = 1
    ```

2.  Adjunte un depurador mediante la clave del Registro Opciones de ejecución de archivos de imagen:

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion
       Image File Execution Options
          SearchIndexer.exe
             Debugger = <path to debugger> <debugger options> 
    ```

    Las opciones de un depurador de ejemplo se describen en la tabla siguiente.

    

    Ejemplo de uso del depurador **ntsd***Debugger = C: \\ debuggersntsd.exe \\ -odGx -c: "sxe ld mydll.dll;g"*   <br/>

3.  Reinicie searchindexer.exe en el depurador mediante compmgmt.msc, services.msc o una ventana de comandos con comandos similares a los siguientes:
    ```
    net stop wsearch
    <copy new DLLs for debugging>
    net start wsearch
            
    ```

    

Para distinguir entre un proceso SearchProtocolHost que se ejecuta en el contexto del sistema y otro que se ejecuta en el contexto de usuario, puede revisar las cadenas de entorno. Con ntsd.exe, por ejemplo, puede usar el comando de extensión **!peb** para mostrar una vista con formato de la información en el bloque de entorno de proceso (PEB).

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener información sobre cómo crear controladores, vea [Registrar extensiones de shell](../shell/reg-shell-exts.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt></dt> Conceptual <dt><a href="-search-3x-wds-phaddins.md">developing Protocol Handlers</a></dt> Understanding <dt><a href="-search-3x-wds-extidx-prot-implementing.md">Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-notifyingofchanges.md">Notifying the Index of Changes</a></dt> Adding Icons and Context <dt><a href="-search-3x-wds-ph-ui-extensions.md">Menus</a></dt> Code <dt><a href="-search-3x-wds-ph-ui-samplecode.md">Sample: Shell Extensions for Protocol Handlers</a></dt> Creating a Search Connector for a Protocol <dt><a href="-search-3x-wds-ph-search-connector.md">Handler</a></dt> Installing and <dt><a href="-search-3x-wds-ph-install-registration.md">Registering Protocol Handlers</a></dt> </dl>

 

 
