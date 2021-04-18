---
title: DuplicateSiblingIDs
description: DuplicateSiblingIDs
ms.assetid: 942385A4-BD14-4046-9ABC-110B32D96BB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27ba2ccca45234bb49fc782c5522b4e446d77a2c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704809"
---
# <a name="duplicatesiblingids"></a>DuplicateSiblingIDs

## <a name="text"></a>Texto

El ID. de automatización duplicado \\ "" producirá {0} \\ ambigüedad entre los elementos.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Un elemento tiene el mismo ID. de automatización que otro elemento.

Este problema puede producir problemas de automatización que impiden que el código de prueba haga referencia al elemento correcto.

## <a name="possible-causes"></a>Causas posibles

-   Los elementos relacionados tienen el mismo identificador de automatización.
-   Implementación incorrecta de la propiedad AutomationId AutomationId.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement.CurrentAutomationId**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentautomationid)
</dt> </dl>

 

 




