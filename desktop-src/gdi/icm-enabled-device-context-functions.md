---
description: Microsoft Image Color Management (ICM) garantiza que una imagen de color, un gráfico o un objeto de texto se represente lo más cerca posible de su intención original en cualquier dispositivo, a pesar de las diferencias en las tecnologías de creación de imágenes y las funcionalidades de color entre dispositivos.
ms.assetid: eced18cf-be5a-4c61-b0e5-36d607daa6ff
title: ICM-Enabled funciones de contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33337aeea32f1ca84b74e3fc45e9bd67dbfe1ce1a5300a502a5303f55cab357
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944205"
---
# <a name="icm-enabled-device-context-functions"></a>ICM-Enabled funciones de contexto de dispositivo

Microsoft Image Color Management (ICM) garantiza que una imagen de color, un gráfico o un objeto de texto se represente lo más cerca posible de su intención original en cualquier dispositivo, a pesar de las diferencias en las tecnologías de creación de imágenes y las funcionalidades de color entre dispositivos. (Para obtener más información, [vea Windows Color System](/previous-versions//dd372446(v=vs.85))).

Hay varias funciones en la interfaz de dispositivo gráfico (GDI) que usan o funcionan con datos de color. Las siguientes funciones de contexto de dispositivo están habilitadas para su uso con ICM:

-   [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)
-   [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)
-   [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)
-   [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)
-   [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)
-   [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)
-   [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)
-   [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)

 

 
