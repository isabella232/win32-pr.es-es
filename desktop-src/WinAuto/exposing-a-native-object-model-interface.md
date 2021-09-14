---
title: Exponer una interfaz de modelo de objetos nativos
description: Si un elemento de interfaz de usuario admite un modelo de objetos nativo que no sea Microsoft Active Accessibility o Automatización de la interfaz de usuario, puede exponer la interfaz personalizada respondiendo a mensajes GETOBJECT de WM que incluyen el identificador de objeto \_ NATIVEOM de OBJID. \_
ms.assetid: 430abeaf-e5ca-48c4-aa35-8d52a8cee2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52543908e89a1cea57c981d60bf7cb2b9fbd1fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160571"
---
# <a name="exposing-a-native-object-model-interface"></a>Exponer una interfaz de modelo de objetos nativos

Si un elemento de interfaz de usuario admite un modelo de objetos nativo que no sea Microsoft Active Accessibility o Automatización de la interfaz de usuario, puede exponer la interfaz personalizada respondiendo a mensajes [**\_ GETOBJECT**](wm-getobject.md) de WM que incluyen el identificador de objeto [**\_ NATIVEOM de OBJID.**](object-identifiers.md) Para responder, el elemento de interfaz de usuario debe devolver el valor recuperado por una llamada a la [**función LresultFromObject.**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)

Un cliente puede recuperar una interfaz de un elemento de interfaz de usuario que admite un modelo de objetos nativo llamando a la [**función AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) y [**especificando OBJID \_ NATIVEOM**](object-identifiers.md) como segundo parámetro.

 

 




