---
description: Un segmento de reconocimiento es la unidad de tinta básica que un reconocedor utiliza internamente para generar un resultado de reconocimiento para un objeto de entrada de lápiz determinado.
ms.assetid: 5215a0bd-6dff-4cda-b2e5-c54f64680e02
title: Segmentos de reconocimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7037849378477950b906b85efe6980c4246421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707140"
---
# <a name="recognition-segments"></a>Segmentos de reconocimiento

Un segmento de reconocimiento es la unidad de tinta básica que un reconocedor utiliza internamente para generar un resultado de reconocimiento para un objeto de entrada de lápiz determinado. Un segmento de reconocimiento es una colección de trazos de tinta. Por ejemplo, un reconocedor que es capaz de reconocer escritura a mano cursiva en inglés podría usar una palabra como el segmento de reconocimiento básico.

Otros reconocedores pueden usar partes de palabras compuestas como segmentos básicos. Por ejemplo, en español, las palabras cortas se combinan normalmente para proporcionar palabras compuestas más largas. "Damelo" es una palabra española que se compone de tres palabras "da me lo" (indíquelo), pero se escribe como una sola palabra. Un reconocedor de español podría reconocer cada subpalabra como un segmento.

Un reconocedor puede encontrar varias maneras de dividir una muestra de entrada manuscrita en segmentos de reconocimiento. Dado que la ambigüedad está implicada en el reconocimiento de la entrada prevista del usuario, el reconocedor puede devolver muchas coincidencias alternativas.

Para obtener más información acerca de los alternativos, vea [alternativas](alternates.md).

 

 



