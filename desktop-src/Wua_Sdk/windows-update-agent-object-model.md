---
description: Los programadores que usan Windows Update Agent (WUA) comienzan agregando una referencia a Wuapi.dll a su proyecto actual (en Visual C++, Microsoft Visual Basic o C \# ) o haciendo referencia a Wuapi. h y Wuguid. lib en un proyecto de C o C++.
ms.assetid: ec9cbb0b-b5d4-41f2-8a25-143130d08a3b
title: Modelo de objetos del agente Windows Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5060a76c850ea9ad97e9132f661d4b64f4f4fd03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556081"
---
# <a name="windows-update-agent-object-model"></a>Modelo de objetos del agente Windows Update

Los programadores que usan Windows Update Agent (WUA) comienzan agregando una referencia a Wuapi.dll a su proyecto actual (en Visual C++, Microsoft Visual Basic o C \# ) o haciendo referencia a Wuapi. h y Wuguid. lib en un proyecto de C o C++. El primer paso en el uso de la API de WUA es crear una instancia de una de las interfaces mediante la creación de un objeto a partir de la coclase adecuada.

En la siguiente ilustración se describe el modelo de objetos de WUA. Para obtener más información, vea la sección "[objetos de WUA y tareas asociadas](#wua-objects-and-associated-tasks)". Para obtener una lista completa de todas las interfaces de WUA, vea [interfaces](interfaces.md).

![modelo de objetos del agente de Windows Update](images/wua-object-model.png)

## <a name="wua-objects-and-associated-tasks"></a>Objetos de WUA y tareas asociadas

En la tabla siguiente se enumeran los objetos de WUA y las tareas típicas que están asociadas a los objetos de WUA.



| Object                                                                | Descripción                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)                         | Iniciar, pausar o reanudar Actualizaciones automáticas.                                                                                                                                                                                                  |
| [**AutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)         | Recupera o establece el día y la hora para instalar las actualizaciones. Especifique cómo se notifica a los usuarios de un evento Actualizaciones automáticas.                                                                                                                          |
| [**Category**](/windows/desktop/api/Wuapi/nn-wuapi-icategory)                                         | Recupera información sobre la categoría de la actualización, incluido el nombre, el identificador, la descripción, el propietario y el producto previsto. Recupera una colección de actualizaciones que pertenecen a esta categoría. Recupera una colección de categorías primarias o secundarias. |
| [**CategoryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)                     | Acceder a una colección de objetos de categoría.                                                                                                                                                                                                    |
| [**DownloadResult**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadresult)                             | Recupera información sobre el resultado de una descarga.                                                                                                                                                                                        |
| [**InstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult)                     | Recupera información sobre el resultado de una instalación o desinstalación. Determine si es necesario reiniciar el sistema para completar la instalación o desinstalación.                                                                  |
| [**SearchResult**](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)                                 | Recupera información sobre el resultado de una búsqueda de categorías o actualizaciones. Recupera una colección de categorías que se encuentra en el equipo de destino mediante la búsqueda. Recupera una colección de actualizaciones encontradas en la búsqueda.                     |
| [**SystemInformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)                       | Recupere información acerca de los requisitos de hardware y reinicio del sistema OEM en el equipo de destino.                                                                                                                                        |
| [**Update**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)                                             | Recupere la mayoría de la información sobre la actualización, incluidas las actualizaciones agrupadas, los requisitos de origen, la identidad, la descripción, las opciones de desinstalación, la prioridad de descarga, el tamaño y la fecha límite.                                                                |
| [**UpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)                         | Obtener acceso a una colección de objetos Update.                                                                                                                                                                                                      |
| [**UpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)                         | Inicia una descarga asincrónica o sincrónica de los archivos que están asociados a las actualizaciones.                                                                                                                                            |
| [**UpdateDownloadResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadresult)                 | Recupera información sobre el resultado de la descarga de una actualización.                                                                                                                                                                       |
| [**UpdateException**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)                           | Recupera la descripción y el contexto de una excepción que se produce cuando se produce un error de actualización.                                                                                                                                            |
| [**UpdateExceptionCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)       | Acceder a una colección de objetos UpdateException.                                                                                                                                                                                             |
| [**UpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)                     | Recuperar información acerca de una actualización instalada o desinstalada, incluida la aplicación procesada, la fecha y la descripción.                                                                                                    |
| [**UpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) | Acceder a una colección de objetos UpdateHistoryEntry.                                                                                                                                                                                          |
| [**UpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult)         | Recupera información sobre el resultado de la instalación o desinstalación de una actualización.                                                                                                                                                  |
| [**UpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)                           | Inicia una instalación asincrónica o sincrónica o la desinstalación de una actualización. Iniciar una secuencia de diálogo interactiva para guiar al usuario a través de los pasos necesarios para instalar actualizaciones.                                                              |
| [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)                             | Busca actualizaciones en el servidor por criterios como el tipo de actualización, el identificador o la categoría.                                                                                                                                            |
| [**UpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)                               | Iniciar una sesión para buscar, descargar, instalar o desinstalar las actualizaciones de una aplicación.                                                                                                                                                  |
| [**WebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy)                                         | Recupere y establezca la configuración del proxy HTTP.                                                                                                                                                                                                       |



 

 

 



