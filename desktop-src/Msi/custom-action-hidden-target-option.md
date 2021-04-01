---
description: Utilice las siguientes marcas de opciones para especificar que el instalador no escriba el valor especificado en el campo de destino de la tabla CustomAction en el registro. Para establecer la opción, agregue el valor de esta tabla al valor del campo Type de la tabla CustomAction.
ms.assetid: b0f99851-a774-4804-8c85-f94943c2d2b0
title: Opción de destino oculto de acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acca69e4c3efc2b43302bf926a56bc53b2bf5e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082789"
---
# <a name="custom-action-hidden-target-option"></a>Opción de destino oculto de acción personalizada

Utilice las siguientes marcas de opciones para especificar que el instalador no escriba el valor especificado en el campo de destino de la [tabla CustomAction](customaction-table.md) en el registro. Para establecer la opción, agregue el valor de esta tabla al valor del campo Type de la tabla CustomAction.



| Constante                            | Hexadecimal | Decimal | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (ninguno)                              | 0x0000      | 0       | El instalador puede escribir el valor en la columna de destino de la tabla CustomAction en el archivo de registro.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **msidbCustomActionTypeHideTarget** | 0x2000      | 8192    | No se impide que el instalador escriba el valor en la columna de destino de la [tabla CustomAction](customaction-table.md) en el archivo de registro. La propiedad CustomActionData tampoco se registra cuando el instalador ejecuta la acción personalizada.<br/> Dado que el instalador establece el valor de CustomActionData desde una propiedad con el mismo nombre que la acción personalizada, dicha propiedad debe aparecer en la propiedad [**MsiHiddenProperties**](msihiddenproperties.md) para evitar que su valor aparezca en el registro.<br/> |



 

Para obtener más información, consulte [impedir que se escriba información confidencial en el archivo de registro](preventing-confidential-information-from-being-written-into-the-log-file.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de acción personalizada](custom-action-reference.md)
</dt> <dt>

[Acerca de las acciones personalizadas](about-custom-actions.md)
</dt> <dt>

[Uso de acciones personalizadas](using-custom-actions.md)
</dt> </dl>

 

 




