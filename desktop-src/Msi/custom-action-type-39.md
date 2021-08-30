---
description: Los desarrolladores Windows paquetes del instalador pueden optar por usar una acción personalizada de tipo 39 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: edf96cc6-ef32-4660-b4ee-50c130626e15
title: Tipo de acción personalizada 39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc28dbb970edab619d884ed8001305d5a3ffa93d4b673be6e2dbfcfde181855
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086235"
---
# <a name="custom-action-type-39"></a>Tipo de acción personalizada 39

El tipo de acción personalizada 39 se usa con instalaciones simultáneas. No se recomiendan las instalaciones simultáneas para la instalación de aplicaciones destinadas a la versión pública. Para obtener información sobre las instalaciones simultáneas, vea [Instalaciones simultáneas.](concurrent-installations.md)

La acción personalizada de tipo 39 instala una aplicación anunciada o ya instalada. Este tipo de acción personalizada se puede usar para volver a instalar o quitar un producto que se ha instalado como una instalación simultánea por el paquete de instalación del producto actual. La acción personalizada tipo 39 no se puede usar para volver a instalar o quitar ningún producto instalado previamente por ningún otro medio. Por ejemplo, si el producto secundario se instala mediante una acción personalizada de tipo 39, tipo 23 o tipo 7 durante la instalación del producto principal, se puede usar una acción personalizada de tipo 39 para quitar el producto secundario cuando se desinstala el producto principal.

## <a name="source"></a>Source

El campo Origen de la [tabla CustomAction](customaction-table.md) contiene el código de producto de la aplicación.

## <a name="numeric-type"></a>Tipo numérico



| Nombre de tipo                                                     | Value |
|---------------------------------------------------------------|-------|
| msidbCustomActionTypeInstall + msidbCustomActionTypeDirectory | 39    |



 

## <a name="target"></a>Destino

El campo Destino de la [tabla CustomAction contiene](customaction-table.md) valores de propiedad que se van a pasar a la instalación simultánea. Esta configuración de propiedades puede especificar características.

## <a name="return-processing-options"></a>Opciones de procesamiento de devolución

Se produce un error en el tipo de acción personalizada 39 si la aplicación no se anuncia ni se instala. Para evitar este error, debe establecer **msidbCustomActionTypeContinueflag**.

Una instalación simultánea no se puede ejecutar de forma asincrónica.

Vea Custom Action Return Processing Options ( Opciones de [procesamiento de devolución de acciones personalizadas).](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Las marcas de opciones están disponibles para controlar la posible ejecución múltiple de acciones personalizadas. Vea Custom Action Execution Scheduling Options ( Opciones [de programación de ejecución de acciones personalizadas).](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script de ejecución

La acción personalizada no usa esta opción.

## <a name="return-values"></a>Valores devueltos

El estado devuelto de la salida del usuario, el error, la suspensión o el éxito de una instalación simultánea se procesa de la misma manera que cualquier otra acción. Sin embargo, tenga Windows instalador traduce los valores devueltos de todas las acciones cuando escribe el valor devuelto en el archivo de registro. Por ejemplo, si el valor devuelto de la acción aparece como 1 en el archivo de registro, significa que la acción devolvió ERROR \_ SUCCESS. Para obtener más información, vea [Registro de valores devueltos de acción.](logging-of-action-return-values.md)

Tenga en cuenta que si una instalación simultánea tiene **msidbCustomActionTypeContinue** establecido, la devolución de ERROR \_ INSTALL \_ USEREXIT, ERROR INSTALL REBOOT, ERROR INSTALL REBOOT NOW o ERROR SUCCESS REBOOT REQUIRED se trata como \_ \_ ERROR \_ \_ \_ \_ \_ \_ \_ SUCCESS. Esto significa que si establece **msidbCustomActionTypeContinue** y la instalación simultánea requiere un reinicio, se omitirá el requisito para el reinicio. Además, se omitirá el código de error de la acción personalizada de instalación simultánea.

Si **no se establece msidbCustomActionTypeContinue,** los siguientes códigos de retorno más ERROR SUCCESS se tratan como correctos y tienen los \_ significados siguientes. Otros códigos de retorno se tratan como errores.



| Mensaje                          | Significado                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| ERROR \_ AL REINICIAR LA \_ INSTALACIÓN           | La marca de reinicio se establecerá para reiniciarse al final de la instalación.                                  |
| ERROR \_ AL INSTALAR EL REINICIO \_ \_ AHORA      | Es necesario reiniciar antes de completar la instalación. El reinicio se procesará inmediatamente. |
| ERROR \_ NECESARIO PARA REINICIAR \_ \_ CORRECTAMENTE | Se requiere un reinicio, pero se ha suprimido.                                                          |



 

## <a name="remarks"></a>Comentarios

Se requiere una expresión condicional para habilitar la instalación simultánea en la instalación o eliminación del componente o la característica asociados.

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

 

 



