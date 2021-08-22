---
description: La interfaz IUpdateInstaller define las siguientes propiedades.
ms.assetid: 876a2150-40a1-42a3-bc9a-05dec94fccd3
title: Propiedades de IUpdateInstaller
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c6076e395e98ef21cd54fbf45ffdc5e57bc29fa8ceffc78c16d9a9a0d2bc4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049153"
---
# <a name="iupdateinstaller-properties"></a>Propiedades de IUpdateInstaller

La [**interfaz IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) define las siguientes propiedades.



| Propiedad                                                                                      | Descripción                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowSourcePrompts**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_allowsourceprompts)                             | Obtiene y establece un valor booleano que indica si se deben mostrar mensajes de origen al usuario al instalar las actualizaciones.                  |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_clientapplicationid)                           | Obtiene y establece la aplicación cliente actual.                                                                                         |
| [**IsBusy**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isbusy)                                                     | Obtiene un valor booleano que indica si una instalación o desinstalación está en curso en un equipo en un momento específico.        |
| [**Se aplica**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isforced)                                                 | Obtiene o establece un valor booleano que indica si se debe instalar o desinstalar una actualización de forma forzada.                                       |
| [**ParentHwnd**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parenthwnd)                                             | Obtiene y establece un identificador para la ventana primaria que puede contener un cuadro de diálogo.                                                            |
| [**ParentWindow**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parentwindow)                                         | Obtiene y establece la interfaz que representa la ventana primaria que puede contener un cuadro de diálogo.                                          |
| [**RebootRequiredBeforeInstallation**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_rebootrequiredbeforeinstallation) | Obtiene un valor booleano que indica si se requiere un reinicio del sistema antes de instalar o desinstalar actualizaciones.                   |
| [**Actualizaciones**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_updates)                                                   | Obtiene y establece una interfaz que contiene una colección de solo lectura de las actualizaciones especificadas para la instalación o desinstalación. |



 

 

 



