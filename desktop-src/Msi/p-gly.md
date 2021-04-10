---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: P (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4e6b8f1343fdd68f4a6ce042852cff1e28e05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156321"
---
# <a name="p-windows-installer"></a>P (Windows Installer)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [o](o-gly.md) p [Q](q-gly.md) [R](r-gly.md) [s](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**configura**
</dt> <dd>

[*archivo. msi*](m-gly.md) y los [*archivos de código fuente externos a los*](e-gly.md) que puede apuntar este archivo. Por lo tanto, un paquete contiene toda la información que necesita el Windows Installer para ejecutar la interfaz de usuario y para instalar o desinstalar la aplicación. Para obtener más información, consulte también [*base de datos del instalador*](i-gly.md).

</dd> <dt>

<span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**código de paquete**
</dt> <dd>

GUID que identifica un paquete determinado. Se requiere un código de paquete único porque algunas transformaciones o paquetes de revisión se pueden aplicar a más de una aplicación o puede actualizar una aplicación a otra aplicación o versión. Para obtener más información, consulte [códigos de paquete](package-codes.md).

</dd> <dt>

<span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**revisiones**
</dt> <dd>

Método de actualización de un archivo que reemplaza solo los bits que se están cambiando, en lugar de todo el archivo. Esto significa que los usuarios pueden descargar una revisión de actualización para un producto que sea mucho más pequeño que todo el producto. Para obtener más información, vea [patch Packages](patch-packages.md).

</dd> <dt>

<span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**archivo de revisión**
</dt> <dd>

[Paquete P atch](patch-packages.md) usado para la revisión. Para obtener más información, consulte [revisiones y actualizaciones](patching-and-upgrades.md).

</dd> <dt>

<span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**modo de vista previa**
</dt> <dd>

Modo para ver el diseño de la interfaz de usuario. Para obtener más información, vea obtener [una vista previa de la interfaz de usuario](previewing-the-user-interface.md).

</dd> <dt>

<span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**barra de progreso**
</dt> <dd>

Controlar el instalador se puede mostrar durante el tiempo de ejecución del script que representa el progreso de la instalación. Para obtener más información, vea [crear un control ProgressBar](authoring-a-progressbar-control.md).

</dd> <dt>

<span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**propiedad**
</dt> <dd>

Variables globales utilizadas durante la instalación. (Consulte [acerca de las propiedades](about-properties.md)).

El término "propiedad" también hace referencia a un atributo de un objeto de automatización. (Consulte [interfaz de automatización](automation-interface.md)).

</dd> <dt>

<span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**edición**
</dt> <dd>

Método de [*publicidad*](a-gly.md) de una característica o aplicación. La publicación no rellena la interfaz de usuario. Sin embargo, si otra aplicación intenta abrir una aplicación publicada, hay suficiente información en el instalador para asignar la aplicación publicada. Para obtener más información, vea [*asignar*](a-gly.md) componentes y [características](components-and-features.md).

</dd> </dl>

 

 



