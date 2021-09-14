---
description: De forma predeterminada, el reconocedor usa un diccionario del sistema que contiene todas las palabras escritas habitualmente en un idioma.
ms.assetid: 2ddf04dd-613b-4570-9474-0e33208c4012
title: Uso de diccionarios de aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dfda443a688af9dfcec44a81f0e5ed2d50846c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267591"
---
# <a name="using-application-dictionaries"></a>Uso de diccionarios de aplicaciones

De forma predeterminada, el reconocedor usa un diccionario del sistema que contiene todas las palabras escritas habitualmente en un idioma. Además, el reconocedor tiene un diccionario de usuarios que contiene palabras que el usuario ha agregado al diccionario. Los usuarios agregan una palabra al diccionario de usuarios a través del Panel de entrada de Tablet PC mediante selecciones en:

-   Lista alternativa (al escribir).
-   Menú Herramientas de voz (al hablar).

Si va a diseñar una aplicación en la que prevé que el usuario escribirá palabras que no se encuentran en el diccionario del sistema o en el diccionario de usuarios, cree un diccionario de aplicaciones. Un diccionario de aplicaciones mejora aún más la precisión del reconocimiento al proporcionar al reconocedor una lista personalizada adicional de palabras que probablemente se escribirán como escritura a mano en una aplicación.

Para crear un diccionario de aplicaciones, use el [**objeto WordList.**](inkwordlist-class.md) El diccionario de aplicación siguiente aumenta la precisión del reconocimiento al proporcionar al reconocedor una lista de palabras esperadas. Por ejemplo, un diccionario de aplicaciones que contiene terminología médica aumenta la precisión del reconocimiento dentro de una aplicación desarrollada para el sector médico en el que es probable que se escriban los términos.

Como otro ejemplo, al diseñar un formulario para que alguien ordene instrumentación, cree un objeto [**WordList**](inkwordlist-class.md) que contenga los nombres de los fabricantes de instrumentación más comunes. Establezca la [**propiedad WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del [**objeto RecognizerContext**](inkrecognizercontext-class.md) en el **objeto WordList** que ha creado. A continuación, el objeto **RecognizerContext** pasa esta lista de palabras al reconocedor. El diccionario de aplicaciones aumenta la precisión del reconocimiento cuando esos nombres se escriben en un campo de la aplicación.

En los temas siguientes se describe cómo usar diccionarios de aplicaciones.

-   [Descripción de las listas de palabras, el contexto del reconocedor y factoids](understanding-wordlists--the-recognizercontext--and-factoids.md)
-   [Uso de diccionarios de aplicaciones con las API de la plataforma de TABLET PC](using-application-dictionaries-with-the-tablet-pc-platform-apis.md)
-   [Crear diccionarios personalizados para el reconocimiento de escritura a mano](creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2.md)

 

 



