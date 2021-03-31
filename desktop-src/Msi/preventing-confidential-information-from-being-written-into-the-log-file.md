---
description: Los desarrolladores pueden impedir que se escriba información confidencial, como contraseñas, en el archivo de registro durante una instalación Windows Installer.
ms.assetid: 950c3c56-3f16-4e1a-875f-d31f45065076
title: Impedir que se escriba información confidencial en el archivo de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17880f18ca08745ab1f4f764397e17b7af8827e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082530"
---
# <a name="preventing-confidential-information-from-being-written-into-the-log-file"></a>Impedir que se escriba información confidencial en el archivo de registro

Al usar el Windows Installer, puede evitar que se escriba información confidencial, por ejemplo contraseñas, en el archivo de registro y se haga visible.

-   El instalador nunca escribe en el registro la información de la columna de contraseña de la [tabla ServiceInstall](serviceinstall-table.md) .
-   Puede impedir que el instalador escriba la propiedad asociada a un [control de edición](edit-control.md) en el registro estableciendo el atributo de [control de contraseña](password-control-attribute.md). La propiedad asociada a un control de edición que tiene el atributo de control de contraseña está oculta aunque la Directiva de [depuración](debug.md) esté establecida en un valor de 7.
-   Puede evitar que el instalador escriba una propiedad privada en el registro incluyendo la propiedad en la propiedad [**MsiHiddenProperties**](msihiddenproperties.md) .
    > [!Note]  
    > Este método puede hacer que la información confidencial especificada en una línea de comandos esté visible en el registro. Cuando la Directiva de [depuración](debug.md) está establecida en un valor de 7, el instalador escribe la información especificada en una línea de comandos en el registro. Esto hace que la propiedad especificada en una línea de comandos sea visible aunque la propiedad esté incluida en la propiedad [**MsiHiddenProperties**](msihiddenproperties.md) .

     

-   Puede evitar que la información de la columna target de la tabla [CustomAction](customaction-table.md) se escriba en el registro incluyendo la marca de bits HideTarget en el campo Type de la tabla CustomAction. El valor de esta marca es 8192 (0x2000). Para obtener más información, vea [opción de destino oculto de acción personalizada](custom-action-hidden-target-option.md).

 

 



