---
description: Todos los diccionarios de aplicación se implementan mediante el objeto de la forma de palabras.
ms.assetid: 805788ec-1672-462a-b188-c680f56c2641
title: Descripción de las listas de palabras, el contexto del reconocedor y Factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27f15d64f353b8702695b0067f13857427fc34e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277390"
---
# <a name="understanding-word-lists-recognizer-context-and-factoids"></a>Descripción de las listas de palabras, el contexto del reconocedor y Factoids

Todos los diccionarios de aplicación se implementan mediante el objeto de la forma de [**palabras**](inkwordlist-class.md) . El objeto [**RecognizerContext**](inkrecognizercontext-class.md) administra el reconocimiento, en parte a través de la propiedad de la referencia de [**palabras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) de ese objeto. El objeto **RecognizerContext** pasa la lista de palabras al reconocedor. Puede habilitar un diccionario de aplicación en cualquier **RecognizerContext** de la aplicación estableciendo la propiedad de la información de **palabras** del objeto **RecognizerContext** . Para que la lista de palabras esté disponible para toda la aplicación, debe establecer la propiedad lista de **palabras** de cada objeto **RecognizerContext** en la aplicación.

En el nivel de reconocedor, todos los diccionarios excepto el Diccionario del sistema se implementan como listas de palabras. Sin embargo, el reconocedor solo puede tener una lista de palabras activa a la vez. Esto significa que no puede tener un diccionario de aplicación y el Diccionario de usuarios activos al mismo tiempo. Por otro lado, el Diccionario del sistema siempre está disponible, a menos que se establezca un Factoid que desactive el Diccionario del sistema.

El Diccionario del usuario es la lista de palabras que el usuario ha agregado a su Tablet PC. Si no se establece la propiedad lista de [**palabras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del [**RecognizerContext**](inkrecognizercontext-class.md) , el **RecognizerContext** pasa el Diccionario del usuario como una lista de palabras al reconocedor. Sin embargo, si se establece la propiedad de lista de **palabras** del objeto **RecognizerContext** , se pasa la lista de palabras al reconocedor en lugar de al diccionario del usuario.

> [!Note]  
> La propiedad [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) del objeto [**RecognizerContext**](inkrecognizercontext-class.md) debe estar vacía antes de establecer la propiedad de la cadena de [**palabras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) . Si la propiedad **Strokes** no está vacía, se produce una excepción. Las palabras no deben agregarse nunca a una lista de palabras una vez que se han asignado a un objeto **RecognizerContext** .

 

La configuración de un Factoid en el objeto [**RecognizerContext**](inkrecognizercontext-class.md) también afecta al modo en que el reconocedor usa los diccionarios de aplicación. Los Factoids que afectan al comportamiento de los diccionarios son:

-   **Palabras**
-   **SystemDictionary**
-   **None**

Por el momento, el Factoid más útil para los diccionarios de aplicación es la Factoid de **palabras** . La lista de **palabras** Factoid sesga el reconocedor para devolver solo las palabras que se encuentran en la lista de palabras. Este Factoid desactiva todos los demás diccionarios excepto la lista de palabras. Si se establece la lista de **palabras** Factoid y no se especifica ninguna lista de palabras en el contexto del reconocedor, el Diccionario de usuario se utiliza como lista de palabras.

Por ejemplo, si está diseñando una aplicación de piezas de aviones con un campo que acepta uno de los diez nombres de partes especializadas, puede crear una lista de palabras que solo contenga estos nombres de partes. La configuración de la Factoid de **palabras** para el campo mejora considerablemente el reconocimiento de las palabras especificadas en ese campo. El Reconocedor no debe elegir entre palabras en el Diccionario del sistema y las palabras en la lista de palabras.

**SystemDictionary** Factoid solo habilita el Diccionario del sistema. El Factoid **None** deshabilita todos los diccionarios. Estos dos Factoids se usan para aumentar la precisión del reconocimiento en ciertos casos. Sin embargo, dado que deshabilitan los diccionarios de aplicación, rara vez se usan junto con los diccionarios de aplicación.

Para obtener más información sobre el modo en que Factoids afecta al reconocimiento, consulte [uso de contexto para mejorar la precisión](using-context-to-improve-accuracy.md).

Para obtener más información sobre **SystemDictionary** y **None** Factoids, consulte [Factoids compatible de la versión 1](supported-factoids-from-version-1.md).

 

 



