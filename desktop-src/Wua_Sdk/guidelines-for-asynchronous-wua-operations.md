---
description: En este tema se identifican las instrucciones que debe seguir al realizar operaciones asincrónicas del agente de Windows Update (WUA).
ms.assetid: 1fb16904-732d-4341-8267-ab8896fc0f7c
title: Instrucciones para las operaciones de WUA asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a4b2198a235d9a03e3730e5d6dce2cd54c0e1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715700"
---
# <a name="guidelines-for-asynchronous-wua-operations"></a>Instrucciones para las operaciones de WUA asincrónicas

En este tema se identifican las instrucciones que debe seguir al realizar operaciones asincrónicas del agente de Windows Update (WUA).

-   Las operaciones de WUA asincrónicas no garantizan ninguna velocidad de finalización determinada. El tiempo de finalización de una operación de WUA asincrónica puede variar considerablemente en función del hardware del equipo, la versión del sistema operativo y la configuración de red. Como con otras API de Windows que tienen dependencias de red y que no contienen un parámetro de tiempo de espera o una duración de tiempo de espera documentada, se recomienda que considere la posibilidad de implementar sus propios mecanismos de tiempo de espera Si necesita tiempos de respuesta garantizados. Por ejemplo, puede crear un subproceso de trabajo que llame a un método WUA asincrónico y que establezca un evento u otro objeto de sincronización cuando se complete la operación de WUA asincrónica; después, el subproceso principal puede usar la función [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) o [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) , que permite especificar un valor de tiempo de espera.
-   Cuando finaliza una búsqueda, descarga, instalación o desinstalación de actualizaciones, puede usar [**IUpdateSearcher:: EndSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch), [**IUpdateDowloader:: EndDownload**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader), [**IUpdateInstaller:: EndInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-endinstall) y [**IUpdateInstaller:: EndUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-enduninstall) desde cualquier subproceso.
-   Cuando inicia una búsqueda, descarga, instalación o desinstalación de actualizaciones mediante [**IUpdateSearcher:: BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch), [**IUpdateDownloader:: BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload), [**IUpdateInstaller:: BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)y [**IUpdateInstaller:: BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall), asegúrese de mantener suficientes los permisos de acceso al liberar referencias a objetos de la API de WUA.
    -   Asegúrese de que no se hace referencia a los objetos de devolución de llamada que se usan en la operación asincrónica antes de destruirlos. Espere a que el recuento de referencias de un objeto de devolución de llamada vuelva al valor inicial antes de destruirlo.
    -   La referencia al objeto de trabajo que se devuelve desde el método **Begin** correspondiente debe controlarse mediante un objeto que difiere de los objetos de devolución de llamada. Utilice un objeto que difiere de los objetos de devolución de llamada para evitar referencias circulares.
    -   Si intenta controlar la referencia al objeto de trabajo mediante un objeto de devolución de llamada, debe llamar al método [**IDownloadJob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup), [**IInstallationJob::**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)Cleanup o [**ISearchJob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) fuera de la función de devolución de llamada para desconectar el objeto de trabajo del objeto de devolución de llamada. Debe hacerlo antes de liberar la referencia al objeto de trabajo devuelto por el método **Begin** .
-   Asegúrese de que se han completado las operaciones de WUA asincrónicas. Windows Script Host puede finalizar un script cuando se completan todos los comandos que están fuera de la función, incluso si la API de WUA todavía tiene referencias al objeto de devolución de llamada.
    -   Use uno de los métodos de **limpieza** o haga que la función de devolución de llamada establezca una variable global compartida al finalizar.
    -   Nunca llame a [**IDownloadJob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup), [**IInstallationJob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)o [**ISearchJob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) en un objeto de trabajo en su función de devolución de llamada.
    -   Para garantizar la secuencia de limpieza correcta en un script que se ejecuta en Windows Internet Explorer, llame al método **Cleanup** en todos los objetos de trabajo al procesar Window. onbeforeunload.
-   No utilice tipos de datos definidos por el usuario (UDT) para operaciones de WUA asincrónicas. [**IUpdateSearcher:: BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch), [**IUpdateDownloader:: BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload), [**IUpdateInstaller:: BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)o [**IUpdateInstaller:: BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall)no admiten el tipo.

 

 
