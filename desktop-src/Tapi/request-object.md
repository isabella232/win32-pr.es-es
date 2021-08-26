---
description: El objeto Request se crea mediante COM CoCreateInstance y expone una interfaz, ITRequest.
ms.assetid: 1e4c71ce-6846-4e64-9346-455ed82aa458
title: Objeto Request
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcf6da101c3642ffe31b05efb18279a79bcfc28ed24af7a959f3275d9cbc4f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905895"
---
# <a name="request-object"></a>Objeto Request

El objeto Request se crea mediante COM **CoCreateInstance** y expone una interfaz, [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest). Esta interfaz expone el [**método MakeCall,**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) que permite que una aplicación TAPI 3 use la telefonía asistida. La telefonía asistida proporciona a las aplicaciones habilitadas para telefonía un mecanismo sencillo para realizar llamadas telefónicas sin necesidad de que el desarrollador se convierta en un fabricante completo de telefonía.

Por ejemplo, una aplicación de hoja de cálculo puede agregar un botón "Realizar llamada" mediante la telefonía asistida sin implementar los controles más elaborados disponibles en una aplicación TAPI completa.

Consulte La introducción [a la telefonía asistida](assisted-telephony-overview.md) para obtener información adicional.

 

 



