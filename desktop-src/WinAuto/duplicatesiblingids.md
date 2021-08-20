---
title: DuplicateSiblingIDs
description: DuplicateSiblingIDs
ms.assetid: 942385A4-BD14-4046-9ABC-110B32D96BB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd9bb311d4aafdf1f509d3404cfe057f96f6bf378b822f6f77cab4943cea097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115362"
---
# <a name="duplicatesiblingids"></a>DuplicateSiblingIDs

## <a name="text"></a>Texto

El id. de automatización \\ duplicado " {0} \\ " provocará ambigüedad entre los elementos.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Un elemento tiene el mismo identificador de Automation que otro elemento.

Este problema puede causar problemas de automatización que impiden que el código de prueba haga referencia al elemento correcto.

## <a name="possible-causes"></a>Causas posibles

-   Los elementos del mismo nivel tienen el mismo identificador de Automation.
-   Implementación incorrecta de la propiedad AutomationId de UIA.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement.CurrentAutomationId**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentautomationid)
</dt> </dl>

 

 




