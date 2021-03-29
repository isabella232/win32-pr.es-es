---
title: Requisitos para los motores de texto a voz
description: Requisitos para los motores de texto a voz
ms.assetid: 21d19949-c9b4-4d9c-9684-6d15162f7a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6d1bc9f4340327c5fbfb71b900e10f60738fdf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486834"
---
# <a name="requirements-for-text-to-speech-engines"></a>Requisitos para los motores de texto a voz

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El motor debe ser totalmente compatible con SAPI 4,0. Además, el motor también debe admitir las siguientes interfaces de SAPI para el texto etiquetado y las notificaciones de marcador. Estas interfaces permiten al agente de Microsoft ajustar el ritmo de la salida de texto al globo de palabras de un carácter y sincronizar el Lip de la boca del carácter (o equivalente) con las palabras pronunciadas.

-   [ITTSCentralW](ittscentralw.md)
-   [ITTSNotifySinkW](ittsnotifysinkw.md)
-   [ITTSBufNotifySinkW](ittsbufnotifysinkw.md)
-   [ITTSAttributesW](ittsattributesw.md)

 

 




