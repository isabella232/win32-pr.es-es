---
description: Se puede aplicar una pequeña actualización a una aplicación mediante la aplicación de revisión de la instalación local de la aplicación.
ms.assetid: 2a04ffd0-d5b6-44f3-bef2-73f59179aed1
title: Aplicación de actualizaciones pequeñas mediante la aplicación de revisiones a la instalación local del producto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4519a8e9e5f50968e9b11bc8154cd73254c3fb81e4a7f4e4a69bb3136033df3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078105"
---
# <a name="applying-small-updates-by-patching-the-local-installation-of-the-product"></a>Aplicación de actualizaciones pequeñas mediante la aplicación de revisiones a la instalación local del producto

Se puede aplicar una pequeña actualización a una aplicación mediante la aplicación de revisión de la instalación local de la aplicación.

**Para aplicar una pequeña revisión de actualización a una instalación local del producto**

1.  Inicie la instalación de la revisión desde la línea de comandos o mediante un archivo ejecutable. Para iniciar desde la línea de comandos, use **msiexec /p \[ patch.msp REINSTALL=** Lista de _características_ *_\] REINSTALLMODE=omus_*. Para iniciar desde un archivo ejecutable, llame a [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o al método [**ApplyPatch**](installer-applypatch.md) y proporcione los mismos argumentos de línea de comandos.
2.  Al aplicar revisiones a una instalación de cliente, el instalador omite el origen de instalación y continúa con la revisión de los archivos que ya están instalados en el equipo del usuario.
3.  El instalador cambia los componentes con revisión marcados como run-from-source a run-locally. Los usuarios no pueden ejecutar estos componentes desde el origen mientras la revisión permanezca en el equipo.
4.  El instalador agrega las transformaciones que se usan para actualizar el archivo .msi o agrega información específica de la revisión al perfil del usuario.
5.  El instalador almacena en caché .msi archivo en el equipo del usuario para que pueda realizar la instalación a petición, reinstalar y reparar la aplicación. Después de aplicar una revisión a una instalación independiente, el instalador hace referencia a dos o más listas de origen a archivos externos: una para el origen original y otra para cada revisión que se ha aplicado.

 

 



