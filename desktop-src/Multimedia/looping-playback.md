---
title: Reproducción en bucle para MCIWnd
description: Reproducción en bucle (MCIWnd)
ms.assetid: 59e27271-332a-4c62-bfcd-5377cdbf0848
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d6a22e917cf764b37444bcaf4afb0393e1c1b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372332"
---
# <a name="looping-playback-for-mciwnd"></a>Reproducción en bucle para MCIWnd

MCIWnd admite la reproducción como bucle continuo. Puede reproducir el contenido de un archivo o dispositivo repetidamente como un bucle mediante la macro  [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) en combinación con el botón Reproducir de la barra de herramientas. El dispositivo de reproducción de vídeo, MCIAVI, admite bucles de reproducción. Para determinar si se ha activado la reproducción continua, use la macro [**MCIWndGetRepeat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)

 

 




