---
description: Cuando la aplicación está tratando con palabras completas, las posiciones válidas para el símbolo de intercalación se marcan con el valor del miembro fWordStop de la \_ estructura LOGATTR del script. Este valor se recupera realizando una llamada a ScriptBreak.
ms.assetid: c9bbfb51-727a-45ff-8450-774bc106f9f7
title: Usar puntos de interrupción de palabras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9cf68d5c90b6e93a6e6f15706ec357c7a33b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279490"
---
# <a name="using-word-break-points"></a>Usar puntos de interrupción de palabras

Cuando la aplicación está tratando con palabras completas, las posiciones válidas para el símbolo de intercalación se marcan con el valor del miembro **fWordStop** de la estructura [**\_ LOGATTR del script**](/windows/win32/api/usp10/ns-usp10-script_logattr) . Este valor se recupera realizando una llamada a [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).

Las posiciones válidas para las líneas de división entre palabras se marcan con el valor **fSoftBreak** recuperado por [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



