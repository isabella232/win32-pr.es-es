---
description: El instalador registra errores y eventos en su propio registro de errores.
ms.assetid: 244e9afa-2052-469e-aa57-424e03ce5673
title: Registro normal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd1abeb4f110603bcc596cb7981ea65c7d9820d8054adc7533c4f85de2d8bf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828545"
---
# <a name="normal-logging"></a>Registro normal

El instalador registra errores y eventos en su propio registro de errores. El tipo de registro que realiza el instalador viene determinado por la configuración del modo de registro. El registro está habilitado y el modo se puede establecer mediante los métodos siguientes:

-   El modo de registro de una instalación iniciada desde la línea de comandos se puede especificar mediante la opción /L de opciones [de la línea de comandos](command-line-options.md). Si no se especifica el modo de registro mediante la opción de línea de comandos /L, se usará el modo de registro predeterminado.
-   El modo de registro de un proceso de instalación se puede especificar mediante programación mediante la [**función MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) o el [**método EnableLog.**](installer-enablelog.md) Si el modo de registro no se especifica mediante la función **MsiEnableLog** o el método **EnableLog,** se usará el modo de registro predeterminado.
-   El modo de registro predeterminado de un paquete de instalación determinado se puede especificar estableciendo la [**propiedad MsiLogging**](msilogging.md) en la [tabla Property](property-table.md) del paquete. Esta propiedad está disponible a partir de Windows Installer 4.0.
-   Si la [**propiedad MsiLogging**](msilogging.md) está presente en la tabla [Property](property-table.md), el modo de registro predeterminado del paquete se puede modificar cambiando el valor mediante una transformación de base [de datos](database-transforms.md). El modo de registro predeterminado no se puede cambiar mediante paquetes [de revisión](patch-packages.md) (un archivo .msp).
-   Si no se ha establecido la propiedad [**MsiLogging,**](msilogging.md) se puede especificar el modo de registro predeterminado para todos los usuarios del equipo mediante la [directiva de](logging.md) registro.
-   Si se ha establecido la propiedad [**MsiLogging,**](msilogging.md) se puede especificar el modo de registro predeterminado para todos los usuarios del equipo estableciendo la directiva [DisableLoggingFromPackage](disableloggingfrompackage.md) y la [directiva de](logging.md) registro.
-   Si la opción /L, [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), [**EnableLog**](installer-enablelog.md), [**MsiLogging**](msilogging.md) o la directiva [de](logging.md) registro no han especificado el modo de registro predeterminado para el paquete, el modo de registro predeterminado para el paquete es el mismo modo que se obtiene al establecer la propiedad **MsiLogging** en "iloggingmo".

 

 



