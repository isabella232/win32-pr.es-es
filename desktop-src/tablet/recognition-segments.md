---
description: Un segmento de reconocimiento es la unidad de entrada de lápiz básica que un reconocedor usa internamente para generar un resultado de reconocimiento para un objeto Ink determinado.
ms.assetid: 5215a0bd-6dff-4cda-b2e5-c54f64680e02
title: Segmentos de reconocimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d43d2e3f700da2ee3ef780de9ac2ad23a17f4f8894163d8c011f6bfa9c5551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455355"
---
# <a name="recognition-segments"></a>Segmentos de reconocimiento

Un segmento de reconocimiento es la unidad de entrada de lápiz básica que un reconocedor usa internamente para generar un resultado de reconocimiento para un objeto Ink determinado. Un segmento de reconocimiento es una colección de trazos de lápiz. Por ejemplo, un reconocedor capaz de reconocer la escritura a mano cursiva en inglés podría usar una palabra como segmento de reconocimiento básico.

Otros reconocedores pueden usar partes de palabras compuestas como segmentos básicos. Por ejemplo, en español, las palabras cortas se combinan normalmente para proporcionar palabras compuestas más largas. "Suéltalo" es una palabra en español que se compone de tres palabras "da me lo" (deme eso), pero se escribe como una sola palabra. Un reconocedor español podría reconocer cada subpago como un segmento.

Un reconocedor puede encontrar varias maneras de dividir una muestra de lápiz en segmentos de reconocimiento. Dado que la ambigüedad está implicada en el reconocimiento de la entrada prevista del usuario, el reconocedor puede devolver muchas coincidencias alternativas.

Para obtener más información sobre las alternativas, vea [Alternativas.](alternates.md)

 

 



