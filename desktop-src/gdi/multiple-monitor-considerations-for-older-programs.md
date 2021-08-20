---
description: Por lo general, las aplicaciones anteriores no necesitan cambios para funcionar en varios sistemas de supervisión.
ms.assetid: 908cf88c-69ed-4855-817d-ba749e14ff85
title: Consideraciones de varios monitores para programas anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4444d3de54886c4743c17f7348482f154e21a11d027cd05014ac5eb26cb6a249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117698771"
---
# <a name="multiple-monitor-considerations-for-older-programs"></a>Consideraciones de varios monitores para programas anteriores

Por lo general, las aplicaciones anteriores no necesitan cambios para funcionar en varios sistemas de supervisión. En la mayoría de los casos, el sistema parecerá tener solo una pantalla. Las métricas del sistema reflejan la presentación principal y las aplicaciones de pantalla completa se muestran en la principal. El sistema controla la minimización, la maximización, los menús y los cuadros de diálogo.

Sin embargo, algunos programas tendrán problemas. Algunos que podrían tener problemas son las aplicaciones de control remoto, las que tienen acceso directo al hardware y las que han revisiones al controlador GDI o DISPLAY. En estos casos, es posible que se requiera al usuario que deshabilite cualquier monitor más allá del monitor principal.

 

 



