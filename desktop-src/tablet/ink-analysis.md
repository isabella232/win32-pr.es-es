---
description: En el caso de una aplicación que acepta escritura a mano mixta y entrada de dibujo, la capacidad de distinguir entre escritura a mano y dibujo y agrupar escritura a mano en subcategorías, como segmentos de reconocimiento, líneas y párrafos, es muy útil.
ms.assetid: 17ce349c-10f3-4d9b-abb0-7af4f40bab32
title: Análisis de la entrada de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021882d8f2de83b4bac9580ae66dd097bfd556db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082006"
---
# <a name="ink-analysis"></a>Análisis de la entrada de lápiz

En el caso de una aplicación que acepta escritura a mano mixta y entrada de dibujo, la capacidad de distinguir entre escritura a mano y dibujo y agrupar escritura a mano en subcategorías, como segmentos de reconocimiento, líneas y párrafos, es muy útil.

## <a name="ink-analysis-library"></a>Biblioteca de análisis de tinta

Las API de análisis de tinta combinan eficazmente dos tecnologías distintas pero gratuitas: el reconocimiento de escritura a mano y el análisis de tinta. La combinación de estas dos tecnologías proporciona resultados más definitivos que las partes tomadas por sí sola.

El reconocimiento de escritura a mano es el análisis computacional de la tinta digital manuscrita para devolver la interpretación basada en caracteres en un idioma determinado. Es decir, el reconocimiento de escritura a mano es el modo en que el equipo "Lee" la escritura a mano de una persona.

El análisis de tintas se puede desglosar aún más en el análisis de diseño y clasificación de tinta. La clasificación de tinta es la división computacional de la entrada manuscrita en unidades semánticamente significativas como párrafos, líneas, palabras y dibujos. El análisis de diseño es el examen computacional de la entrada manuscrita para determinar la posición de la tinta en la superficie de entrada manuscrita y cómo se relacionan los trazos entre sí espacialmente e incluso semánticamente.

Para más información sobre cómo usar las API de administrado de tinta, consulte [información general del análisis de tinta](ink-analysis-overview.md).

 

 



