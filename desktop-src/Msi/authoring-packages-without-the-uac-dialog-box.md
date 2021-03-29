---
description: Cuando no se necesitan privilegios elevados para instalar un paquete de Windows Installer, el autor del paquete puede suprimir el cuadro de diálogo que muestra el control de cuentas de usuario (UAC) para solicitar a los usuarios la autorización de administrador.
ms.assetid: cab30f95-cc93-46db-aba5-741b44adb6de
title: Crear paquetes sin el cuadro de diálogo UAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dcd44bf7d2250e12e7cafde46b57978b48cceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813331"
---
# <a name="authoring-packages-without-the-uac-dialog-box"></a>Crear paquetes sin el cuadro de diálogo UAC

Cuando no se necesitan privilegios elevados para instalar un paquete de Windows Installer, el autor del paquete puede suprimir el cuadro de diálogo que muestra el [*control de cuentas de usuario*](u-gly.md) (UAC) para solicitar a los usuarios la autorización de administrador.

Para suprimir la presentación del cuadro de diálogo de UAC al instalar la aplicación, el autor del paquete debe hacer lo siguiente:

-   Instale la aplicación mediante el instalador de Windows 4,0 o posterior en Windows Vista.
-   No dependa de usar privilegios del sistema elevados para instalar la aplicación en el equipo.
-   Instale la aplicación en el contexto por usuario y haga que este sea el contexto de instalación predeterminado del paquete. Si no se establece la propiedad [**AllUsers**](allusers.md) , el instalador instala el paquete en el contexto por usuario. Si no incluye la propiedad **AllUsers** en la tabla de [propiedades](property-table.md), el instalador no establece esta propiedad y, por tanto, la instalación por usuario se convierte en el contexto de instalación predeterminado. Puede invalidar este valor predeterminado estableciendo la propiedad **AllUsers** en la línea de comandos.
-   Establezca bit 3 en la propiedad [**Resumen de recuento de palabras**](word-count-summary.md) para indicar que no se necesitan privilegios elevados para instalar la aplicación.

 

 



