---
description: Los desarrolladores pueden impedir que se pueda especificar información confidencial, como contraseñas, en el archivo de registro durante una instalación Windows Installer.
ms.assetid: 950c3c56-3f16-4e1a-875f-d31f45065076
title: Impedir que se escriba información confidencial en el archivo de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17880f18ca08745ab1f4f764397e17b7af8827e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473957"
---
# <a name="preventing-confidential-information-from-being-written-into-the-log-file"></a>Impedir que se escriba información confidencial en el archivo de registro

Cuando se usa Windows Installer, puede evitar que la información confidencial, por ejemplo, las contraseñas, se introduce en el archivo de registro y se hace visible.

-   El instalador nunca escribe la información de la columna Contraseña de la [tabla ServiceInstall](serviceinstall-table.md) en el registro.
-   Puede impedir que el instalador escriba la propiedad asociada a un [Control de edición](edit-control.md) en el registro estableciendo el atributo [de control de contraseña](password-control-attribute.md). La propiedad asociada a un control de edición que tiene el atributo de control de contraseña está oculta incluso si la [directiva de](debug.md) depuración está establecida en un valor de 7.
-   Puede impedir que el instalador escriba una propiedad privada en el registro incluyendo la propiedad en [**la propiedad MsiHiddenProperties.**](msihiddenproperties.md)
    > [!Note]  
    > Este método puede hacer que la información confidencial especificada en una línea de comandos sea visible en el registro. Cuando la [directiva](debug.md) de depuración se establece en un valor de 7, el instalador escribirá la información especificada en una línea de comandos en el registro. Esto hace que la propiedad especificada en una línea de comandos sea visible incluso si la propiedad está incluida en [**la propiedad MsiHiddenProperties.**](msihiddenproperties.md)

     

-   Puede evitar que la información de la columna Destino de la tabla [CustomAction](customaction-table.md) se escriba en el registro incluyendo la marca de bits HideTarget en el campo Tipo de la tabla CustomAction. El valor de esta marca es 8192 (0x2000). Para obtener más información, vea [Custom Action Hidden Target Option](custom-action-hidden-target-option.md).

 

 



