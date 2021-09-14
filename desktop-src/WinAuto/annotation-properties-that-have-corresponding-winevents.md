---
title: Propiedades de anotación que tienen winEvents correspondientes
description: Tenga cuidado al reemplazar las propiedades que cambian con frecuencia, especialmente las que examinan los clientes como resultado de un winEvent (como State, Value y, para algunos controles, las propiedades Name).
ms.assetid: 2505d015-9381-4e1c-a10f-6db3fbb25ca3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a8849c66cb0067b63be1c846e9e140ae06f4b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070716"
---
# <a name="annotation-properties-that-have-corresponding-winevents"></a>Propiedades de anotación que tienen winEvents correspondientes

Tenga cuidado al invalidar las propiedades que cambian con frecuencia, especialmente las que examinan los clientes como resultado de un winEvent (como [**State**](state-property.md), [**Value**](value-property.md)y, para algunos controles, las propiedades [**Name).**](name-property.md)

En muchos casos, especialmente para los controles USER y ComCtl, el winEvent que señala un cambio de propiedad se envía antes de que se notifique al propietario del control (normalmente a través de [WM \_ NOTIFY](../controls/wm-notify.md)). La actualización de la propiedad [**mediante SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) en el controlador WM NOTIFY será demasiado tarde; los clientes que usan el enlace en contexto ya tendrán acceso \_ al valor anterior.

Puede controlar estos tipos de propiedades mediante objetos de servidor de devolución de llamada (mediante [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)); sin embargo, el servidor no puede usar ningún estado actualizado en el controlador WM NOTIFY porque aún no se habrá \_ llamado a ese controlador. Por ejemplo, en lugar de usar una variable de valor actual almacenada en caché que se actualiza en el controlador WM NOTIFY y que estará desactualizado, el objeto de devolución de llamada \_ [**IAccPropServer::GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) debe enviar un mensaje directamente al control para obtener su verdadero valor actual para generar la propiedad necesaria.

 

 