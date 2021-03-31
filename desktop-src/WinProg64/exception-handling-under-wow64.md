---
title: Control de excepciones en WOW64
description: WOW64 usa las excepciones nativas x64, ia64 o ARM64 como transporte para las excepciones x86. Por lo tanto, en una aplicación de 32 bits que se ejecuta bajo WOW64, las excepciones no detectadas se comportan como excepciones nativas de 64 bits.
ms.assetid: 2EE1A1F3-A691-4ee6-9587-7FF7C4F9DD98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb57e56b85be4769d452a5772ff7b0024724641
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078232"
---
# <a name="exception-handling-under-wow64"></a>Control de excepciones en WOW64

WOW64 usa las excepciones nativas x64, ia64 o ARM64 como transporte para las excepciones x86. Por lo tanto, en una aplicación de 32 bits que se ejecuta bajo WOW64, las excepciones no detectadas se comportan como excepciones nativas de 64 bits.

En una aplicación que se ejecuta en una versión de 32 bits de Windows, las excepciones no detectadas se pasan a los controladores de excepciones de nivel superior de la aplicación, si están disponibles. En la misma aplicación de 32 bits que se ejecuta bajo WOW64, el sistema puede suprimir las excepciones no detectadas.

**Windows Vista, Windows Server 2003 y Windows XP:** En la misma aplicación de 32 bits que se ejecuta bajo WOW64, el sistema llama a los filtros de excepción, pero puede suprimir las excepciones no detectadas sin invocar los controladores asociados. Este comportamiento ha cambiado a partir de Windows Vista con Service Pack 1 (SP1).

Para obtener más información sobre las excepciones no detectadas en los procedimientos de ventana, vea la función [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

 

 