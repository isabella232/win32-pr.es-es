---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar una acción personalizada tipo 23 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 8219f157-585d-4733-8e10-c05813b398ba
title: Tipo de acción personalizada 23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05576c44ab634dc117501a89e6b86594f5483458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913870"
---
# <a name="custom-action-type-23"></a>Tipo de acción personalizada 23

El tipo de acción personalizada 23 se usa con instalaciones simultáneas. No se recomiendan instalaciones simultáneas para la instalación de aplicaciones destinadas a publicarse en el público. Para obtener información acerca de las instalaciones simultáneas, consulte [instalaciones](concurrent-installations.md)simultáneas.

Esta acción personalizada instala otro paquete del instalador que reside en el árbol de origen de la aplicación.

## <a name="source"></a>Source

La ubicación del paquete de instalación simultánea se especifica en relación con la raíz de la ubicación de origen que se muestra en el campo origen de la [tabla CustomAction](customaction-table.md).

## <a name="numeric-type"></a>Tipo numérico



| Nombre de tipo                                                      | Value |
|----------------------------------------------------------------|-------|
| msidbCustomActionTypeInstall + msidbCustomActionTypeSourceFile | 23    |



 

## <a name="target"></a>Destino

El campo de destino de la [tabla CustomAction](customaction-table.md) contiene valores de propiedades que se van a pasar a la instalación simultánea. Estos valores de propiedades pueden especificar características.

## <a name="return-processing-options"></a>Opciones de procesamiento de valores devueltos

La sesión de instalación simultánea se ejecuta como un subproceso independiente en el proceso actual. Una instalación simultánea no se puede ejecutar de forma asincrónica.

Para obtener más información, vea [Opciones de procesamiento de devoluciones de acciones personalizadas](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Las marcas de opciones están disponibles para controlar la posible ejecución múltiple de acciones personalizadas. Para obtener más información, consulte Opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opciones de ejecución de In-Script

No se utiliza.

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
</dt> <dt>

[Valores devueltos de la acción personalizada](custom-action-return-values.md)
</dt> </dl>

 

 



