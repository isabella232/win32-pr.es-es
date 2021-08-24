---
description: Los programadores que usan Windows Update Agent (WUA) comienzan agregando una referencia a Wuapi.dll a su proyecto actual (en Visual C++, Microsoft Visual Basic o C ) o haciendo referencia a \# Wuapi.h y Wuguid.lib en un proyecto de C o C++.
ms.assetid: ec9cbb0b-b5d4-41f2-8a25-143130d08a3b
title: Windows Actualizar el modelo de objetos del Agente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32b60f9306dfae5910418ddc07353a421e0325c0953fb1f47994ad007ded5ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855455"
---
# <a name="windows-update-agent-object-model"></a>Windows Actualizar el modelo de objetos del Agente

Los programadores que usan Windows Update Agent (WUA) comienzan agregando una referencia a Wuapi.dll a su proyecto actual (en Visual C++, Microsoft Visual Basic o C ) o haciendo referencia a \# Wuapi.h y Wuguid.lib en un proyecto de C o C++. El primer paso para usar la API de WUA es crear una instancia de una de las interfaces mediante la creación de un objeto a partir de la coclase adecuada.

En la ilustración siguiente se describe el modelo de objetos WUA. Para obtener más información, vea la sección["Objetos WUA y tareas](#wua-objects-and-associated-tasks)asociadas". Para obtener una lista completa de todas las interfaces WUA, vea [Interfaces](interfaces.md).

![Modelo de objetos del agente de Windows Update](images/wua-object-model.png)

## <a name="wua-objects-and-associated-tasks"></a>Objetos WUA y tareas asociadas

En la tabla siguiente se enumeran los objetos WUA y las tareas típicas asociadas a los objetos WUA.



| Object                                                                | Descripción                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)                         | Inicie, pause o reanude Actualizaciones automáticas.                                                                                                                                                                                                  |
| [**AutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)         | Recupere o establezca el día y la hora para instalar las actualizaciones. Especifique cómo se notifica a los usuarios de Actualizaciones automáticas evento.                                                                                                                          |
| [**Category**](/windows/desktop/api/Wuapi/nn-wuapi-icategory)                                         | Recupere información sobre la categoría de la actualización, incluidos el nombre, el identificador, la descripción, el propietario y el producto previsto. Recuperar una colección de actualizaciones que pertenecen a esta categoría. Recuperar una colección de las categorías primarias o secundarias. |
| [**CategoryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)                     | Acceda a una colección de objetos Category.                                                                                                                                                                                                    |
| [**DownloadResult**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadresult)                             | Recuperar información sobre el resultado de una descarga.                                                                                                                                                                                        |
| [**InstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult)                     | Recupere información sobre el resultado de una instalación o desinstalación. Determine si es necesario reiniciar el sistema para completar la instalación o desinstalación.                                                                  |
| [**SearchResult**](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)                                 | Recuperar información sobre el resultado de una búsqueda de categorías o actualizaciones. Recupere una colección de categorías encontradas en el equipo de destino mediante la búsqueda. Recupere una colección de actualizaciones encontradas por la búsqueda.                     |
| [**SystemInformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)                       | Recupere información sobre los requisitos de reinicio del sistema y hardware oem en el equipo de destino.                                                                                                                                        |
| [**Actualizar**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)                                             | Recupere la mayoría de la información sobre la actualización, incluidas las actualizaciones agrupadas, los requisitos de origen, la identidad, la descripción, las opciones de desinstalación, la prioridad de descarga, el tamaño y la fecha límite.                                                                |
| [**UpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)                         | Acceda a una colección de objetos Update.                                                                                                                                                                                                      |
| [**UpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)                         | Inicie una descarga asincrónica o sincrónica de los archivos asociados a las actualizaciones.                                                                                                                                            |
| [**UpdateDownloadResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadresult)                 | Recupere información sobre el resultado de la descarga de una actualización.                                                                                                                                                                       |
| [**UpdateException**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)                           | Recupere la descripción y el contexto de una excepción que se produce cuando se produce un error de actualización.                                                                                                                                            |
| [**UpdateExceptionCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)       | Acceda a una colección de objetos UpdateException.                                                                                                                                                                                             |
| [**UpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)                     | Recupere información sobre una actualización que se ha instalado o desinstalado, incluida la aplicación procesada, la fecha y la descripción.                                                                                                    |
| [**UpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) | Acceda a una colección de objetos UpdateHistoryEntry.                                                                                                                                                                                          |
| [**UpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult)         | Recupere información sobre el resultado de la instalación o desinstalación de una actualización.                                                                                                                                                  |
| [**UpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)                           | Inicie una instalación asincrónica o sincrónica o la desinstalación de una actualización. Inicie una secuencia de diálogo interactiva para guiar al usuario a través de los pasos para instalar las actualizaciones.                                                              |
| [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)                             | Busca actualizaciones en el servidor por criterios como el tipo de actualización, el identificador o la categoría.                                                                                                                                            |
| [**UpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)                               | Inicie una sesión para buscar, descargar, instalar o desinstalar las actualizaciones de una aplicación.                                                                                                                                                  |
| [**Webproxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy)                                         | Recupere y establezca la configuración del proxy HTTP.                                                                                                                                                                                                       |



 

 

 



