---
description: La acción CCPSearch usa firmas de archivo para validar que los productos aptos se instalan en un sistema antes de realizar una instalación de actualización.
ms.assetid: 0aa7bf8b-de76-464d-8e7b-3aa4f609fe19
title: Acción CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8b1f01462ac0ba9dcf8838b9a043d95aef8cefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652596"
---
# <a name="ccpsearch-action"></a>Acción CCPSearch

La acción CCPSearch usa firmas de archivo para validar que los productos aptos se instalan en un sistema antes de realizar una instalación de actualización.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción CCPSearch debe crearse en la [tabla InstallUISequence](installuisequence-table.md) y en la [tabla InstallExecuteSequence](installexecutesequence-table.md). El instalador impide que la acción CCPSearch se ejecute en la secuencia InstallExecuteSequence si la acción ya se ejecutó en la secuencia InstallUISequence. La acción CCPSearch debe ser anterior a la acción [RMCCPSearch](rmccpsearch-action.md) .

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay mensajes ActionData.

## <a name="remarks"></a>Observaciones

La acción CCPSearch busca las firmas de archivo enumeradas en la tabla CCPSearch del sistema con las tablas siguientes en orden: Signature, CompLocator, RegLocator, IniLocator y DrLocator.

Si se determina que existe alguna firma, la propiedad de **\_ éxito de CCP** se establece en 1 y la acción CCPSearch finaliza.

La ausencia de la firma de la tabla Signature denota un directorio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[CCPSearch](ccpsearch-table.md)
</dt> <dt>

[Signature](signature-table.md)
</dt> <dt>

[CompLocator](complocator-table.md)
</dt> <dt>

[RegLocator](reglocator-table.md)
</dt> <dt>

[IniLocator](inilocator-table.md)
</dt> <dt>

[DrLocator](drlocator-table.md)
</dt> </dl>

 

 



