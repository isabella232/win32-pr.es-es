---
title: Reproducción en bucle de MCIWnd
description: Reproducción en bucle (MCIWnd)
ms.assetid: 59e27271-332a-4c62-bfcd-5377cdbf0848
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d6a22e917cf764b37444bcaf4afb0393e1c1b
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106188010"
---
# <a name="looping-playback-for-mciwnd"></a>Reproducción en bucle de MCIWnd

MCIWnd admite la reproducción como un bucle continuo. Puede reproducir el contenido de un archivo o dispositivo repetidamente como un bucle mediante el uso de la macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) en combinación con el botón **reproducir** de la barra de herramientas. El dispositivo de reproducción de vídeo, MCIAVI, admite bucles de reproducción. Para determinar si se ha activado la reproducción continua, use la macro [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) .

 

 




