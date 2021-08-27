---
title: Interacción con WinEvents
description: El tiempo de ejecución de la anotación dinámica no enviará WinEvents; Es responsabilidad del anotador enviar los eventos adecuados, cuando sea necesario. Si necesita enviar WinEvents, asegúrese de enviarlos una vez realizada la anotación.
ms.assetid: 657a540b-8838-4d2e-ade6-c4fa1ad08e21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1789a152ab37161e1f217639e4ad40d597b0689529da3a5f65bf669b986e14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098465"
---
# <a name="interaction-with-winevents"></a>Interacción con WinEvents

El tiempo de ejecución de la anotación dinámica no enviará [WinEvents](winevents-infrastructure.md); Es responsabilidad del anotador enviar los eventos adecuados, cuando sea necesario. Si necesita enviar WinEvents, asegúrese de enviarlos una vez realizada la anotación.

Por ejemplo, si usa [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) para establecer la propiedad [**Name**](name-property.md) de un elemento, envíe un evento [**EVENT OBJECT \_ \_ NAMECHANGE**](event-constants.md) para ese objeto después de que se devuelva **SetPropValue.**

Sin embargo, si usa [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) para establecer ValueMap para un control deslizante, no se requiere ningún evento porque al establecer valueMap no se cambia el valor del control deslizante.

 

 




