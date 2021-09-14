---
description: Si no se establece la opción de procesamiento de devolución msidbCustomActionTypeContinue, la acción personalizada debe devolver un código de estado entero como se muestra en la tabla siguiente.
ms.assetid: 56c2d639-eef8-47cd-9d47-9a4781b9be36
title: Valores devueltos de acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c01ba6273aea6cf950edb56ef3c2a94ab9a272d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158714"
---
# <a name="custom-action-return-values"></a>Valores devueltos de acción personalizada

Si no se establece la opción de procesamiento de devolución **msidbCustomActionTypeContinue,** la acción personalizada debe devolver un código de estado entero como se muestra en la tabla siguiente.



| Valor devuelto                 | Descripción                           |
|------------------------------|---------------------------------------|
| FUNCIÓN DE \_ ERROR \_ NO \_ LLAMADA | Acción no ejecutada.                  |
| ERROR \_ CORRECTO               | Acciones completadas correctamente.       |
| ERROR \_ AL \_ INSTALAR USEREXIT     | El usuario finalizó prematuramente.          |
| ERROR DE \_ INSTALACIÓN \_      | Error irrecuperable.         |
| ERROR \_ NO \_ MÁS \_ ELEMENTOS       | Omita las acciones restantes, no un error. |



 

Tenga en cuenta que las acciones personalizadas [que son archivos ejecutables](executable-files.md) deben devolver un valor de 0 para que se ejecute correctamente. El instalador interpreta cualquier otro valor devuelto como error. Para omitir los valores devueltos, establezca la marca de bits **msidbCustomActionTypeContinue** en el campo Type de la [tabla CustomAction](customaction-table.md).

Para obtener más información sobre **la opción msidbCustomActionTypeContinue** y otras opciones de procesamiento de devolución, vea [Custom Action Return Processing Options](custom-action-return-processing-options.md).

Tenga en Windows instalador traduce los valores devueltos de todas las acciones cuando escribe el valor devuelto en el archivo de registro. Por ejemplo, si el valor devuelto de la acción aparece como 1 en el archivo de registro, significa que la acción devolvió ERROR \_ SUCCESS. Para obtener más información sobre esta traducción, vea [Registro de valores devueltos de acción](logging-of-action-return-values.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códigos de error](error-codes.md)
</dt> <dt>

[Registro de valores devueltos de acción](logging-of-action-return-values.md)
</dt> </dl>

 

 



