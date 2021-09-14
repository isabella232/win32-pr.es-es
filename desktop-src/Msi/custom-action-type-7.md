---
description: Los desarrolladores Windows paquetes del instalador pueden optar por usar una acción personalizada de tipo 7 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 4a8f35f9-58a8-417e-b72e-159f4af7d83f
title: Tipo de acción personalizada 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d3cc1c68fae098c6ef70797ed87df887ff898a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158670"
---
# <a name="custom-action-type-7"></a>Tipo de acción personalizada 7

El tipo de acción personalizada 7 se usa con instalaciones simultáneas. No se recomiendan las instalaciones simultáneas para la instalación de aplicaciones destinadas a la versión pública. Para obtener más información sobre las instalaciones simultáneas, vea [Instalaciones simultáneas.](concurrent-installations.md)

Esta acción personalizada instala otro paquete del instalador que está anidado dentro del primer paquete.

## <a name="source"></a>Source

La base de datos de la aplicación simultánea se almacena como un subalmacenamiento del paquete y el nombre del subalmacenamiento se designa en el campo Origen de la [tabla CustomAction](customaction-table.md).

## <a name="numeric-type"></a>Tipo numérico



| Nombre de tipo                                                      | Value |
|----------------------------------------------------------------|-------|
| msidbCustomActionTypeInstall + msidbCustomActionTypeBinaryData | 7     |



 

## <a name="target"></a>Destino

El campo Destino de la [tabla CustomAction contiene](customaction-table.md) la configuración de propiedades que se pasará a la instalación simultánea. Esta configuración de propiedades puede especificar características.

## <a name="return-processing-options"></a>Opciones de procesamiento de devolución

La sesión de instalación simultánea se ejecuta como un subproceso independiente en el proceso actual. Una instalación simultánea no se puede ejecutar de forma asincrónica.

Vea Custom Action Return Processing Options ( Opciones de [procesamiento de devolución de acciones personalizadas).](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Las marcas de opciones están disponibles para controlar la posible ejecución múltiple de acciones personalizadas. Vea Custom Action Execution Scheduling Options ( Opciones [de programación de ejecución de acciones personalizadas).](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script de ejecución

Esta acción personalizada no usa esta opción.

## <a name="return-values"></a>Valores devueltos

El estado devuelto de la salida del usuario, el error, la suspensión o el éxito de una instalación simultánea se procesa de la misma manera que cualquier otra acción. Sin embargo, tenga Windows installer traduce los valores devueltos de todas las acciones cuando escribe el valor devuelto en el archivo de registro. Por ejemplo, si el valor devuelto de la acción aparece como 1 en el archivo de registro, significa que la acción devolvió ERROR \_ SUCCESS. Para obtener más información sobre esta traducción, vea [Registro de valores devueltos de acción](logging-of-action-return-values.md).

Tenga en cuenta que si una instalación simultánea tiene **msidbCustomActionTypeContinue** establecido, la devolución de ERROR \_ INSTALL \_ USEREXIT, ERROR INSTALL REBOOT, ERROR INSTALL REBOOT NOW o ERROR SUCCESS REBOOT REQUIRED se trata como \_ \_ ERROR \_ \_ \_ \_ \_ \_ \_ SUCCESS. Esto significa que si establece **msidbCustomActionTypeContinue** y la instalación simultánea requiere un reinicio, se omitirá el requisito para el reinicio. Además, se omitirá el código de error de la acción personalizada de instalación simultánea.

Si **no se establece msidbCustomActionTypeContinue,** los siguientes códigos de retorno más ERROR SUCCESS se tratan como correctos y tienen los \_ significados siguientes. Otros códigos de retorno se tratan como errores.



| Mensaje                          | Significado                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| ERROR \_ AL REINICIAR LA \_ INSTALACIÓN           | La marca de reinicio se establecerá para reiniciarse al final de la instalación.                                  |
| ERROR \_ AL INSTALAR EL REINICIO \_ \_ AHORA      | Es necesario reiniciar antes de completar la instalación. El reinicio se procesará inmediatamente. |
| ERROR \_ NECESARIO PARA REINICIAR \_ \_ CORRECTAMENTE | Se requiere un reinicio, pero se ha suprimido.                                                          |



 

## <a name="remarks"></a>Observaciones

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
</dt> <dt>

[Valores devueltos de acción personalizada](custom-action-return-values.md)
</dt> </dl>

 

 



