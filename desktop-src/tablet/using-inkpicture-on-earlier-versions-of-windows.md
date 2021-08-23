---
description: Puede usar el control InkPicture para representar la entrada de lápiz en microsoft Windows 2000, Windows Server 2003 y ediciones de PC que no son tabletas de Windows XP. Sin embargo, no puede usar el control para introducir entrada de lápiz en estos sistemas operativos.
ms.assetid: e5d00b0f-0a4f-4ea2-ae63-dfb6bc8c2caf
title: Usar InkPicture en versiones anteriores de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52423e8eb3e4c7f59da7a7caac299428dd8efcdce2192819444bfe91070f10b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091365"
---
# <a name="using-inkpicture-on-earlier-versions-of-windows"></a>Usar InkPicture en versiones anteriores de Windows

Puede usar el [control InkPicture](inkpicture-control.md) para representar la entrada de lápiz en microsoft Windows 2000, Windows Server 2003 y ediciones de PC que no son tabletas de Windows XP. Sin embargo, no puede usar el control para introducir entrada de lápiz en estos sistemas operativos.

La propiedad [**InkEnabled del**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) control se establece **en FALSE** y el intento de cambiar la propiedad no tiene ningún efecto. Puede asignar valores a otras propiedades y manipular la entrada de lápiz mediante programación, pero no puede usar el control para recopilar la entrada de lápiz.

 

 



