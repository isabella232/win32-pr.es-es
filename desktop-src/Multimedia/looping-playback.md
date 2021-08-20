---
title: Reproducción en bucle para MCIWnd
description: Reproducción en bucle (MCIWnd)
ms.assetid: 59e27271-332a-4c62-bfcd-5377cdbf0848
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9144cd17886ff9d6f59bc38311481335a9ae581e5464d7feda0e7fd1a4ec2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139296"
---
# <a name="looping-playback-for-mciwnd"></a>Reproducción en bucle para MCIWnd

MCIWnd admite la reproducción como bucle continuo. Puede reproducir el contenido de un archivo o dispositivo repetidamente como un bucle mediante la macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) en combinación con el botón **Reproducir** de la barra de herramientas. El dispositivo de reproducción de vídeo, MCIAVI, admite bucles de reproducción. Para determinar si se ha activado la reproducción continua, use la macro [**MCIWndGetRepeat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)

 

 




