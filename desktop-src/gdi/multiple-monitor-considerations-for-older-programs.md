---
description: Por lo general, las aplicaciones antiguas no necesitan cambios para trabajar en varios sistemas de supervisión.
ms.assetid: 908cf88c-69ed-4855-817d-ba749e14ff85
title: Consideraciones de varios monitores para programas anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feebb356cb2f9c5480c84f1718b51d6e866ef621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984922"
---
# <a name="multiple-monitor-considerations-for-older-programs"></a>Consideraciones de varios monitores para programas anteriores

Por lo general, las aplicaciones antiguas no necesitan cambios para trabajar en varios sistemas de supervisión. Para la mayoría, el sistema parecerá tener una sola pantalla. Las métricas del sistema reflejan la pantalla principal y las aplicaciones de pantalla completa que aparecen en el servidor principal. El sistema controla la minimización, la maximización, los menús y los cuadros de diálogo.

Sin embargo, algunos programas tendrán problemas. Algunos de los problemas que podrían tener problemas son las aplicaciones de control remoto, las que tienen acceso directo al hardware y las que han revisado el controlador de pantalla o el GDI. En estos casos, puede ser necesario que el usuario deshabilite cualquier monitor más allá del monitor principal.

 

 



