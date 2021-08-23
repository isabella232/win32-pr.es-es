---
description: Una alternativa es una posible coincidencia de palabras para un segmento de reconocimiento. Un reconocedor genera alternativas y las basa en coincidencias aceptables de la entrada de entrada de lápiz o audio en un diccionario o factoid.
ms.assetid: 69327f1d-f240-4b8a-8bee-0a96a0c425c2
title: Alternativas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76faf27b82a6bfc064fddbad3d2d4ca6c2dddc098d56bca340b677cea17a319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119337045"
---
# <a name="alternates"></a>Alternativas

Una alternativa es una posible coincidencia de palabras para un segmento de reconocimiento. Un reconocedor genera alternativas y las basa en coincidencias aceptables de la entrada de entrada de lápiz o audio en un diccionario o factoid.

> [!Note]  
> La evaluación de confianza solo está disponible actualmente para el inglés de Microsoft (Estados Unidos) y los reconocedores de gestos.

 

A veces, la entrada de lápiz puede tener distinciones ambiguas entre segmentos. El reconocedor compara estos segmentos con un diccionario de reconocedores para determinar posibles coincidencias. Cuando el reconocedor compara los segmentos, mantiene una lista de posibles coincidencias alternativas y asigna un nivel de confianza a cada uno de ellos, eligiendo una de las principales opciones.

> [!Note]  
> El reconocedor no puede proporcionar alternativas para una parte de la entrada de lápiz menor que un segmento de reconocimiento.

 

 

 



