---
description: De forma predeterminada, el reconocedor utiliza un diccionario del sistema que contiene todas las palabras escritas normalmente en un idioma.
ms.assetid: 2ddf04dd-613b-4570-9474-0e33208c4012
title: Uso de diccionarios de aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dfda443a688af9dfcec44a81f0e5ed2d50846c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497344"
---
# <a name="using-application-dictionaries"></a>Uso de diccionarios de aplicación

De forma predeterminada, el reconocedor utiliza un diccionario del sistema que contiene todas las palabras escritas normalmente en un idioma. Además, el reconocedor tiene un diccionario de usuario que contiene palabras que el usuario ha agregado al diccionario. Los usuarios agregan una palabra al Diccionario de usuarios a través del panel de entrada de Tablet PC a través de selecciones en:

-   La lista alternativa (al escribir).
-   Menú de herramientas de voz (al hablar).

Si diseña una aplicación en la que espera que el usuario escriba palabras que no se encuentran en el Diccionario del sistema o en el Diccionario del usuario, cree un diccionario de aplicación. Un diccionario de aplicación mejora aún más la precisión del reconocimiento al proporcionar al reconocedor una lista personalizada adicional de palabras que se pueden escribir como escritura a mano en una aplicación.

Puede crear un diccionario de aplicación mediante el objeto de la información de [**palabras**](inkwordlist-class.md) . El Diccionario de aplicación subsiguiente aumenta la precisión del reconocimiento al proporcionar al reconocedor una lista de palabras previstas. Por ejemplo, un diccionario de aplicación que contiene la terminología médica aumenta la precisión del reconocimiento en una aplicación desarrollada para el sector médico en el que es probable que se escriban los términos.

Otro ejemplo: al diseñar un formulario para que alguien pida instrumentos musicales, cree un objeto de una nueva de [**palabras**](inkwordlist-class.md) que contenga los nombres de los fabricantes de instrumentos más comunes. Establezca la propiedad de la definición de [**palabras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del objeto [**RecognizerContext**](inkrecognizercontext-class.md) en el objeto de la de **palabras** que creó. A continuación, el objeto **RecognizerContext** pasa esta lista de palabras al reconocedor. El Diccionario de aplicación aumenta la precisión del reconocimiento cuando estos nombres se escriben en un campo de la aplicación.

En los temas siguientes se describe cómo usar los diccionarios de aplicaciones.

-   [Descripción de las listas de palabras, el contexto del reconocedor y Factoids](understanding-wordlists--the-recognizercontext--and-factoids.md)
-   [Uso de diccionarios de aplicación con las API de la plataforma de Tablet PC](using-application-dictionaries-with-the-tablet-pc-platform-apis.md)
-   [Crear diccionarios personalizados para el reconocimiento de escritura a mano](creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2.md)

 

 



