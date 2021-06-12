---
description: Obtenga información Windows Installer conceptos que comienzan por la letra P, como el código del paquete y la aplicación de revisiones.
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: P (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8923359197916a1186fe28ab0d12e4118b989bc
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011108"
---
# <a name="p-windows-installer"></a>P (Windows Installer)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L M [N](m-gly.md) [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**Paquete**
</dt> <dd>

[*.msi archivo y*](m-gly.md) cualquier [*archivo de origen externo*](e-gly.md) al que pueda apuntar este archivo. Por lo tanto, un paquete contiene toda la información Windows Installer debe ejecutar la interfaz de usuario y para instalar o desinstalar la aplicación. Para obtener más información, vea también instalador [*de base de datos*](i-gly.md).

</dd> <dt>

<span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**código del paquete**
</dt> <dd>

GUID que identifica un paquete determinado. Se requiere un código de paquete único porque algunas transformaciones o paquetes de revisión se pueden aplicar a más de una aplicación o pueden actualizar una aplicación a otra aplicación o versión. Para obtener más información, vea [Códigos de paquete](package-codes.md).

</dd> <dt>

<span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**Parches**
</dt> <dd>

Método de actualización de un archivo que reemplaza solo los bits que se cambian, en lugar de todo el archivo. Esto significa que los usuarios pueden descargar una revisión de actualización para un producto que es mucho menor que todo el producto. Para obtener más información, vea [Paquetes de revisión.](patch-packages.md)

</dd> <dt>

<span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**archivo de revisión**
</dt> <dd>

Paquete [P atch usado](patch-packages.md) para la aplicación de revisiones. Para obtener más información, vea [Aplicación de revisiones y actualizaciones.](patching-and-upgrades.md)

</dd> <dt>

<span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**modo de vista previa**
</dt> <dd>

Modo para ver el diseño de la interfaz de usuario. Para obtener más información, vea [Vista previa del Interfaz de usuario](previewing-the-user-interface.md).

</dd> <dt>

<span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**barra de progreso**
</dt> <dd>

Controlar el instalador puede mostrarse durante el tiempo de ejecución del script que representa el progreso de la instalación. Para obtener más información, [vea Creación de un control ProgressBar](authoring-a-progressbar-control.md).

</dd> <dt>

<span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**Propiedad**
</dt> <dd>

Variables globales usadas durante una instalación. (Vea [Acerca de las propiedades](about-properties.md)).

El término "propiedad" también hace referencia a un atributo de un objeto de automatización. (Consulte [La interfaz de Automation).](automation-interface.md)

</dd> <dt>

<span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**Editorial**
</dt> <dd>

Método para [*anunciar*](a-gly.md) una característica o aplicación. La publicación no rellena la interfaz de usuario. Sin embargo, si otra aplicación intenta abrir una aplicación publicada, hay suficiente información para que el instalador asigne la aplicación publicada. Para obtener más información, vea [*asignación de*](a-gly.md) componentes [y características.](components-and-features.md)

</dd> </dl>

 

 



