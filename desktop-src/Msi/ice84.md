---
description: ICE84 comprueba la tabla AdvtExecuteSequence, la tabla AdminExecuteSequence y la tabla InstallExecuteSequence para comprobar que no se han establecido las siguientes acciones estándar con condiciones en el campo condición.
ms.assetid: 0d1bbf4b-ffab-409e-a292-891dfa823433
title: ICE84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8960f53f5a01e9bec95a02bb3241487aa31aaae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361154"
---
# <a name="ice84"></a>ICE84

ICE84 comprueba la tabla [AdvtExecuteSequence](advtexecutesequence-table.md), la [tabla AdminExecuteSequence](adminexecutesequence-table.md)y la [tabla InstallExecuteSequence](installexecutesequence-table.md) para comprobar que no se han establecido las siguientes [acciones estándar](standard-actions.md) con condiciones en el campo condición.

-   [Acción CostInitialize](costinitialize-action.md)
-   [Acción CostFinalize](costfinalize-action.md)
-   [Acción FileCost](filecost-action.md)
-   [Acción InstallValidate](installvalidate-action.md)
-   [Acción InstallInitialize](installinitialize-action.md)
-   [Acción InstallFinalize](installfinalize-action.md)
-   [Acción ProcessComponents](processcomponents-action.md)
-   [Acción PublishFeatures](publishfeatures-action.md)
-   [Acción PublishProduct](publishproduct-action.md)
-   [Acción RegisterProduct](registerproduct-action.md)
-   [Acción UnpublishFeatures](unpublishfeatures-action.md)

Si se encuentran condiciones, ICE84 publica una advertencia.

## <a name="result"></a>Resultado

ICE84 envía la siguiente advertencia.



| Error ICE84                                                             | Descripción                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| La acción ' \[ 1 ' que se \] encuentra en la tabla% s es una acción necesaria con una condición. | Se ha creado una acción necesaria con una condición. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



