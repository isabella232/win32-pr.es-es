---
title: Texto de descripción de punto de restauración
description: Cuando una aplicación llama a la función SRSetRestorePoint, puede proporcionar cualquier texto como una descripción para el punto de restauración; sin embargo, en la siguiente tabla se muestra el texto de Descripción recomendado.
ms.assetid: e6e1974b-c162-4019-9349-936f3786cb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e90fd1b7d5776c8c3798a68946382cc702b3bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268877"
---
# <a name="restore-point-description-text"></a>Texto de descripción de punto de restauración

Cuando una aplicación llama a la función [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) , puede proporcionar cualquier texto como una descripción para el punto de restauración; sin embargo, en la siguiente tabla se muestra el texto de Descripción recomendado.



| Modificación del sistema                            | Tipo de punto de restauración      | Descripción            |
|------------------------------------------------|-------------------------|------------------------|
| Instalación de la aplicación                       | instalación de la aplicación \_    | Se instaló *appname*    |
| Modificación de aplicaciones (agregar o quitar características) | MODIFICAR \_ configuración        | *Nombreaplicación* configurado   |
| Eliminación de aplicaciones                            | desinstalación de la aplicación \_  | Se quitó *appname*      |
| Instalación del controlador de dispositivo                     | \_instalación del controlador de dispositivo \_ | Instalado *drivername* |



 

Los instaladores, como Windows Installer e InstallShield, usan estas convenciones para el texto descriptivo:

-   El nombre del producto sigue el verbo; por ejemplo, instalado *appname*.
-   El nombre de producto se puede usar solo (*appname*) o el nombre del producto y el nombre de la empresa se pueden usar (*MyCompany appname*).

 

 




