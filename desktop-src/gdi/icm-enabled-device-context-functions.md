---
description: La administración del color de imagen (ICM) de Microsoft garantiza que una imagen de color, un gráfico o un objeto de texto se representan lo más cerca posible de su intención original en cualquier dispositivo, a pesar de las diferencias en las tecnologías de creación de imágenes y las capacidades de color entre los dispositivos.
ms.assetid: eced18cf-be5a-4c61-b0e5-36d607daa6ff
title: ICM-Enabled funciones de contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a0b49e62d0b4d05e0690d2aee0d3c5f0f530cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984951"
---
# <a name="icm-enabled-device-context-functions"></a>ICM-Enabled funciones de contexto de dispositivo

La administración del color de imagen (ICM) de Microsoft garantiza que una imagen de color, un gráfico o un objeto de texto se representan lo más cerca posible de su intención original en cualquier dispositivo, a pesar de las diferencias en las tecnologías de creación de imágenes y las capacidades de color entre los dispositivos. (Para obtener más información, consulte [sistema de color de Windows](/previous-versions//dd372446(v=vs.85))).

Hay varias funciones en la interfaz de dispositivo gráfico (GDI) que utilizan o operan en los datos de color. Las siguientes funciones de contexto de dispositivo están habilitadas para su uso con ICM:

-   [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)
-   [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)
-   [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)
-   [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)
-   [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)
-   [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)
-   [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)
-   [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)

 

 
