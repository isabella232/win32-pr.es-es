---
title: Generar coordenadas de textura
description: En lugar de proporcionar explícitamente coordenadas de textura, puede hacer que OpenGL las genere como una función de otros datos de vértices mediante glTexGen \.
ms.assetid: 5c9ce163-6107-46a3-8c8d-fc87d2f8cf9a
keywords:
- Canalización de procesamiento de OpenGL, coordenadas de textura
- coordenadas de textura OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d3f5b807f25aee2783ff8dab3a4930a9c797ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268998"
---
# <a name="generating-texture-coordinates"></a>Generar coordenadas de textura

En lugar de proporcionar explícitamente coordenadas de textura, puede hacer que OpenGL las genere como una función de otros datos de vértices mediante [glTexGen \* ](gltexgen-functions.md). Una vez especificadas o generadas las coordenadas de textura, se transforman mediante la matriz de textura. Esta matriz se controla con las mismas funciones que se usan para las transformaciones de matriz (vea [transformaciones de matriz](matrix-transformations.md)).

 

 




