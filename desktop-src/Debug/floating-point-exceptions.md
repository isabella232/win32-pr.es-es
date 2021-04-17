---
description: De forma predeterminada, el sistema tiene todas las excepciones FP desactivadas.
ms.assetid: efbea036-de9c-4f92-865a-494161da375e
title: Excepciones de punto flotante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a4db92a13a0215bb372db12d30bb11a749a0fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659305"
---
# <a name="floating-point-exceptions"></a>Excepciones de punto flotante

De forma predeterminada, el sistema tiene todas las excepciones FP desactivadas. Por lo tanto, los cálculos generan NAN o infinito, en lugar de una excepción. Antes de poder interceptar las excepciones de punto flotante (FP) mediante el control de excepciones estructurado, debe llamar a la función de biblioteca en tiempo de ejecución de C de [ \_ controlfp \_ s](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) para activar todas las excepciones FP posibles. Para capturar solo determinadas excepciones, use solo las marcas que corresponden a las excepciones que se van a capturar. Tenga en cuenta que cualquier controlador de errores de FP debe llamar a [ \_ clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) como su primera instrucción FP. Esta función borra las excepciones de punto flotante.

 

 
