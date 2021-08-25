---
description: Todos los diccionarios de aplicaciones se implementan mediante el objeto WordList.
ms.assetid: 805788ec-1672-462a-b188-c680f56c2641
title: Descripción de las listas de palabras, el contexto del reconocedor y factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60fbfc7a3a3099a1146307637d20e777cca416789a61f5dd034f9d86911f1a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842815"
---
# <a name="understanding-word-lists-recognizer-context-and-factoids"></a>Descripción de las listas de palabras, el contexto del reconocedor y factoids

Todos los diccionarios de aplicaciones se implementan mediante el [**objeto WordList.**](inkwordlist-class.md) El [**objeto RecognizerContext**](inkrecognizercontext-class.md) administra el reconocimiento, en parte a través de la propiedad [**WordList de ese**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) objeto. El **objeto RecognizerContext** pasa la lista de palabras al reconocedor. Puede habilitar un diccionario de aplicaciones en **cualquier RecognizerContext** de la aplicación estableciendo la **propiedad WordList** del **objeto RecognizerContext.** Para que la lista de palabras esté disponible para toda la aplicación, debe establecer la **propiedad WordList** de cada objeto **RecognizerContext** de la aplicación.

En el nivel de reconocedor, todos los diccionarios excepto el diccionario del sistema se implementan como listas de palabras. Sin embargo, el reconocedor solo puede tener una lista de palabras activa a la vez. Esto significa que no puede tener un diccionario de aplicaciones y el diccionario de usuarios activos al mismo tiempo. Por otro lado, el diccionario del sistema siempre está disponible, a menos que se establezca un factoid que apague el diccionario del sistema.

El diccionario de usuarios es la lista de palabras que el usuario ha agregado a su tablet PC. Si no se establece la propiedad [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) de [**RecognizerContext,**](inkrecognizercontext-class.md) **RecognizerContext** pasa el diccionario de usuarios como una lista de palabras al reconocedor. Sin embargo, si se establece la propiedad **WordList** del objeto **RecognizerContext,** la lista de palabras se pasa al reconocedor en lugar del diccionario de usuarios.

> [!Note]  
> La [**propiedad Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) del [**objeto RecognizerContext**](inkrecognizercontext-class.md) debe estar vacía antes de establecer la [**propiedad WordList.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) Si la **propiedad Strokes** no está vacía, se produce una excepción. Las palabras nunca se deben agregar a una lista de palabras después de que se haya asignado a un **objeto RecognizerContext.**

 

Establecer un factoid en [**el objeto RecognizerContext**](inkrecognizercontext-class.md) también afecta al modo en que el reconocedor usa los diccionarios de aplicaciones. Los factoids que afectan al comportamiento de los diccionarios son:

-   **WordList**
-   **SystemDictionary**
-   **None**

Con diferencia, el factoid más útil para los diccionarios de aplicaciones es **el factoid WordList.** El **factoid WordList** sesgo el reconocedor para devolver solo las palabras encontradas en la lista de palabras. Este factoid desactiva todos los demás diccionarios, excepto la lista de palabras. Si se establece el factoid **WordList** y no se especifica ninguna lista de palabras en el contexto del reconocedor, el diccionario de usuarios se usa como la lista de palabras.

Por ejemplo, si va a diseñar una aplicación de piezas de avión con un campo que acepta uno de los diez nombres de partes especializadas, puede crear una lista de palabras que contenga solo estos nombres de partes. Establecer el **factoid WordList** para el campo mejora considerablemente el reconocimiento de las palabras especificadas en ese campo. El reconocedor no necesita elegir entre las palabras del diccionario del sistema y las palabras de la lista de palabras.

El **factoid SystemDictionary** habilita solo el diccionario del sistema. El **factoid None** deshabilita todos los diccionarios. Estos dos factoids se usan para aumentar la precisión del reconocimiento en determinadas instancias. Sin embargo, dado que deshabilitan los diccionarios de aplicaciones, rara vez se usan junto con los diccionarios de aplicaciones.

Para obtener más información sobre cómo afectan los factoids al reconocimiento, vea [Usar contexto para mejorar la precisión.](using-context-to-improve-accuracy.md)

Para obtener más información sobre **los factoids SystemDictionary** y **None,** vea [Supported Factoids from Version 1](supported-factoids-from-version-1.md).

 

 



