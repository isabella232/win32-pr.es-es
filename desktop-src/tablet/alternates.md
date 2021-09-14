---
description: Una alternativa es una posible coincidencia de palabras para un segmento de reconocimiento. Un reconocedor genera alternativas y las basa en coincidencias aceptables de la entrada de lápiz o audio en un diccionario o factoid.
ms.assetid: 69327f1d-f240-4b8a-8bee-0a96a0c425c2
title: Alternativas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350c9ac97f0af1451a0ded6445cf658dad4ee4c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247875"
---
# <a name="alternates"></a>Alternativas

Una alternativa es una posible coincidencia de palabras para un segmento de reconocimiento. Un reconocedor genera alternativas y las basa en coincidencias aceptables de la entrada de lápiz o audio en un diccionario o factoid.

> [!Note]  
> Actualmente, la evaluación de confianza solo está disponible para el inglés de Microsoft (Estados Unidos) y los reconocedores de gestos.

 

A veces, la entrada de lápiz puede tener distinciones ambiguas entre segmentos. El reconocedor compara estos segmentos con un diccionario de reconocedores para determinar posibles coincidencias. Cuando el reconocedor compara los segmentos, mantiene una lista de posibles coincidencias alternativas y asigna un nivel de confianza a cada uno de ellos, eligiendo una de las principales opciones.

> [!Note]  
> El reconocedor no puede proporcionar alternativas para una parte de la entrada de lápiz menor que un segmento de reconocimiento.

 

 

 



