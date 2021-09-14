---
description: Las aplicaciones pueden escuchar eventos del sistema mediante el objeto InkCollector y escuchar el evento SystemGesture en él.
ms.assetid: 141afdbe-b5a7-47dc-b505-46089a5eda75
title: Escuchar eventos del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1429e652140cc9624d324401edef7817dad40ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256544"
---
# <a name="listening-to-system-events"></a>Escuchar eventos del sistema

Las aplicaciones pueden escuchar eventos del sistema mediante el objeto [**InkCollector**](inkcollector-class.md) y escuchar el [**evento SystemGesture**](inkcollector-systemgesture.md) en él. Puede establecer qué eventos escucha una aplicación. Cuando se produce una acción de lápiz de tableta, el evento **SystemGesture** correspondiente se envía a la aplicación en su **objeto InkCollector.** Una aplicación puede cancelar el mensaje del mouse que corresponde a un evento **SystemGesture** determinado cuando recibe el evento. Para obtener más información sobre cómo cancelar mensajes del mouse, vea **Evento SystemGesture.**

 

 



