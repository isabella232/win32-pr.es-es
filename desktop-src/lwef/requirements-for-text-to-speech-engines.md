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
# <a name="requirements-for-text-to-speech-engines"></a><span data-ttu-id="59456-103">Requisitos para los motores de texto a voz</span><span class="sxs-lookup"><span data-stu-id="59456-103">Requirements for Text-To-Speech Engines</span></span>

<span data-ttu-id="59456-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="59456-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="59456-105">El motor debe ser totalmente compatible con SAPI 4,0.</span><span class="sxs-lookup"><span data-stu-id="59456-105">The engine must be fully SAPI 4.0-compliant.</span></span> <span data-ttu-id="59456-106">Además, el motor también debe admitir las siguientes interfaces de SAPI para el texto etiquetado y las notificaciones de marcador.</span><span class="sxs-lookup"><span data-stu-id="59456-106">In addition, the engine must also support the following SAPI interfaces for tagged text and bookmark notifications.</span></span> <span data-ttu-id="59456-107">Estas interfaces permiten al agente de Microsoft ajustar el ritmo de la salida de texto al globo de palabras de un carácter y sincronizar el Lip de la boca del carácter (o equivalente) con las palabras pronunciadas.</span><span class="sxs-lookup"><span data-stu-id="59456-107">These interfaces enable Microsoft Agent to pace the output of text to a character's word balloon and lip-sync the character's mouth (or equivalent) with the spoken words.</span></span>

-   [<span data-ttu-id="59456-108">ITTSCentralW</span><span class="sxs-lookup"><span data-stu-id="59456-108">ITTSCentralW</span></span>](ittscentralw.md)
-   [<span data-ttu-id="59456-109">ITTSNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="59456-109">ITTSNotifySinkW</span></span>](ittsnotifysinkw.md)
-   [<span data-ttu-id="59456-110">ITTSBufNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="59456-110">ITTSBufNotifySinkW</span></span>](ittsbufnotifysinkw.md)
-   [<span data-ttu-id="59456-111">ITTSAttributesW</span><span class="sxs-lookup"><span data-stu-id="59456-111">ITTSAttributesW</span></span>](ittsattributesw.md)

 

 




