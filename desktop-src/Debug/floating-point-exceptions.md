---
description: De forma predeterminada, el sistema tiene desactivadas todas las excepciones fp.
ms.assetid: efbea036-de9c-4f92-865a-494161da375e
title: Excepciones de punto flotante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2990929b712c65a09dcdae1e88d0a84b03d0f6d6cb3b6070fb3096ca998a10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691815"
---
# <a name="floating-point-exceptions"></a>Excepciones de punto flotante

De forma predeterminada, el sistema tiene desactivadas todas las excepciones fp. Por lo tanto, los cálculos tienen como resultado NAN o INFINITY, en lugar de una excepción. Para poder capturar excepciones de punto flotante (FP) mediante el control de excepciones estructurado, debe llamar a la función de biblioteca en tiempo de ejecución [ \_ \_ C](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) del equipo de control para activar todas las posibles excepciones de FP. Para capturar solo excepciones concretas, use solo las marcas correspondientes a las excepciones que se capturarán. Tenga en cuenta que cualquier controlador de errores de FP debe llamar [ \_ a clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) como su primera instrucción FP. Esta función borra las excepciones de punto flotante.

 

 
