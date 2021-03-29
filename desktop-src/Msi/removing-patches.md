---
description: A partir de Windows Installer&\# 160; versión&\# 160; 3.0, es posible crear e instalar revisiones que se pueden desinstalar de forma individual y en cualquier orden, sin tener que desinstalar y volver a instalar toda la aplicación y otras revisiones.
ms.assetid: 2ad30ac9-eac9-49cf-98ae-5c053a0b500a
title: Quitar revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd54db3bde3a356a0c3adb299555248bbc87a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652784"
---
# <a name="removing-patches"></a>Quitar revisiones

A partir de Windows Installer versión 3,0, es posible crear e instalar revisiones que se pueden desinstalar de forma individual y en cualquier orden, sin tener que desinstalar y volver a instalar toda la aplicación y otras revisiones. Windows Installer 3,0 también permite crear [paquetes de revisiones](patch-packages.md) con una [tabla MsiPatchSequence](msipatchsequence-table.md) que contiene información sobre la secuenciación de revisiones. Con las versiones de Windows Installer anteriores a Windows Installer 3,0, el único método para quitar revisiones concretas de una aplicación consiste en desinstalar toda la aplicación con revisión y, a continuación, volver a instalar sin volver a aplicar las revisiones que se van a quitar.

El hecho de que una revisión se pueda desinstalar depende de cómo se haya creado la revisión, la versión de Windows Installer utilizada para instalar la revisión y los cambios realizados por la revisión en la aplicación. Si no se instala una revisión, la única manera de quitar la revisión es desinstalar toda la aplicación y reinstalar sin aplicar la revisión que se va a quitar.

Puede desinstalar una o varias revisiones mediante una opción de línea de comandos, la interfaz de scripting o llamando a [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) desde otra aplicación. Consulte [desinstalación de revisiones](uninstalling-patches.md) para obtener más información sobre cómo desinstalar revisiones.

El valor de la propiedad [**MSIPATCHREMOVE**](msipatchremove.md) muestra las revisiones que se van a desinstalar. Para cada revisión de la lista, el instalador comprueba que la revisión no se pueda instalar. Si el usuario no tiene privilegios para quitar la revisión, la revisión es desconocida para el producto, la Directiva de revisión impide la eliminación o la revisión se marcó como no desinstalable, el instalador devuelve un error que indica que se ha producido un error en la transacción de instalación. Vea [revisiones desinstalables](uninstallable-patches.md) para obtener más información acerca de qué determina si una revisión no se instala.

Una vez comprobada la revisión como extraíble, el instalador quita la revisión de la secuencia de aplicación de revisión. Para obtener más información sobre cómo Windows Installer 3,0 determina la secuencia que se va a usar al aplicar revisiones, consulte [secuenciación de revisiones](sequencing-patches.md). Tenga en cuenta que la eliminación de revisiones de la secuencia puede hacer que las revisiones estén marcadas como obsoletas o reemplazadas por activas.

Todas las revisiones seleccionadas para su eliminación se muestran en la propiedad [**MsiPatchRemovalList**](msipatchremovallist.md) . Esta propiedad es una propiedad privada establecida por el instalador y se puede usar en expresiones condicionales o consultarse mediante [acciones personalizadas](custom-actions.md). La propiedad contiene la lista de GUID de código de revisión de las revisiones que se van a quitar. Una acción personalizada puede determinar si el estado de instalación de la revisión se aplica, está obsoleto o se ha reemplazado llamando a la propiedad [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) o [**PatchProperty**](patch-patchproperty.md) del [objeto patch](patch-object.md).

Después de quitar una revisión, el estado de la aplicación es el mismo que si la revisión no se hubiera instalado nunca. Si es posible, el instalador restringe el proceso al subconjunto de características afectadas por la revisión que se va a quitar. El instalador establece automáticamente la propiedad [**REINSTALL**](reinstall.md) en la lista de características afectadas. Los archivos que se agregaron mediante la revisión se quitan y se sobrescriben los archivos modificados por la revisión. Los archivos y las entradas del registro se restauran a la versión esperada por el producto menos la revisión. Las características y los componentes que se agregaron mediante la revisión se anulan del registro de la aplicación. Tenga en cuenta que el contenido adicional agregado por la revisión puede permanecer en el equipo del usuario si otro parche lo usa, pero todavía es aplicable.

Si un archivo de un componente compartido se actualiza mediante una revisión, el cambio afecta a todas las aplicaciones que comparten el componente. Cuando se quita la revisión, el cambio afecta a todas las aplicaciones que comparten el componente. Esto significa que la eliminación de una revisión por parte de una aplicación puede restaurar el archivo del componente compartido a una versión inferior a la que requiere otra aplicación. Esto podría corregir la primera aplicación, pero hace que la segunda aplicación deje de funcionar. En este caso, la segunda aplicación se puede reparar reinstalando la segunda aplicación con los métodos descritos en [reinstalar una característica o aplicación](reinstalling-a-feature-or-application.md). Se restaurará la versión revisada del archivo.

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

[Revisión de desinstalación de acciones personalizadas](patch-uninstall-custom-actions.md)
</dt> <dt>

[Revisiones desinstalables](uninstallable-patches.md)
</dt> <dt>

[Desinstalación de revisiones](uninstalling-patches.md)
</dt> </dl>

 

 



