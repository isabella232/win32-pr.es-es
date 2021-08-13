---
description: Use las siguientes marcas de opción para especificar que el instalador no escriba el valor especificado en el campo Destino de la tabla CustomAction en el registro. Para establecer la opción, agregue el valor de esta tabla al valor del campo Tipo de la tabla CustomAction.
ms.assetid: b0f99851-a774-4804-8c85-f94943c2d2b0
title: Opción de destino oculto de acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1adc0df477510ac7d5d6bec65025b6fed1bfd7971e6ddf35da3a7e4cbc714690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638168"
---
# <a name="custom-action-hidden-target-option"></a>Opción de destino oculto de acción personalizada

Use las siguientes marcas de opción para especificar que el instalador no escriba el valor especificado en el campo Destino de la [tabla CustomAction](customaction-table.md) en el registro. Para establecer la opción, agregue el valor de esta tabla al valor del campo Tipo de la tabla CustomAction.



| Constante                            | Hexadecimal | Decimal | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (ninguno)                              | 0x0000      | 0       | El instalador puede escribir el valor de la columna Target de la tabla CustomAction en el archivo de registro.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **msidbCustomActionTypeHideTarget** | 0x2000      | 8192    | Se impide que el instalador escriba el valor de la columna Target de la [tabla CustomAction](customaction-table.md) en el archivo de registro. La propiedad CustomActionData tampoco se registra cuando el instalador ejecuta la acción personalizada.<br/> Dado que el instalador establece el valor de CustomActionData de una propiedad con el mismo nombre que la acción personalizada, esa propiedad debe aparecer en la propiedad [**MsiHiddenProperties**](msihiddenproperties.md) para evitar que su valor aparezca en el registro.<br/> |



 

Para obtener más información, vea [Impedir que se escriba información confidencial en el archivo de registro.](preventing-confidential-information-from-being-written-into-the-log-file.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de acción personalizada](custom-action-reference.md)
</dt> <dt>

[Acerca de las acciones personalizadas](about-custom-actions.md)
</dt> <dt>

[Uso de acciones personalizadas](using-custom-actions.md)
</dt> </dl>

 

 




