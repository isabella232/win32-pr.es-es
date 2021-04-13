---
description: El instalador registra los errores y los eventos en su propio registro de errores.
ms.assetid: 244e9afa-2052-469e-aa57-424e03ce5673
title: Registro normal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0846305ef53c596fbd6f117eaf76b0715a94c313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544251"
---
# <a name="normal-logging"></a>Registro normal

El instalador registra los errores y los eventos en su propio registro de errores. El tipo de registro que realiza el instalador viene determinado por la configuración del modo de registro. El registro está habilitado y el modo se puede establecer mediante los métodos siguientes:

-   El modo de registro de una instalación iniciada desde la línea de comandos se puede especificar mediante la opción/L de las opciones de la [línea de comandos](command-line-options.md). Si no se especifica el modo de registro mediante la opción de línea de comandos/L, se usará el modo de registro predeterminado.
-   El modo de registro de un proceso de instalación se puede especificar mediante programación con la función [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) o el método [**EnableLog**](installer-enablelog.md) . Si no se especifica el modo de registro mediante la función **MsiEnableLog** o el método **EnableLog** , se usará el modo de registro predeterminado.
-   El modo de registro predeterminado de un paquete de instalación determinado se puede especificar estableciendo la propiedad [**MsiLogging**](msilogging.md) en la [tabla de propiedades](property-table.md) del paquete. Esta propiedad está disponible a partir de Windows Installer 4,0.
-   Si la propiedad [**MsiLogging**](msilogging.md) está presente en la [tabla de propiedades](property-table.md), el modo de registro predeterminado del paquete se puede modificar cambiando el valor mediante una transformación de [base de datos](database-transforms.md). El modo de registro predeterminado no se puede cambiar mediante el uso de [paquetes de revisión](patch-packages.md) (un archivo. msp).
-   Si no se ha establecido la propiedad [**MsiLogging**](msilogging.md) , el modo de registro predeterminado para todos los usuarios del equipo se puede especificar mediante la Directiva de [registro](logging.md) .
-   Si se ha establecido la propiedad [**MsiLogging**](msilogging.md) , el modo de registro predeterminado para todos los usuarios del equipo se puede especificar mediante el establecimiento de la Directiva de [DisableLoggingFromPackage](disableloggingfrompackage.md) y la Directiva de [registro](logging.md) .
-   Si el modo de registro no se ha especificado con la opción/L, la propiedad [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), [**EnableLog**](installer-enablelog.md), [**MsiLogging**](msilogging.md) o la Directiva de [registro](logging.md) , el modo de registro predeterminado del paquete es el mismo que se obtiene al establecer la propiedad **MsiLogging** en ' iwearmo '.

 

 



