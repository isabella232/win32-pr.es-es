---
description: La interfaz IUpdate define las siguientes propiedades.
ms.assetid: d87544f1-a107-440f-8ce0-77d9f2d90578
title: Propiedades de IUpdate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df3f67f95936ea54dd09131e605da9e439caa43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542283"
---
# <a name="iupdate-properties"></a>Propiedades de IUpdate

La interfaz [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) define las siguientes propiedades.



| Propiedad                                                                           | Descripción                                                                                                                                                                         |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutoSelectOnWebSites**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_autoselectonwebsites)                       | Obtiene un valor booleano que indica si la actualización se marca para que se seleccione automáticamente mediante Windows Update.                                                                   |
| [**BundledUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_bundledupdates)                                   | Obtiene una interfaz que contiene información sobre la lista ordenada de las actualizaciones agrupadas de la actualización.                                                                           |
| [**CanRequireSource**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_canrequiresource)                               | Obtiene un valor booleano que indica si se requiere el medio de origen de la actualización para la instalación o desinstalación.                                                          |
| [**Categorías**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_categories)                                           | Obtiene una interfaz que contiene una colección de categorías a las que pertenece la actualización.                                                                                             |
| [**Fecha límite**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deadline)                                               | Obtiene la fecha en la que se debe instalar la actualización.                                                                                                                                |
| [**DeltaCompressedContentAvailable**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deltacompressedcontentavailable) | Obtiene un valor booleano que indica si el contenido con compresión Delta está disponible en un servidor para la actualización.                                                                       |
| [**DeltaCompressedContentPreferred**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deltacompressedcontentpreferred) | Obtiene un valor booleano que indica si se prefiere el contenido con compresión Delta durante la descarga e instalación o desinstalación de la actualización si el contenido con compresión Delta está disponible. |
| [**DeploymentAction**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deploymentaction)                               | Obtiene la acción para la que se implementa la actualización.                                                                                                                                   |
| [**Descripción**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_description)                                         | Obtiene la descripción localizada de la actualización.                                                                                                                                       |
| [**DownloadContents**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_downloadcontents)                               | Obtiene información del archivo sobre el contenido de descarga de la actualización.                                                                                                                    |
| [**DownloadPriority**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_downloadpriority)                               | Obtiene la prioridad de descarga sugerida de la actualización.                                                                                                                                 |
| [**EulaAccepted**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_eulaaccepted)                                       | Obtiene un valor booleano que indica si los términos de licencia del software de Microsoft asociados a la actualización se aceptan para el equipo.                                 |
| [**EulaText**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_eulatext)                                               | Obtiene el texto localizado completo de los términos de licencia del software de Microsoft asociados a la actualización.                                                                           |
| [**HandlerID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_handlerid)                                             | Obtiene el controlador de instalación de la actualización.                                                                                                                                             |
| [**Identidad**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_identity)                                               | Obtiene una interfaz que contiene el identificador único de la actualización.                                                                                                                |
| [**Impresión**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_image)                                                     | Obtiene una interfaz que contiene información sobre una imagen que está asociada a la actualización.                                                                                      |
| [**InstallationBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_installationbehavior)                       | Obtiene una interfaz que contiene las opciones de instalación de la actualización.                                                                                                             |
| [**IsBeta**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isbeta)                                                   | Obtiene un valor booleano que indica si la actualización es una versión beta.                                                                                                           |
| [**IsDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isdownloaded)                                       | Obtiene un valor booleano que indica si todo el contenido de la actualización se almacena en la memoria caché del equipo.                                                                                       |
| [**IsHidden**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)                                               | Obtiene un valor booleano que indica si un usuario oculta una actualización.                                                                                                          |
| [**IsInstalled**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isinstalled)                                         | Obtiene un valor booleano que indica si la actualización está instalada en un equipo cuando se realiza la búsqueda.                                                                     |
| [**IsMandatory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ismandatory)                                         | Obtiene un valor booleano que indica si la instalación de la actualización es obligatoria.                                                                                            |
| [**IsUninstallable**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isuninstallable)                                 | Obtiene un valor booleano que indica si un usuario puede desinstalar la actualización de un equipo.                                                                                        |
| [**KBArticleIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_kbarticleids)                                       | Obtiene una colección de identificadores de artículos de Microsoft Knowledge base que están asociados a la actualización.                                                                                      |
| [**Lenguajes**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_languages)                                              | Obtiene una interfaz que contiene los idiomas admitidos por la actualización.                                                                                                     |
| [**LastDeploymentChangeTime**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_lastdeploymentchangetime)               | Obtiene la fecha y hora de la última publicación de la actualización, en formato de hora universal coordinada (UTC), en el servidor que implementa la actualización.                                               |
| [**MaxDownloadSize**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_maxdownloadsize)                                 | Obtiene el tamaño máximo de la descarga de la actualización.                                                                                                                                       |
| [**MinDownloadSize**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_mindownloadsize)                                 | Obtiene el tamaño mínimo de descarga de la actualización.                                                                                                                                       |
| [**MoreInfoUrls**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_moreinfourls)                                       | Obtiene una colección de cadenas específicas del lenguaje que especifican los hipervínculos para obtener más información acerca de la actualización.                                                                    |
| [**MsrcSeverity**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_msrcseverity)                                       | Obtiene el nivel de gravedad de la actualización del centro de respuesta de seguridad de Microsoft.                                                                                                          |
| [**RecommendedCPUSpeed**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedcpuspeed)                         | Obtiene la velocidad de CPU recomendada utilizada para instalar la actualización, en megahercios (MHz).                                                                                                      |
| [**RecommendedHardDiskSpace**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedharddiskspace)               | Obtiene el espacio disponible recomendado que debe estar disponible en el disco duro antes de instalar la actualización. El espacio disponible se especifica en megabytes (MB).                             |
| [**RecommendedMemory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedmemory)                             | Obtiene el tamaño de memoria física recomendado que debe estar disponible en el equipo antes de instalar la actualización. El tamaño de la memoria física se especifica en megabytes (MB).         |
| [**Leame**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_releasenotes)                                       | Obtiene las notas de la versión localizadas de la actualización.                                                                                                                                    |
| [**SecurityBulletinIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_securitybulletinids)                         | Obtiene una colección de valores de cadena que contienen los identificadores de boletines de seguridad asociados a la actualización.                                                                      |
| [**SupersededUpdateIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_supersededupdateids)                         | Obtiene una colección de identificadores de actualización. Esta colección de identificadores especifica las actualizaciones que se sustituyen por la actualización.                                                    |
| [**SupportUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_supporturl)                                           | Obtiene un hipervínculo a la información de compatibilidad específica del idioma de la actualización.                                                                                                       |
| [**Title**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title)                                                     | Obtiene el título localizado de la actualización.                                                                                                                                             |
| [**Tipo**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_type)                                                       | Obtiene el tipo de la actualización.                                                                                                                                                        |
| [**UninstallationBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationbehavior)                   | Obtiene una interfaz que contiene las opciones de desinstalación de la actualización.                                                                                                          |
| [**UninstallationNotes**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationnotes)                         | Obtiene las notas de desinstalación de la actualización.                                                                                                                                       |
| [**UninstallationSteps**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationsteps)                         | Obtiene una interfaz que contiene los pasos de desinstalación de la actualización.                                                                                                            |



 

 

 



