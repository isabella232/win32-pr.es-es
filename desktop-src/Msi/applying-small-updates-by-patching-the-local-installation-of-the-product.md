---
description: Se puede aplicar una actualización pequeña a una aplicación mediante la aplicación de una revisión de la instalación local de la aplicación.
ms.assetid: 2a04ffd0-d5b6-44f3-bef2-73f59179aed1
title: Aplicar actualizaciones pequeñas mediante la revisión de la instalación local del producto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bced3e7f69761ff3e270046718eedb9032cab8a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001747"
---
# <a name="applying-small-updates-by-patching-the-local-installation-of-the-product"></a>Aplicar actualizaciones pequeñas mediante la revisión de la instalación local del producto

Se puede aplicar una actualización pequeña a una aplicación mediante la aplicación de una revisión de la instalación local de la aplicación.

**Para aplicar una pequeña revisión de actualización a una instalación local del producto**

1.  Inicie la instalación de la revisión desde la línea de comandos o mediante un archivo ejecutable. Para iniciar desde la línea de comandos, use **msiexec/p patch. MSP REINSTALL \[ =**_lista de características_ *_\] REINSTALLMODE = OMUs_*. Para iniciar desde un archivo ejecutable, llame a [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o al [**método ApplyPatch**](installer-applypatch.md) y proporcione los mismos argumentos de la línea de comandos.
2.  Al aplicar una revisión a una instalación de cliente, el instalador omite el origen de instalación y continúa con la revisión de los archivos que ya están instalados en el equipo del usuario.
3.  El instalador cambia cualquier componente revisado marcado como ejecutar desde el origen a ejecución local. Los usuarios no pueden ejecutar estos componentes desde el origen, siempre y cuando la revisión permanezca en el equipo.
4.  El instalador agrega las transformaciones que se usan para actualizar el archivo. msi o agrega información específica de la revisión al perfil del usuario.
5.  El instalador almacena en caché el archivo. msi en el equipo del usuario para que pueda realizar la instalación a petición, reinstalar y reparar la aplicación. Después de aplicar una revisión a una instalación independiente, el instalador hace referencia a dos o más listas de origen a archivos externos: una para el origen original y otra para cada revisión que se ha aplicado.

 

 



