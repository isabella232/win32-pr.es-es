---
description: Por lo general, las aplicaciones anteriores no necesitan cambios para funcionar en varios sistemas de supervisión.
ms.assetid: 908cf88c-69ed-4855-817d-ba749e14ff85
title: Consideraciones de varios monitores para programas anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feebb356cb2f9c5480c84f1718b51d6e866ef621
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127475921"
---
# <a name="multiple-monitor-considerations-for-older-programs"></a>Consideraciones de varios monitores para programas anteriores

Por lo general, las aplicaciones anteriores no necesitan cambios para funcionar en varios sistemas de supervisión. En la mayoría de los casos, el sistema parecerá tener solo una pantalla. Las métricas del sistema reflejan la presentación principal y las aplicaciones de pantalla completa se muestran en la principal. El sistema controla la minimización, la maximización, los menús y los cuadros de diálogo.

Sin embargo, algunos programas tendrán problemas. Algunos que podrían tener problemas son las aplicaciones de control remoto, las que tienen acceso directo al hardware y las que han revisiones al controlador GDI o DISPLAY. En estos casos, es posible que se requiera al usuario que deshabilite cualquier monitor más allá del monitor principal.

 

 



