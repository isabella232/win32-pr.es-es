---
title: Exponer una interfaz del modelo de objetos nativos
description: Si un elemento de la interfaz de usuario admite un modelo de objetos nativo que no sea Microsoft Active Accessibility o la automatización de la interfaz de usuario, puede exponer la interfaz personalizada respondiendo a \_ los mensajes de WM GETOBJECT que incluyen el \_ identificador de objeto OBJID NATIVEOM.
ms.assetid: 430abeaf-e5ca-48c4-aa35-8d52a8cee2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52543908e89a1cea57c981d60bf7cb2b9fbd1fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075952"
---
# <a name="exposing-a-native-object-model-interface"></a>Exponer una interfaz del modelo de objetos nativos

Si un elemento de la interfaz de usuario admite un modelo de objetos nativo que no sea Microsoft Active Accessibility o la automatización de la interfaz de usuario, puede exponer la interfaz personalizada respondiendo a los mensajes de [**WM \_ GETOBJECT**](wm-getobject.md) que incluyen el identificador de objeto [**OBJID \_ NATIVEOM**](object-identifiers.md) . Para responder, el elemento de la interfaz de usuario debe devolver el valor recuperado por una llamada a la función [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .

Un cliente puede recuperar una interfaz de un elemento de la interfaz de usuario que admita un modelo de objetos nativo llamando a la función [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) y especificando [**OBJID \_ NATIVEOM**](object-identifiers.md) como segundo parámetro.

 

 




