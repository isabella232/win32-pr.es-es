---
description: Secuencias de acciones sugeridas para una tabla Básica AdminUISequence en una base de Windows installer.
ms.assetid: a5371133-7d55-4041-8e1f-ecc8245c8d3a
title: AdminUISequence sugerido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40a38958bac2be283a43054f6b2ab8d0473f0ecf3646e259f872c4336c0e5aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627165"
---
# <a name="suggested-adminuisequence"></a>AdminUISequence sugerido



| Acción                                      | Condición | Secuencia |
|---------------------------------------------|-----------|----------|
| FatalErrorDlg                               |           | -3       |
| UserExitDlg                                 |           | -2       |
| ExitDlg                                     |           | -1       |
| PrepareDlg                                  |           | 140      |
| [CostInitialize](costinitialize-action.md) |           | 800      |
| [FileCost](filecost-action.md)             |           | 900      |
| [CostFinalize](costfinalize-action.md)     |           | 1000     |
| AdminWelcomeDlg                             |           | 1230     |
| ProgressDlg                                 |           | 1280     |
| [ExecuteAction](executeaction-action.md)   |           | 1300     |



 

 

 



