---
description: ICE84 comprueba la tabla AdvtExecuteSequence, la tabla AdminExecuteSequence y la tabla InstallExecuteSequence para comprobar que las siguientes acciones estándar no se han establecido con condiciones en el campo Condición.
ms.assetid: 0d1bbf4b-ffab-409e-a292-891dfa823433
title: ICE84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8960f53f5a01e9bec95a02bb3241487aa31aaae5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074523"
---
# <a name="ice84"></a>ICE84

ICE84 comprueba la [tabla AdvtExecuteSequence](advtexecutesequence-table.md), la tabla [AdminExecuteSequence](adminexecutesequence-table.md)y la tabla [](standard-actions.md) [InstallExecuteSequence](installexecutesequence-table.md) para comprobar que las siguientes acciones estándar no se han establecido con condiciones en el campo Condición.

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

Si se encuentran condiciones, ICE84 envía una advertencia.

## <a name="result"></a>Resultado

ICE84 publica la advertencia siguiente.



| Error ice84                                                             | Descripción                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| La acción \[ '1' \] que se encuentra en la tabla %s es una acción necesaria con una condición. | Se ha escrito una acción necesaria con una condición . |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



