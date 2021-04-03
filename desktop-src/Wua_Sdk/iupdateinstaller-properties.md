---
description: La interfaz IUpdateInstaller define las siguientes propiedades.
ms.assetid: 876a2150-40a1-42a3-bc9a-05dec94fccd3
title: Propiedades de IUpdateInstaller
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77df235c49e7b6f27b0f93ec3b0c4def12135065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908063"
---
# <a name="iupdateinstaller-properties"></a>Propiedades de IUpdateInstaller

La interfaz [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) define las siguientes propiedades.



| Propiedad                                                                                      | Descripción                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowSourcePrompts**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_allowsourceprompts)                             | Obtiene y establece un valor booleano que indica si se van a mostrar mensajes de origen al usuario al instalar las actualizaciones.                  |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_clientapplicationid)                           | Obtiene y establece la aplicación cliente actual.                                                                                         |
| [**IsBusy**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isbusy)                                                     | Obtiene un valor booleano que indica si una instalación o desinstalación está en curso en un equipo en un momento determinado.        |
| [**IsForced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isforced)                                                 | Obtiene o establece un valor booleano que indica si se va a instalar o desinstalar forzosamente una actualización.                                       |
| [**ParentHwnd**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parenthwnd)                                             | Obtiene y establece un identificador para la ventana primaria que puede contener un cuadro de diálogo.                                                            |
| [**ParentWindow**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parentwindow)                                         | Obtiene y establece la interfaz que representa la ventana primaria que puede contener un cuadro de diálogo.                                          |
| [**RebootRequiredBeforeInstallation**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_rebootrequiredbeforeinstallation) | Obtiene un valor booleano que indica si es necesario reiniciar el sistema antes de instalar o desinstalar las actualizaciones.                   |
| [**Actualizaciones**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_updates)                                                   | Obtiene y establece una interfaz que contiene una colección de solo lectura de las actualizaciones que se especifican para la instalación o desinstalación. |



 

 

 



