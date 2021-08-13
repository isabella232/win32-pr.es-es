---
title: Control de excepciones en WOW64
description: WOW64 usa excepciones x64, ia64 o ARM64 nativas como transporte para excepciones x86. Por lo tanto, en una aplicación de 32 bits que se ejecuta en WOW64, las excepciones no detectadas se comportan como excepciones nativas de 64 bits.
ms.assetid: 2EE1A1F3-A691-4ee6-9587-7FF7C4F9DD98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7d461a809ac35a4742f9bdbbaeb461eb6d7365075d9c4b57334a94f434c1e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561539"
---
# <a name="exception-handling-under-wow64"></a>Control de excepciones en WOW64

WOW64 usa excepciones x64, ia64 o ARM64 nativas como transporte para excepciones x86. Por lo tanto, en una aplicación de 32 bits que se ejecuta en WOW64, las excepciones no detectadas se comportan como excepciones nativas de 64 bits.

En una aplicación que se ejecuta en una versión de 32 bits de Windows, las excepciones no detectadas se pasan a controladores de excepciones de nivel superior de la aplicación, cuando están disponibles. En la misma aplicación de 32 bits que se ejecuta en WOW64, el sistema puede suprimir las excepciones no detectadas.

**Windows Vista, Windows Server 2003 y Windows XP:** En la misma aplicación de 32 bits que se ejecuta en WOW64, el sistema llama a los filtros de excepción, pero puede suprimir las excepciones no detectadas sin invocar a los controladores asociados. Este comportamiento cambió a partir de Windows Vista con Service Pack 1 (SP1).

Para obtener más información sobre las excepciones no detectadas en procedimientos de ventana, vea la [función WindowProc.](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

 

 