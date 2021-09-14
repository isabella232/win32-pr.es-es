---
description: Cuando no se requieren privilegios elevados para instalar un paquete del instalador de Windows, el autor del paquete puede suprimir el cuadro de diálogo que muestra control de cuentas de usuario (UAC) para solicitar a los usuarios autorización de administrador.
ms.assetid: cab30f95-cc93-46db-aba5-741b44adb6de
title: Crear paquetes sin el cuadro de diálogo UAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dcd44bf7d2250e12e7cafde46b57978b48cceb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159022"
---
# <a name="authoring-packages-without-the-uac-dialog-box"></a>Crear paquetes sin el cuadro de diálogo UAC

Cuando no se requieren privilegios elevados para instalar un paquete del instalador de Windows, el autor del paquete puede suprimir el cuadro de diálogo que se muestra en [*Control*](u-gly.md) de cuentas de usuario (UAC) para solicitar a los usuarios autorización de administrador.

Para suprimir la presentación del cuadro de diálogo UAC al instalar la aplicación, el autor del paquete debe hacer lo siguiente:

-   Instale la aplicación mediante Windows Installer 4.0 o posterior en Windows Vista.
-   No dependa del uso de privilegios elevados del sistema para instalar la aplicación en el equipo.
-   Instale la aplicación en el contexto por usuario y haga que sea el contexto de instalación predeterminado del paquete. Si no se establece la propiedad [**ALLUSERS,**](allusers.md) el instalador instala el paquete en el contexto por usuario. Si no incluye la propiedad **ALLUSERS** en la tabla [Property](property-table.md), el instalador no establece esta propiedad y, por tanto, la instalación por usuario se convierte en el contexto de instalación predeterminado. Puede invalidar este valor predeterminado estableciendo la **propiedad ALLUSERS** en la línea de comandos.
-   Establezca bit 3 en la [**propiedad Resumen de recuento**](word-count-summary.md) de palabras para indicar que no se necesitan privilegios elevados para instalar la aplicación.

 

 



