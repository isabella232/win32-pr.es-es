---
description: Si no se establece la opción de procesamiento de devoluciones msidbCustomActionTypeContinue, la acción personalizada debe devolver un código de estado entero, tal como se muestra en la tabla siguiente.
ms.assetid: 56c2d639-eef8-47cd-9d47-9a4781b9be36
title: Valores devueltos de la acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c01ba6273aea6cf950edb56ef3c2a94ab9a272d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669849"
---
# <a name="custom-action-return-values"></a>Valores devueltos de la acción personalizada

Si no se establece la opción de procesamiento de devoluciones **msidbCustomActionTypeContinue** , la acción personalizada debe devolver un código de estado entero, tal como se muestra en la tabla siguiente.



| Valor devuelto                 | Descripción                           |
|------------------------------|---------------------------------------|
| función de ERROR \_ \_ no \_ llamada | Acción no ejecutada.                  |
| ERROR \_ correcto               | Acciones completadas correctamente.       |
| ERROR al \_ instalar \_ USEREXIT     | El usuario terminó prematuramente.          |
| ERROR de instalación de ERROR \_ \_      | Se produjo un error irrecuperable.         |
| \_no hay \_ más \_ elementos de error       | Omitir las acciones restantes, no un error. |



 

Tenga en cuenta que las acciones personalizadas que son [archivos ejecutables](executable-files.md) deben devolver un valor de 0 para que se ejecute correctamente. El instalador interpreta cualquier otro valor devuelto como error. Para omitir los valores devueltos, establezca la marca de bits **msidbCustomActionTypeContinue** en el campo Type de la [tabla CustomAction](customaction-table.md).

Para obtener más información sobre la opción **msidbCustomActionTypeContinue** y otras opciones de procesamiento de valores devueltos, vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).

Tenga en cuenta que Windows Installer traduce los valores devueltos de todas las acciones cuando escribe el valor devuelto en el archivo de registro. Por ejemplo, si el valor devuelto de la acción aparece como 1 en el archivo de registro, significa que la acción devolvió un ERROR de \_ éxito. Para obtener más información sobre esta traducción, consulte [registro de valores devueltos de acciones](logging-of-action-return-values.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códigos de error](error-codes.md)
</dt> <dt>

[Registro de valores devueltos de acción](logging-of-action-return-values.md)
</dt> </dl>

 

 



