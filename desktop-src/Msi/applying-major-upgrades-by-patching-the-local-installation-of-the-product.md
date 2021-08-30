---
description: Una actualización principal se puede aplicar a una aplicación mediante la aplicación de revisiones de la instalación local de la aplicación desde la línea de comandos o mediante un archivo ejecutable.
ms.assetid: be651457-5c66-478b-89d5-3d7607702b8e
title: Aplicación de actualizaciones principales mediante la aplicación de revisiones a la instalación local del producto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8ee1aab4290e7cf81004f440af739b1adcd3442bd31d0e5c991db129874ff3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927075"
---
# <a name="applying-major-upgrades-by-patching-the-local-installation-of-the-product"></a>Aplicación de actualizaciones principales mediante la aplicación de revisiones a la instalación local del producto

Una actualización principal se puede aplicar a una aplicación mediante la aplicación de revisiones de la instalación local de la aplicación desde la línea de comandos o mediante un archivo ejecutable.

> [!Note]  
> No se recomienda proporcionar una actualización principal como paquete de revisión porque un paquete de revisión de actualización principal no se puede secuenciar con otras actualizaciones y porque la revisión no es una revisión [que se pueda desinstalar.](uninstallable-patches.md) La [Msimsp.exe](msimsp-exe.md) no se puede usar para generar un paquete de revisión que aplique una actualización principal. En su lugar, aplique las actualizaciones principales como se describe en Aplicar actualizaciones [principales mediante la instalación del producto](applying-major-upgrades-by-installing-the-product.md).

 

**Para aplicar una revisión de actualización principal a una instalación local del producto**

1.  Inicie la instalación de la revisión desde la línea de comandos o mediante un archivo ejecutable. Para iniciar desde la línea de comandos, use msiexec /p patch.msp. Para iniciar desde un ejecutable, llame a [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o al método [**ApplyPatch**](installer-applypatch.md) y proporcione los mismos argumentos de línea de comandos.
2.  Al aplicar revisiones a una instalación de cliente, el instalador omite el origen de instalación y continúa con la revisión de los archivos que ya están instalados en el equipo del usuario.
3.  El instalador cambia los componentes con revisión marcados como run-from-source a run-locally. Los usuarios no pueden ejecutar estos componentes desde el origen mientras la revisión permanezca en el equipo.
4.  El instalador agrega todas las transformaciones que se usan para actualizar el archivo .msi o agrega información específica de la revisión al perfil del usuario.
5.  El instalador almacena en caché .msi archivo en el equipo del usuario para que pueda realizar la instalación a petición, reinstalar y reparar la aplicación. Después de aplicar una revisión a una instalación independiente, el instalador hace referencia a dos o más listas de origen a archivos externos: uno para el origen original y otro para cada revisión que se ha aplicado.

 

 



