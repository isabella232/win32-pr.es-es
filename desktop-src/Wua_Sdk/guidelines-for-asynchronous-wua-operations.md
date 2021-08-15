---
description: En este tema se identifican las instrucciones siguientes al realizar operaciones asincrónicas Windows Update Agent (WUA).
ms.assetid: 1fb16904-732d-4341-8267-ab8896fc0f7c
title: Directrices para las operaciones asincrónicas de WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24801c7639e75f34f1517ee626ff7acb7c1d13f85a6ebf57e7d824f7f0d3191d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049493"
---
# <a name="guidelines-for-asynchronous-wua-operations"></a>Directrices para las operaciones asincrónicas de WUA

En este tema se identifican las instrucciones siguientes al realizar operaciones asincrónicas Windows Update Agent (WUA).

-   Las operaciones de WUA asincrónicas no garantizan ninguna velocidad de finalización determinada. El tiempo de finalización de una operación WUA asincrónica puede variar ampliamente en función del hardware del equipo, la versión del sistema operativo y la configuración de red. Al igual que con otras API de Windows que tienen dependencias de red y que no contienen un parámetro de tiempo de espera o una duración de tiempo de espera documentada, se recomienda considerar la posibilidad de implementar sus propios mecanismos de tiempo de espera si necesita tiempos de respuesta garantizados. Por ejemplo, puede crear un subproceso de trabajo que llame a un método WUA asincrónico y que establece un evento u otro objeto de sincronización cuando se complete la operación de WUA asincrónica; A continuación, el subproceso principal puede usar las funciones [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) o [**WaitForMultipleObjects,**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) lo que permite especificar un valor de tiempo de espera.
-   Al finalizar una búsqueda, descarga, instalación o desinstalación de actualizaciones, puede usar [**IUpdateSearcher::EndSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch), [**IUpdateDowloader::EndDownload**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader), [**IUpdateInstaller::EndInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-endinstall) [**e IUpdateInstaller::EndUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-enduninstall) desde cualquier subproceso.
-   Al iniciar una búsqueda, descarga, instalación o desinstalación de actualizaciones mediante [**IUpdateSearcher::BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch), [**IUpdateDownloader::BeginDownloader::BeginDownload,**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) [**IUpdateInstaller::BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) [**e IUpdateInstaller::BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall), asegúrese de mantener las permisiones de acceso suficientes al liberar referencias a objetos de API de WUA.
    -   Asegúrese de que los objetos de devolución de llamada que se usan en la operación asincrónica no estén referenciados antes de destruirlos. Espere a que el recuento de referencias de un objeto de devolución de llamada vuelva al valor inicial antes de destruirlo.
    -   La referencia al objeto de trabajo que se devuelve desde el método **Begin** correspondiente debe controlarse mediante un objeto que difiere de los objetos de devolución de llamada. Use un objeto que difiese de los objetos de devolución de llamada para evitar referencias circulares.
    -   Si intenta controlar la referencia al objeto de trabajo mediante un objeto de devolución de llamada, debe llamar al método [**IDownloadJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup), [**IInstallationJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)o [**ISearchJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) fuera de la función de devolución de llamada para desconectar el objeto de trabajo del objeto de devolución de llamada. Debe hacerlo antes de liberar la referencia al objeto de trabajo devuelto por el **método Begin.**
-   Asegúrese de que las operaciones de WUA asincrónicas se han completado. Windows El host de script puede finalizar un script cuando se completan todos los comandos fuera de cualquier función, incluso si la API de WUA todavía tiene referencias al objeto de devolución de llamada.
    -   Use uno de los métodos **CleanUp** o que la función de devolución de llamada establezca una variable global compartida tras la finalización.
    -   Nunca llame a [**IDownloadJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup), [**IInstallationJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)o [**ISearchJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) en un objeto de trabajo en su función de devolución de llamada.
    -   Para garantizar la secuencia de limpieza correcta en un script que se ejecuta en Windows Internet Explorer, llame al método **CleanUp** en todos los objetos de trabajo al procesar window.onbeforeunload.
-   No use tipos de datos definidos por el usuario (UDT) para operaciones WUA asincrónicas. El tipo no es compatible con [**IUpdateSearcher::BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch), [**IUpdateDownloader::BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload), [**IUpdateInstaller::BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)o [**IUpdateInstaller::BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall).

 

 
