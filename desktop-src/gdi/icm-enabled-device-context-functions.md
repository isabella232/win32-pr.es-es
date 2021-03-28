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
# <a name="icm-enabled-device-context-functions"></a><span data-ttu-id="619f7-103">ICM-Enabled funciones de contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="619f7-103">ICM-Enabled Device Context Functions</span></span>

<span data-ttu-id="619f7-104">La administración del color de imagen (ICM) de Microsoft garantiza que una imagen de color, un gráfico o un objeto de texto se representan lo más cerca posible de su intención original en cualquier dispositivo, a pesar de las diferencias en las tecnologías de creación de imágenes y las capacidades de color entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="619f7-104">Microsoft Image Color Management (ICM) ensures that a color image, graphic, or text object is rendered as closely as possible to its original intent on any device, despite differences in imaging technologies and color capabilities between devices.</span></span> <span data-ttu-id="619f7-105">(Para obtener más información, consulte [sistema de color de Windows](/previous-versions//dd372446(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="619f7-105">(For more information, see [Windows Color System](/previous-versions//dd372446(v=vs.85)).)</span></span>

<span data-ttu-id="619f7-106">Hay varias funciones en la interfaz de dispositivo gráfico (GDI) que utilizan o operan en los datos de color.</span><span class="sxs-lookup"><span data-stu-id="619f7-106">There are various functions in the graphics device interface (GDI) that use or operate on color data.</span></span> <span data-ttu-id="619f7-107">Las siguientes funciones de contexto de dispositivo están habilitadas para su uso con ICM:</span><span class="sxs-lookup"><span data-stu-id="619f7-107">The following device context functions are enabled for use with ICM:</span></span>

-   [<span data-ttu-id="619f7-108">**CreateCompatibleDC**</span><span class="sxs-lookup"><span data-stu-id="619f7-108">**CreateCompatibleDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)
-   [<span data-ttu-id="619f7-109">**CreateDC**</span><span class="sxs-lookup"><span data-stu-id="619f7-109">**CreateDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdca)
-   [<span data-ttu-id="619f7-110">**GetDCBrushColor**</span><span class="sxs-lookup"><span data-stu-id="619f7-110">**GetDCBrushColor**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)
-   [<span data-ttu-id="619f7-111">**GetDCPenColor**</span><span class="sxs-lookup"><span data-stu-id="619f7-111">**GetDCPenColor**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)
-   [<span data-ttu-id="619f7-112">**ResetDC**</span><span class="sxs-lookup"><span data-stu-id="619f7-112">**ResetDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)
-   [<span data-ttu-id="619f7-113">**SelectObject**</span><span class="sxs-lookup"><span data-stu-id="619f7-113">**SelectObject**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)
-   [<span data-ttu-id="619f7-114">**SetDCBrushColor**</span><span class="sxs-lookup"><span data-stu-id="619f7-114">**SetDCBrushColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)
-   [<span data-ttu-id="619f7-115">**SetDCPenColor**</span><span class="sxs-lookup"><span data-stu-id="619f7-115">**SetDCPenColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)

 

 
