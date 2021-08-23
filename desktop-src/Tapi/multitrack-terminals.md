---
description: TAPI 3.1 presenta la noción de terminal multipista, un terminal que, básicamente, es una colección de terminales \# &0034;seguimiento&\# 0034; terminales.
ms.assetid: 8dd6f792-a29e-40fd-9f5b-ee5525028c2e
title: Terminales multipista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9e5f9c6d614308370b3d9211f578d5fcb2650bd3c5ba7f8a81dbc981ad2687
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575525"
---
# <a name="multitrack-terminals"></a>Terminales multipista

TAPI 3.1 presenta la noción de terminal multipista, un terminal que, básicamente, es una colección de terminales de "seguimiento". Los terminales multipista facilitan la carga del programador en situaciones en las que hay varios flujos multimedia implicados en una sesión de comunicaciones.

El [Terminal de grabación de archivos](file-playback-terminal-and-file-recording-terminal.md) es un ejemplo de terminal multipista. Consta de "pistas", donde cada "pista" es un terminal correspondiente a una secuencia en el archivo grabado.

Un [terminal de pista](track-terminals.md) puede ser otro terminal multipista o un terminal de un solo seguimiento. Un terminal de una sola pista es un terminal que no tiene terminales de pista. Un terminal de un solo seguimiento es un terminal en el sentido TAPI 3 de la palabra.

Para obtener más información sobre los terminales multipista, vea los temas siguientes:

-   [Acerca de los terminales multipista](about-multitrack-terminals.md)
-   [Mecanismo de selección de terminal predeterminado](default-terminal-selection-mechanism.md)
-   [Selección manual de terminal](manual-terminal-selection.md)
-   [Uso de terminales multipista y el mecanismo de selección predeterminado](using-multitrack-terminals-and-the-default-selection-mechanism.md)

 

 



