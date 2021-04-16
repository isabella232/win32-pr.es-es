---
description: La acción RMCCPSearch usa firmas de archivo para validar que los productos aptos se instalan en un sistema antes de realizar una instalación de actualización.
ms.assetid: d37b2434-86eb-4c6e-b817-77c75dcebbf5
title: Acción RMCCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c273ccb03bb77e0346edf73177d938d6002878a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677590"
---
# <a name="rmccpsearch-action"></a>Acción RMCCPSearch

La acción RMCCPSearch usa firmas de archivo para validar que los productos aptos se instalan en un sistema antes de realizar una instalación de actualización.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RMCCPSearch debe crearse en la [tabla InstallUISequence](installuisequence-table.md) y en la [tabla InstallExecuteSequence](installexecutesequence-table.md). El instalador impide que RMCCPSearch se ejecute en la secuencia InstallExecuteSequence si la acción ya se ejecutó en la secuencia InstallUISequence.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay mensajes ActionData.

## <a name="remarks"></a>Observaciones

La acción RMCCPSearch requiere que la propiedad de la [**\_ unidad de CCP**](ccp-drive.md) se establezca en la ruta de acceso raíz en el [*volumen*](v-gly.md) extraíble que tiene la instalación de cualquiera de los productos calificados.

Cada firma de archivo de la tabla CCPSearch se busca en la ruta de acceso a la que se hace referencia en la propiedad de la [**\_ unidad de CCP**](ccp-drive.md) mediante la tabla [DrLocator](drlocator-table.md) . La ausencia de la firma de la tabla [Signature](signature-table.md) denota un directorio. Si se determina que existe alguna firma, la acción RMCCPSearch finaliza.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla CCPSearch](ccpsearch-table.md)
</dt> </dl>

 

 



