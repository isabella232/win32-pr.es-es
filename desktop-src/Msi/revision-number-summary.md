---
description: Para un paquete de instalación, la propiedad Resumen del número de revisión contiene el código del paquete del instalador.
ms.assetid: 79702b44-846a-4672-8e22-9b6e3f4b4678
title: Propiedad Resumen del número de revisión
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b11371c4a431322fd7ceca7fd645fc8eb8bea47688b740340e973507271f6a25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869065"
---
# <a name="revision-number-summary-property"></a>Propiedad Resumen del número de revisión

Para un paquete de instalación, la **propiedad Resumen del número de revisión** contiene el código del [*paquete*](p-gly.md) del instalador. Para obtener más información sobre los códigos de paquete, vea [Códigos de paquete .](package-codes.md)

Para una transformación, la propiedad **Resumen** del número de revisión enumera los GUID del código de producto y la versión de los productos nuevos y originales, así como el GUID del código de actualización. La lista se separa con punto y coma como se muestra a continuación.

"Original-Product-Code Original-Product-Version ; New-Product code New-Product-Version; Upgrade-Code"

Para un paquete de revisión, la **propiedad Resumen** del número de revisión especifica el código de revisión GUID para la revisión. Esto puede ir seguido de una lista de GUID de código de revisión para las revisiones obsoletas que se van a quitar cuando se aplica esta revisión. Los códigos de revisión se concatenan sin delimitadores que separan los GUID de la lista.

**Windows Installer 3.0: ** Si hay información de secuenciación presente en la tabla [MsiPatchSequence](msipatchsequence-table.md), Windows Installer 3.0 usa la información de secuenciación de la tabla y omite la lista de revisiones obsoletas incluidas en la propiedad **Resumen** del número de revisión. Windows El instalador 3.0 todavía puede usar la información de revisión obsoleta en la propiedad **Resumen** del número de revisión si el paquete no contiene una tabla MsiPatchSequence.

**Windows Installer 2.0: ** No se admite la tabla [MsiPatchSequence.](msipatchsequence-table.md) Windows El instalador 2.0 todavía puede usar la información de revisión obsoleta en la propiedad **Resumen** del número de revisión si el paquete no contiene una tabla MsiPatchSequence.

Esta propiedad de resumen es obligatoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Descripciones de propiedades de resumen](summary-property-descriptions.md)
</dt> </dl>

 

 




