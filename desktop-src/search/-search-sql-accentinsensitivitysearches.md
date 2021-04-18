---
description: De forma predeterminada, el motor y el catálogo de Windows Search no distinguen los signos diacríticos, que son signos de acento agregados a las letras para modificar el significado o la Pronunciación de una palabra.
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: Sensibilidad diacrítica en las búsquedas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46fb68676418fc109fa24ed2d55fb9602b7ad41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715009"
---
# <a name="diacritic-sensitivity-in-searches"></a>Sensibilidad diacrítica en las búsquedas

De forma predeterminada, el motor y el catálogo de Windows Search no distinguen los signos diacríticos, que son signos de acento agregados a las letras para modificar el significado o la Pronunciación de una palabra. Sin embargo, Windows Search permite cambiar esto para el catálogo mediante el [Administrador de catálogos](-search-3x-wds-mngidx-catalog-manager.md) para establecer la sensibilidad diacrítica. Por ejemplo, con la distinción de diacríticos establecida en **false**, el catálogo trataría "resume" y "resumé" como si fueran la misma palabra.

En el nivel de consulta, los términos de consulta con signos diacríticos en las cláusulas FREETEXT y Contains se pasan al motor y, a continuación, se normalizan (como serían en el tiempo de índice) para buscar coincidencias. La coincidencia con el catálogo siempre distingue los signos diacríticos.

> [!Note]  
> Este no es el caso de los intervalos de caracteres 0x2e81-F8FF y 0x1100-0x11ff.

 

 

 



