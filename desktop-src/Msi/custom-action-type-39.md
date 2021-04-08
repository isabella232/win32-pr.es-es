---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar un tipo de acción personalizada 39 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: edf96cc6-ef32-4660-b4ee-50c130626e15
title: Tipo de acción personalizada 39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e49667fbad6e71aa8b2197b00ae9dd49f7dfff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910709"
---
# <a name="custom-action-type-39"></a>Tipo de acción personalizada 39

El tipo de acción personalizada 39 se usa con instalaciones simultáneas. No se recomiendan instalaciones simultáneas para la instalación de aplicaciones destinadas a publicarse en el público. Para obtener información acerca de las instalaciones simultáneas, consulte [instalaciones](concurrent-installations.md)simultáneas.

La acción personalizada Type 39 instala una aplicación anunciada o ya instalada. Este tipo de acción personalizada se puede usar para reinstalar o quitar un producto que el paquete de instalación del producto actual ha instalado como una instalación simultánea. La acción personalizada Type 39 no se puede usar para reinstalar o quitar ningún producto instalado previamente por otros medios. Por ejemplo, si el producto secundario se instala mediante un tipo 39, el tipo 23 o la acción personalizada tipo 7 durante la instalación del producto principal, se puede usar una acción personalizada tipo 39 para quitar el producto secundario cuando se desinstale el producto principal.

## <a name="source"></a>Source

El campo de origen de la [tabla CustomAction](customaction-table.md) contiene el código de producto de la aplicación.

## <a name="numeric-type"></a>Tipo numérico



| Nombre de tipo                                                     | Value |
|---------------------------------------------------------------|-------|
| msidbCustomActionTypeInstall + msidbCustomActionTypeDirectory | 39    |



 

## <a name="target"></a>Destino

El campo de destino de la [tabla CustomAction](customaction-table.md) contiene valores de propiedades que se van a pasar a la instalación simultánea. Estos valores de propiedades pueden especificar características.

## <a name="return-processing-options"></a>Opciones de procesamiento de valores devueltos

Se produce un error en el tipo de acción personalizada 39 si la aplicación no se anuncia ni se instala. Para evitar este error, debe establecer **msidbCustomActionTypeContinueflag**.

Una instalación simultánea no se puede ejecutar de forma asincrónica.

Vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Las marcas de opciones están disponibles para controlar la posible ejecución múltiple de acciones personalizadas. Consulte [Opciones de programación de la ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opciones de ejecución de In-Script

La acción personalizada no usa esta opción.

## <a name="return-values"></a>Valores devueltos

El estado de retorno de usuario Exit, error, Suspend o Success desde una instalación simultánea se procesa de la misma manera que cualquier otra acción. Sin embargo, tenga en cuenta que Windows Installer traduce los valores devueltos de todas las acciones cuando escribe el valor devuelto en el archivo de registro. Por ejemplo, si el valor devuelto de la acción aparece como 1 en el archivo de registro, significa que la acción devolvió un ERROR de \_ éxito. Para obtener más información, vea [registro de valores devueltos de acción](logging-of-action-return-values.md).

Tenga en cuenta que si se establece **msidbCustomActionTypeContinue** en una instalación simultánea, se reiniciará un error de instalación de \_ \_ USEREXIT, error de \_ instalación de \_ reinicio, error al reiniciar el proceso de \_ instalación \_ \_ , o \_ \_ se requiere un reinicio correcto \_ \_ para el error. Esto significa que si establece **msidbCustomActionTypeContinue** y la instalación simultánea requiere un reinicio, se omitirá el requisito del reinicio. Además, se omitirá el código de error de la acción personalizada de instalación simultánea.

Si no se establece **msidbCustomActionTypeContinue** , los siguientes códigos de retorno \_ y error correcto se tratan como correctos y tienen los significados siguientes. Otros códigos de retorno se tratan como errores.



| Mensaje                          | Significado                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| ERROR de \_ instalación de \_ reinicio           | La marca de reinicio se establecerá para reiniciarse al final de la instalación.                                  |
| ERROR \_ al \_ reiniciar \_ ahora      | Se requiere un reinicio antes de completar la instalación. El reinicio se procesará inmediatamente. |
| ERROR \_ de \_ reinicio correcto \_ necesario | Se requiere un reinicio, pero se suprime.                                                          |



 

## <a name="remarks"></a>Observaciones

Se requiere una expresión condicional para habilitar la instalación simultánea en la instalación o desinstalación del componente o característica asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instalaciones simultáneas](concurrent-installations.md)
</dt> <dt>

[Referencia de acción personalizada](custom-action-reference.md)
</dt> <dt>

[Acerca de las acciones personalizadas](about-custom-actions.md)
</dt> <dt>

[Uso de acciones personalizadas](using-custom-actions.md)
</dt> </dl>

 

 



