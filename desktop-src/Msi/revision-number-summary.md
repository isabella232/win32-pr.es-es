---
description: Para un paquete de instalación, la propiedad Resumen del número de revisión contiene el código del paquete del instalador.
ms.assetid: 79702b44-846a-4672-8e22-9b6e3f4b4678
title: Propiedad de Resumen de número de revisión
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e97df1eafec2d543be0f975b9f5daca7728267b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653907"
---
# <a name="revision-number-summary-property"></a>Propiedad de Resumen de número de revisión

Para un paquete de instalación, la propiedad **Resumen del número de revisión** contiene el código del [*paquete*](p-gly.md) del instalador. Para obtener más información sobre los códigos de paquete, consulte [códigos de paquete](package-codes.md).

En el caso de una transformación, la propiedad **Resumen del número de revisión** muestra los GUID de código de producto y la versión de los productos nuevos y originales y el GUID del código de actualización. La lista está separada por signos de punto y coma como se indica a continuación.

"Original-Product-Code original-Product-version; New-Product Code New-Product-version; Upgrade-Code "

En el caso de un paquete de revisión, la propiedad **Resumen del número de revisión** especifica el código de revisión del GUID para la revisión. Puede ir seguido de una lista de GUID de código de revisión para las revisiones obsoletas que se van a quitar cuando se aplica esta revisión. Los códigos de revisión se concatenan sin delimitadores que separan los GUID de la lista.

* * Windows Installer 3,0: * * si hay información de secuenciación presente en la [tabla MsiPatchSequence](msipatchsequence-table.md), Windows Installer 3,0 usa la información de secuenciación de la tabla y omite la lista de revisiones obsoletas incluidas en la propiedad **Resumen de número de revisión** . Windows Installer 3,0 puede seguir usando la información de revisión obsoleta en la propiedad **Resumen de número de revisión** si el paquete no contiene una tabla MsiPatchSequence.

* * Windows Installer 2,0: * * no se admite la [tabla MsiPatchSequence](msipatchsequence-table.md) . Windows Installer 2,0 puede seguir usando la información de revisión obsoleta en la propiedad **Resumen de número de revisión** si el paquete no contiene una tabla MsiPatchSequence.

Esta propiedad de resumen es obligatoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Descripciones de propiedades de Resumen](summary-property-descriptions.md)
</dt> </dl>

 

 




