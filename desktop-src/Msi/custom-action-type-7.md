---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar una acción personalizada tipo 7 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 4a8f35f9-58a8-417e-b72e-159f4af7d83f
title: Tipo de acción personalizada 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d3cc1c68fae098c6ef70797ed87df887ff898a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082787"
---
# <a name="custom-action-type-7"></a>Tipo de acción personalizada 7

El tipo de acción personalizada 7 se usa con instalaciones simultáneas. No se recomiendan instalaciones simultáneas para la instalación de aplicaciones destinadas a publicarse en el público. Para obtener más información acerca de las instalaciones simultáneas, consulte [instalaciones simultáneas](concurrent-installations.md).

Esta acción personalizada instala otro paquete del instalador que está anidado dentro del primer paquete.

## <a name="source"></a>Source

La base de datos de la aplicación simultánea se almacena como un subalmacenamiento del paquete y el nombre del subalmacenamiento se designa en el campo origen de la [tabla CustomAction](customaction-table.md).

## <a name="numeric-type"></a>Tipo numérico



| Nombre de tipo                                                      | Value |
|----------------------------------------------------------------|-------|
| msidbCustomActionTypeInstall + msidbCustomActionTypeBinaryData | 7     |



 

## <a name="target"></a>Destino

El campo de destino de la [tabla CustomAction](customaction-table.md) contiene los valores de propiedades que se van a pasar a la instalación simultánea. Estos valores de propiedades pueden especificar características.

## <a name="return-processing-options"></a>Opciones de procesamiento de valores devueltos

La sesión de instalación simultánea se ejecuta como un subproceso independiente en el proceso actual. Una instalación simultánea no se puede ejecutar de forma asincrónica.

Vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Las marcas de opciones están disponibles para controlar la posible ejecución múltiple de acciones personalizadas. Consulte [Opciones de programación de la ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opciones de ejecución de In-Script

Esta acción personalizada no usa esta opción.

## <a name="return-values"></a>Valores devueltos

El estado de retorno de usuario Exit, error, Suspend o Success desde una instalación simultánea se procesa de la misma manera que cualquier otra acción. Sin embargo, tenga en cuenta que Windows Installer traduce los valores devueltos de todas las acciones cuando escribe el valor devuelto en el archivo de registro. Por ejemplo, si el valor devuelto de la acción aparece como 1 en el archivo de registro, significa que la acción devolvió un ERROR de \_ éxito. Para obtener más información sobre esta traducción, consulte [registro de valores devueltos de acciones](logging-of-action-return-values.md).

Tenga en cuenta que si se ha establecido **msidbCustomActionTypeContinue** en una instalación simultánea, se devuelve un error de \_ instalación de \_ USEREXIT, error de \_ instalación de reinicio, error al reiniciar el proceso de instalación \_ \_ \_ \_ o error de \_ \_ reinicio correcto \_ \_ . Esto significa que si establece **msidbCustomActionTypeContinue** y la instalación simultánea requiere un reinicio, se omitirá el requisito del reinicio. Además, se omitirá el código de error de la acción personalizada de instalación simultánea.

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
</dt> <dt>

[Valores devueltos de la acción personalizada](custom-action-return-values.md)
</dt> </dl>

 

 



