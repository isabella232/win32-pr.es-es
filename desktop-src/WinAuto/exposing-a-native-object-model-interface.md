---
title: Exponer una interfaz de modelo de objetos nativos
description: Si un elemento de interfaz de usuario admite un modelo de objetos nativo que no sea Microsoft Active Accessibility o Automatización de la interfaz de usuario, puede exponer la interfaz personalizada respondiendo a mensajes GETOBJECT de WM que incluyen el identificador de objeto \_ OBJID \_ NATIVEOM.
ms.assetid: 430abeaf-e5ca-48c4-aa35-8d52a8cee2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701ed721e8259aa3b707fa1d7a6f2e80b9da13a3760b9850edef22b169d772e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644925"
---
# <a name="exposing-a-native-object-model-interface"></a>Exponer una interfaz de modelo de objetos nativos

Si un elemento de interfaz de usuario admite un modelo de objetos nativo distinto de Microsoft Active Accessibility o Automatización de la interfaz de usuario, puede exponer la interfaz personalizada respondiendo a mensajes [**\_ GETOBJECT**](wm-getobject.md) de WM que incluyen el identificador de objeto [**OBJID \_ NATIVEOM.**](object-identifiers.md) Para responder, el elemento de la interfaz de usuario debe devolver el valor recuperado por una llamada a la [**función LresultFromObject.**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)

Un cliente puede recuperar una interfaz de un elemento de interfaz de usuario que admite un modelo de objetos nativo llamando a la función [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) y especificando [**OBJID \_ NATIVEOM como**](object-identifiers.md) segundo parámetro.

 

 




