---
title: Requisitos de los motores de texto a voz
description: Requisitos de los motores de texto a voz
ms.assetid: 21d19949-c9b4-4d9c-9684-6d15162f7a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3025be266d0aa40cd5a3bca6adb63e333310df444be7bd07e3a72b0f10b9c49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746420"
---
# <a name="requirements-for-text-to-speech-engines"></a>Requisitos de los motores de texto a voz

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

El motor debe ser totalmente compatible con SAPI 4.0. Además, el motor también debe admitir las siguientes interfaces SAPI para notificaciones etiquetadas de texto y marcadores. Estas interfaces permiten a Microsoft Agent dar un ritmo a la salida de texto al globo de palabras de un carácter y sincronizar la expresión del carácter (o equivalente) con las palabras habladas.

-   [ITTSCentralW](ittscentralw.md)
-   [ITTSNotifySinkW](ittsnotifysinkw.md)
-   [ITTSBufNotifySinkW](ittsbufnotifysinkw.md)
-   [ITTSAttributesW](ittsattributesw.md)

 

 




