---
description: ICE84 comprueba la tabla AdvtExecuteSequence, la tabla AdminExecuteSequence y la tabla InstallExecuteSequence para comprobar que las siguientes acciones estándar no se han establecido con condiciones en el campo Condición.
ms.assetid: 0d1bbf4b-ffab-409e-a292-891dfa823433
title: ICE84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2af31c343db973481bd69599fadc9c632bbc6dc58a473a69015b3eb0fbe781d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895005"
---
# <a name="ice84"></a>ICE84

ICE84 comprueba la tabla [](standard-actions.md) [AdvtExecuteSequence,](advtexecutesequence-table.md)la tabla [AdminExecuteSequence](adminexecutesequence-table.md)y la tabla [InstallExecuteSequence](installexecutesequence-table.md) para comprobar que las siguientes acciones estándar no se han establecido con condiciones en el campo Condición.

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



| Error ICE84                                                             | Descripción                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| La acción \[ '1' \] que se encuentra en la tabla %s es una acción necesaria con una condición. | Se ha escrito una acción necesaria con una condición . |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



