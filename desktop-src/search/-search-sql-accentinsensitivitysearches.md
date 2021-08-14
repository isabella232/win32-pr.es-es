---
description: De forma predeterminada, el motor de Windows Search y el catálogo no son sensibles a los signos diacríticos, que son marcas de acento agregadas a las letras para modificar el significado o la pronunciación de una palabra.
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: Confidencialidad diacrítica en las búsquedas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fcde4eb6cde6fe7a0b25a1d58f8026176de2fe30b6b0e2f020275821891a404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863689"
---
# <a name="diacritic-sensitivity-in-searches"></a>Confidencialidad diacrítica en las búsquedas

De forma predeterminada, el motor de Windows Search y el catálogo no son sensibles a los signos diacríticos, que son marcas de acento agregadas a las letras para modificar el significado o la pronunciación de una palabra. Sin embargo, Windows Search le permite cambiar esto para el catálogo mediante el Administrador de [catálogos](-search-3x-wds-mngidx-catalog-manager.md) para establecer la confidencialidad diacrítica. Por ejemplo, con la confidencialidad diacrítica establecida en **FALSE,** el catálogo trataría "resume" y "resumé" como si fueran la misma palabra.

En el nivel de consulta, los términos de consulta con signos diacríticos en las cláusulas FREETEXT y CONTAINS se pasan al motor y, a continuación, se normalizan (como lo harían en el momento del índice) para la coincidencia. La coincidencia con el catálogo siempre es diacrítica.

> [!Note]  
> Este no es el caso de los intervalos de caracteres 0x2e81-f8ff y 0x1100-0x11ff.

 

 

 



