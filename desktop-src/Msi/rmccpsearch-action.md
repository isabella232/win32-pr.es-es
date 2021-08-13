---
description: La acción RMCCPSearch usa firmas de archivo para validar que los productos aptos se instalan en un sistema antes de realizar una instalación de actualización.
ms.assetid: d37b2434-86eb-4c6e-b817-77c75dcebbf5
title: Acción RMCCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d18431a6806d055c824bf51331d6390a6f669100aa9a33db9665b9d7b37008c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625905"
---
# <a name="rmccpsearch-action"></a>Acción RMCCPSearch

La acción RMCCPSearch usa firmas de archivo para validar que los productos aptos se instalan en un sistema antes de realizar una instalación de actualización.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RMCCPSearch debe crearse en la [tabla InstallUISequence](installuisequence-table.md) y [en la tabla InstallExecuteSequence](installexecutesequence-table.md). El instalador impide que RMCCPSearch se ejecute en la secuencia InstallExecuteSequence si la acción ya se ha ejecutado en la secuencia InstallUISequence.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Observaciones

La acción RMCCPSearch requiere que la propiedad [**CCP \_ DRIVE**](ccp-drive.md) se [](v-gly.md) establezca en la ruta de acceso raíz del volumen extraíble que tiene la instalación para cualquiera de los productos aptos.

Cada firma de archivo de la tabla CCPSearch se busca en la ruta de acceso a la que hace referencia la propiedad [**CCP \_ DRIVE**](ccp-drive.md) mediante la [tabla DrLocator.](drlocator-table.md) La ausencia de la firma de la [tabla Firma](signature-table.md) denota un directorio. Si se determina que existe alguna firma, la acción RMCCPSearch finaliza.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla CCPSearch](ccpsearch-table.md)
</dt> </dl>

 

 



