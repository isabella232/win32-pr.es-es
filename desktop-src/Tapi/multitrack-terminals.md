---
description: TAPI 3,1 presenta la noción de un terminal Multipista, un terminal que, en esencia, es una colección de &\# 0034; realiza un seguimiento de&\# 0034; terminales.
ms.assetid: 8dd6f792-a29e-40fd-9f5b-ee5525028c2e
title: Terminales multipista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb795169f5e7cbd669e0bceb1d635e33c912c50a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677476"
---
# <a name="multitrack-terminals"></a>Terminales multipista

TAPI 3,1 presenta la noción de un terminal Multipista, un terminal que, en esencia, es una colección de terminales de "pista". Los terminales multipista facilitan la carga del programador en situaciones en las que varios flujos multimedia están implicados en una sesión de comunicaciones.

El [terminal de grabación de archivos](file-playback-terminal-and-file-recording-terminal.md) es un ejemplo de un terminal multipista. Consta de "pistas", donde cada "Track" es un terminal que corresponde a una secuencia en el archivo grabado.

Un [terminal de seguimiento](track-terminals.md) puede ser otro terminal Multipista o un terminal de una sola pista. Un terminal de una sola pista es un terminal que no tiene terminales de seguimiento. Un terminal de una sola pista es un terminal en el sentido TAPI 3 de la palabra.

Para obtener más información acerca de los terminales Multipista, vea los temas siguientes:

-   [Acerca de los terminales multipista](about-multitrack-terminals.md)
-   [Mecanismo de selección de terminal predeterminado](default-terminal-selection-mechanism.md)
-   [Selección de terminal manual](manual-terminal-selection.md)
-   [Usar terminales multipista y el mecanismo de selección predeterminado](using-multitrack-terminals-and-the-default-selection-mechanism.md)

 

 



