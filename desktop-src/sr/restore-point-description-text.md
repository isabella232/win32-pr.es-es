---
title: Texto de descripción del punto de restauración
description: Cuando una aplicación llama a la función SRSetRestorePoint, puede proporcionar cualquier texto como descripción para el punto de restauración. sin embargo, en la tabla siguiente se muestra el texto de descripción recomendado.
ms.assetid: e6e1974b-c162-4019-9349-936f3786cb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd785d143d3eed243e5d80ec261f121817db6187013f70b6f6cc6be0b1c2b790
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111255"
---
# <a name="restore-point-description-text"></a>Texto de descripción del punto de restauración

Cuando una aplicación llama a [**la función SRSetRestorePoint,**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) puede proporcionar cualquier texto como descripción para el punto de restauración. sin embargo, en la tabla siguiente se muestra el texto de descripción recomendado.



| Modificación del sistema                            | Tipo de punto de restauración      | Descripción            |
|------------------------------------------------|-------------------------|------------------------|
| Instalación de la aplicación                       | INSTALACIÓN DE \_ LA APLICACIÓN    | AppName *instalado*    |
| Modificación de la aplicación (agregar o quitar características) | MODIFICAR \_ CONFIGURACIÓN        | AppName *configurado*   |
| Eliminación de aplicaciones                            | DESINSTALACIÓN DE \_ APLICACIONES  | Se ha *quitado AppName*      |
| Instalación del controlador de dispositivo                     | INSTALACIÓN \_ DEL CONTROLADOR DE \_ DISPOSITIVO | Installed *DriverName* |



 

Los instaladores, como Windows Installer e InstallShield, usan estas convenciones para el texto de descripción:

-   El nombre del producto sigue el verbo ; por ejemplo, Installed *AppName*.
-   El nombre del producto se puede usar por sí solo *(AppName*) o el nombre del producto y el nombre de la empresa (*MyCompany AppName*).

 

 




