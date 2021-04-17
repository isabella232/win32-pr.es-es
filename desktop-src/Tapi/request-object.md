---
description: El objeto de solicitud se crea mediante COM CoCreateInstance y expone una interfaz, ITRequest.
ms.assetid: 1e4c71ce-6846-4e64-9346-455ed82aa458
title: Objeto de solicitud
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51e81cae01f2624ba863b304c0a5f732b221199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677799"
---
# <a name="request-object"></a>Objeto de solicitud

El objeto de solicitud se crea mediante COM **CoCreateInstance** y expone una interfaz, [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest). Esta interfaz expone el método [**MakeCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) , que permite a una aplicación TAPI 3 usar la telefonía asistida. La telefonía asistida proporciona aplicaciones habilitadas para telefonía con un mecanismo sencillo para realizar llamadas telefónicas sin necesidad de que el desarrollador se convierta completamente en una llamada de telefonía.

Por ejemplo, una aplicación de hoja de cálculo puede Agregar un botón "make Call" con telefonía asistida sin implementar los controles más elaborados disponibles en una aplicación TAPI completa.

Consulte la [Introducción a la telefonía asistida](assisted-telephony-overview.md) para obtener información adicional.

 

 



