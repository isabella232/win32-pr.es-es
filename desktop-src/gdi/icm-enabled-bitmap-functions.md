---
description: La administración del color de imagen (ICM) de Microsoft garantiza que una imagen de color, un objeto gráfico o un objeto de texto se representan lo más cerca posible de su intención original en cualquier dispositivo, a pesar de las diferencias en las tecnologías de creación de imágenes y las capacidades de color entre los dispositivos.
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: ICM-Enabled funciones de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b89dac569aafad1ef94b066bc97f588bac62c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908485"
---
# <a name="icm-enabled-bitmap-functions"></a><span data-ttu-id="e3b13-103">ICM-Enabled funciones de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="e3b13-103">ICM-Enabled Bitmap Functions</span></span>

<span data-ttu-id="e3b13-104">La administración del color de imagen (ICM) de Microsoft garantiza que una imagen de color, un objeto gráfico o un objeto de texto se representan lo más cerca posible de su intención original en cualquier dispositivo, a pesar de las diferencias en las tecnologías de creación de imágenes y las capacidades de color entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e3b13-104">Microsoft Image Color Management (ICM) ensures that a color image, graphic object, or text object is rendered as closely as possible to its original intent on any device, despite differences in imaging technologies and color capabilities between devices.</span></span> <span data-ttu-id="e3b13-105">Tanto si está digitalizando una imagen como en otro gráfico en un escáner de color, descargándolo a través de Internet, viéndolo o editándolo en pantalla o imprimiendo en papel, película u otros medios, ICM 2,0 le ayuda a mantener la coherencia y la precisión de los colores.</span><span class="sxs-lookup"><span data-stu-id="e3b13-105">Whether you are scanning an image or other graphic on a color scanner, downloading it over the Internet, viewing or editing it onscreen, or printing it on paper, film, or other media, ICM 2.0 helps you keep colors consistent and accurate.</span></span> <span data-ttu-id="e3b13-106">Para obtener más información acerca de ICM, consulte [sistema de color de Windows](/previous-versions//dd372446(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e3b13-106">For more information about ICM, see [Windows Color System](/previous-versions//dd372446(v=vs.85)).</span></span>

<span data-ttu-id="e3b13-107">Hay varias funciones en la interfaz de dispositivo gráfico (GDI) que utilizan o operan en los datos de color.</span><span class="sxs-lookup"><span data-stu-id="e3b13-107">There are various functions in the graphics device interface (GDI) that use or operate on color data.</span></span> <span data-ttu-id="e3b13-108">Las siguientes funciones de mapa de bits están habilitadas para su uso con ICM:</span><span class="sxs-lookup"><span data-stu-id="e3b13-108">The following bitmap functions are enabled for use with ICM:</span></span>

-   [<span data-ttu-id="e3b13-109">**BitBlt**</span><span class="sxs-lookup"><span data-stu-id="e3b13-109">**BitBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)
-   [<span data-ttu-id="e3b13-110">**CreateDIBitmap**</span><span class="sxs-lookup"><span data-stu-id="e3b13-110">**CreateDIBitmap**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)
-   [<span data-ttu-id="e3b13-111">**CreateDIBSection**</span><span class="sxs-lookup"><span data-stu-id="e3b13-111">**CreateDIBSection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)
-   [<span data-ttu-id="e3b13-112">**MaskBlt**</span><span class="sxs-lookup"><span data-stu-id="e3b13-112">**MaskBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)
-   [<span data-ttu-id="e3b13-113">**SetDIBColorTable**</span><span class="sxs-lookup"><span data-stu-id="e3b13-113">**SetDIBColorTable**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)
-   [<span data-ttu-id="e3b13-114">**StretchBlt**</span><span class="sxs-lookup"><span data-stu-id="e3b13-114">**StretchBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)
-   [<span data-ttu-id="e3b13-115">**SetDIBits**</span><span class="sxs-lookup"><span data-stu-id="e3b13-115">**SetDIBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)
-   [<span data-ttu-id="e3b13-116">**SetDIBitsToDevice**</span><span class="sxs-lookup"><span data-stu-id="e3b13-116">**SetDIBitsToDevice**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)
-   [<span data-ttu-id="e3b13-117">**StretchDIBits**</span><span class="sxs-lookup"><span data-stu-id="e3b13-117">**StretchDIBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

 

 
