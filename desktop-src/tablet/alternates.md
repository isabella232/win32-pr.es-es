---
description: Una alternativa es una coincidencia de palabras posible para un segmento de reconocimiento. Un reconocedor genera alternativas y las basa en coincidencias aceptables de la entrada manuscrita o de audio en un diccionario o Factoid.
ms.assetid: 69327f1d-f240-4b8a-8bee-0a96a0c425c2
title: Alternativas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350c9ac97f0af1451a0ded6445cf658dad4ee4c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666201"
---
# <a name="alternates"></a>Alternativas

Una alternativa es una coincidencia de palabras posible para un segmento de reconocimiento. Un reconocedor genera alternativas y las basa en coincidencias aceptables de la entrada manuscrita o de audio en un diccionario o Factoid.

> [!Note]  
> Actualmente, la evaluación de confianza solo está disponible para los reconocedores de Microsoft English (Estados Unidos) y gestos.

 

A veces, la tinta puede tener distinciones ambiguas entre segmentos. El reconocedor compara estos segmentos con un diccionario de reconocedor para determinar las posibles coincidencias. Cuando el reconocedor compara los segmentos, mantiene una lista de posibles coincidencias alternativas y asigna un nivel de confianza a cada una de ellas, seleccionando una opción superior.

> [!Note]  
> El Reconocedor no puede proporcionar alternativas para una parte de la tinta menor que un segmento de reconocimiento.

 

 

 



