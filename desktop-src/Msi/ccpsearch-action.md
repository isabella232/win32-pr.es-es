---
description: La acción CCPSearch usa firmas de archivo para validar que los productos aptos están instalados en un sistema antes de realizar una instalación de actualización.
ms.assetid: 0aa7bf8b-de76-464d-8e7b-3aa4f609fe19
title: Acción CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 201af22dd557541825dcf2c47f06e7cf67cd8785fa85e0b78a28c25a570ffc89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145698"
---
# <a name="ccpsearch-action"></a>Acción CCPSearch

La acción CCPSearch usa firmas de archivo para validar que los productos aptos están instalados en un sistema antes de realizar una instalación de actualización.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción CCPSearch debe crearse en la [tabla InstallUISequence](installuisequence-table.md) y en la [tabla InstallExecuteSequence](installexecutesequence-table.md). El instalador impide que la acción CCPSearch se ejecute en la secuencia InstallExecuteSequence si la acción ya se ha ejecutado en la secuencia InstallUISequence. La acción CCPSearch debe ir antes de [la acción RMCCPSearch.](rmccpsearch-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Comentarios

La acción CCPSearch busca firmas de archivo enumeradas en la tabla CCPSearch del sistema mediante las siguientes tablas en orden: Signature, CompLocator, RegLocator, IniLocator y DrLocator.

Si se determina que existe alguna firma, la propiedad **CCP \_ Success** se establece en 1 y la acción CCPSearch finaliza.

La ausencia de la firma de la tabla Firma denota un directorio.

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

 

 



