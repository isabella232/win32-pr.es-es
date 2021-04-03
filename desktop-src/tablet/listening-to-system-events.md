---
description: Las aplicaciones pueden escuchar eventos del sistema mediante el objeto InkCollector y escuchando el evento SystemGesture en él.
ms.assetid: 141afdbe-b5a7-47dc-b505-46089a5eda75
title: Escuchar eventos del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1429e652140cc9624d324401edef7817dad40ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083402"
---
# <a name="listening-to-system-events"></a>Escuchar eventos del sistema

Las aplicaciones pueden escuchar eventos del sistema mediante el objeto [**InkCollector**](inkcollector-class.md) y escuchando el evento [**SystemGesture**](inkcollector-systemgesture.md) en él. Puede establecer los eventos a los que escuchará una aplicación. Cuando se produce una acción del lápiz de Tablet PC, el evento **SystemGesture** correspondiente se envía a la aplicación en su objeto **InkCollector** . Una aplicación puede cancelar el mensaje del mouse que corresponde a un evento **SystemGesture** determinado cuando recibe el evento. Para obtener más información sobre cómo cancelar los mensajes del mouse, vea evento **SystemGesture** .

 

 



