---
description: Cuando la aplicación está tratando con palabras enteras, las posiciones válidas para el carácter de diálogo se marcan con el valor del miembro fWordStop de la estructura \_ LOGATTR de SCRIPT. Este valor se recupera mediante una llamada a ScriptBreak.
ms.assetid: c9bbfb51-727a-45ff-8450-774bc106f9f7
title: Usar puntos de interrupción de Word
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733d761d15299e02fbfb84d541a7ceba5d4d77a9b57e0280bfeedee24532d8cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146868"
---
# <a name="using-word-break-points"></a>Usar puntos de interrupción de Word

Cuando la aplicación está tratando con palabras enteras, las posiciones válidas para el carácter de diálogo se marcan con el valor del miembro **fWordStop** de la estructura [**\_ LOGATTR de SCRIPT.**](/windows/win32/api/usp10/ns-usp10-script_logattr) Este valor se recupera realizando una llamada a [**ScriptBreak.**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)

Las posiciones válidas para las líneas de separación entre palabras se marcan mediante el **valor fSoftBreak** recuperado por [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



