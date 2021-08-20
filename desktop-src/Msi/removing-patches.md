---
description: A partir de Windows Installer&\# 160;versión&160;3.0, es posible crear e instalar revisiones que se pueden desinstalar de forma independiente y en cualquier orden, sin tener que desinstalar y reinstalar toda la aplicación y otras \# revisiones.
ms.assetid: 2ad30ac9-eac9-49cf-98ae-5c053a0b500a
title: Eliminación de revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18998207ead28729101fd8782432cb25bf31f0d4763faa8e99c341f9b1fde7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990705"
---
# <a name="removing-patches"></a>Eliminación de revisiones

A partir de Windows Installer versión 3.0, es posible crear e instalar revisiones que se pueden desinstalar de forma independiente y en cualquier orden, sin tener que desinstalar y reinstalar toda la aplicación y otras revisiones. Windows El instalador 3.0 también permite crear paquetes de revisión con una tabla [MsiPatchSequence](msipatchsequence-table.md) que contiene información de secuenciación de revisiones. [](patch-packages.md) Con versiones de Windows Installer anteriores a Windows Installer 3.0, el único método para quitar revisiones concretas de una aplicación es desinstalar toda la aplicación con revisión y, a continuación, volver a instalar sin volver a aplicar ninguna revisión que se va a quitar.

Si se puede desinstalar una revisión depende de cómo se haya creado la revisión, de la versión de Windows Installer usada para instalar la revisión y de los cambios realizados por la revisión en la aplicación. Si una revisión no se puede desinstalar, la única manera de quitar la revisión es desinstalar toda la aplicación y volver a instalarla sin aplicar la revisión que se va a quitar.

Puede desinstalar una o varias revisiones mediante una opción de línea de comandos, la interfaz de scripting o llamando a [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) desde otra aplicación. Consulte [Desinstalación de revisiones para](uninstalling-patches.md) obtener más información sobre cómo desinstalar revisiones.

El valor de la [**propiedad MSIPATCHREMOVE**](msipatchremove.md) enumera las revisiones que se desinstalarán. Para cada revisión de la lista, el instalador comprueba que la revisión se puede desinstalar. Si el usuario no tiene privilegios para quitar la revisión, la revisión es desconocida para el producto, la directiva de revisión impide la eliminación o la revisión se ha marcado como no desinstalable, el instalador devuelve un error que indica una transacción de instalación con errores. Consulte [Revisiones desinstalables para](uninstallable-patches.md) obtener más información sobre lo que determina si una revisión no se puede desinstalar.

Una vez que la revisión se comprueba como extraíble, el instalador quita la revisión de la secuencia de aplicación de revisiones. Para obtener más información sobre Windows Installer 3.0 determina qué secuencia usar al aplicar revisiones, vea [Secuenciar revisiones](sequencing-patches.md). Tenga en cuenta que la eliminación de revisiones de la secuencia puede hacer que las revisiones marcadas como obsoletas o reemplazadas se activen.

Todas las revisiones seleccionadas para su eliminación se muestran [**en la propiedad MsiPatchRemovalList.**](msipatchremovallist.md) Esta propiedad es una propiedad privada establecida por el instalador y se puede usar en expresiones condicionales o consultada por [acciones personalizadas.](custom-actions.md) La propiedad contiene la lista de GUID de código de revisión de revisiones que se quitarán. Una acción personalizada puede determinar si el estado de instalación de la revisión se aplica, está obsoleto o se reemplaza mediante una llamada a [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) o a la propiedad [**PatchProperty**](patch-patchproperty.md) del [objeto Patch](patch-object.md).

Después de quitar una revisión, el estado de la aplicación es el mismo que si la revisión nunca se instalara. Si es posible, el instalador restringe el proceso al subconjunto de características afectadas por la revisión que se va a quitar. El instalador establece automáticamente la propiedad [**REINSTALL**](reinstall.md) en la lista de características afectadas. Los archivos agregados por la revisión se quitan y se sobrescriben los archivos modificados por la revisión. Los archivos y las entradas del Registro se restauran a la versión esperada por el producto menos la revisión. Las características y los componentes agregados por la revisión no se registrarán en la aplicación. Tenga en cuenta que el contenido adicional agregado por la revisión puede permanecer en el equipo del usuario si el contenido lo usa otra revisión que sigue siendo aplicable.

Si una revisión actualiza un archivo de un componente compartido, el cambio afecta a todas las aplicaciones que comparten el componente. Cuando se quita la revisión, de nuevo, el cambio afecta a todas las aplicaciones que comparten el componente. Esto significa que la eliminación de una revisión por parte de una aplicación puede restaurar el archivo del componente compartido a una versión inferior a la requerida por otra aplicación. Esto podría corregir la primera aplicación, pero hacer que la segunda deje de funcionar. En este caso, la segunda aplicación se puede reparar reinstalando la segunda aplicación mediante los métodos que se describen en Reinstalación de una [característica o aplicación.](reinstalling-a-feature-or-application.md) Esto restaurará la versión con revisión del archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[Secuenciación de revisiones](sequencing-patches.md)
</dt> <dt>

[Acciones personalizadas de desinstalación de revisiones](patch-uninstall-custom-actions.md)
</dt> <dt>

[Revisiones que se pueden desinstalar](uninstallable-patches.md)
</dt> <dt>

[Desinstalación de revisiones](uninstalling-patches.md)
</dt> </dl>

 

 



