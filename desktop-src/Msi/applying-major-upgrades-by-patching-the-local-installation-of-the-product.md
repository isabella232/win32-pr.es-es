---
description: Una actualización principal se puede aplicar a una aplicación si se aplica una revisión a la instalación local de la aplicación desde la línea de comandos o mediante un archivo ejecutable.
ms.assetid: be651457-5c66-478b-89d5-3d7607702b8e
title: Aplicar las actualizaciones principales mediante la revisión de la instalación local del producto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043d106ed9f8d6455ab4412959b70854a526a4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909101"
---
# <a name="applying-major-upgrades-by-patching-the-local-installation-of-the-product"></a>Aplicar las actualizaciones principales mediante la revisión de la instalación local del producto

Una actualización principal se puede aplicar a una aplicación si se aplica una revisión a la instalación local de la aplicación desde la línea de comandos o mediante un archivo ejecutable.

> [!Note]  
> No se recomienda proporcionar una actualización principal como paquete de revisión porque un paquete de revisión de actualización principal no se puede secuenciar con otras actualizaciones y porque la revisión no es una [revisión desinstalable](uninstallable-patches.md). La utilidad de [Msimsp.exe](msimsp-exe.md) no se puede usar para generar un paquete de revisión que aplique una actualización principal. En su lugar, aplique las actualizaciones principales, tal y como se describe en [aplicar actualizaciones principales instalando el producto](applying-major-upgrades-by-installing-the-product.md).

 

**Para aplicar una revisión de actualización principal a una instalación local del producto**

1.  Inicie la instalación de la revisión desde la línea de comandos o mediante un archivo ejecutable. Para iniciar desde la línea de comandos, use msiexec/p patch. msp. Para iniciar desde un archivo ejecutable, llame a [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o al [**método ApplyPatch**](installer-applypatch.md) y proporcione los mismos argumentos de la línea de comandos.
2.  Al aplicar una revisión a una instalación de cliente, el instalador omite el origen de instalación y continúa con la revisión de los archivos que ya están instalados en el equipo del usuario.
3.  El instalador cambia cualquier componente revisado marcado como ejecutar desde el origen a ejecución local. Los usuarios no pueden ejecutar estos componentes desde el origen, siempre y cuando la revisión permanezca en el equipo.
4.  El instalador agrega las transformaciones que se usan para actualizar el archivo. msi o agrega información específica de la revisión al perfil del usuario.
5.  El instalador almacena en caché el archivo. msi en el equipo del usuario para que pueda realizar la instalación a petición, reinstalar y reparar la aplicación. Después de aplicar una revisión a una instalación independiente, el instalador hace referencia a dos o más listas de origen a archivos externos: una para el origen original y otra para cada revisión que se ha aplicado.

 

 



