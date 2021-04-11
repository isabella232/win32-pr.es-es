---
description: Las capacidades de color de los dispositivos, como las pantallas e impresoras, pueden oscilar entre monocromo y miles de colores.
ms.assetid: 3d71c24c-77f4-4344-91c3-439052402fae
title: Conceptos básicos de color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 992953bef75b2bab1f33dbd044a9c80387b5ccd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276017"
---
# <a name="color-basics"></a><span data-ttu-id="9bedb-103">Conceptos básicos de color</span><span class="sxs-lookup"><span data-stu-id="9bedb-103">Color Basics</span></span>

<span data-ttu-id="9bedb-104">Las capacidades de color de los dispositivos, como las pantallas e impresoras, pueden oscilar entre monocromo y miles de colores.</span><span class="sxs-lookup"><span data-stu-id="9bedb-104">The color capabilities of devices, such as displays and printers, can range from monochrome to thousands of colors.</span></span> <span data-ttu-id="9bedb-105">Dado que es posible que una aplicación tenga que generar la salida de los dispositivos a lo largo de este intervalo, debe estar preparado para controlar las diversas funcionalidades de color.</span><span class="sxs-lookup"><span data-stu-id="9bedb-105">Because an application may need to generate output for devices throughout this range, it should be prepared to handle varying color capabilities.</span></span>

<span data-ttu-id="9bedb-106">Una aplicación puede detectar el número de colores disponibles para un dispositivo determinado mediante la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) para recuperar el valor NUMCOLORS.</span><span class="sxs-lookup"><span data-stu-id="9bedb-106">An application can discover the number of colors available for a given device by using the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function to retrieve the NUMCOLORS value.</span></span> <span data-ttu-id="9bedb-107">Este valor especifica el número de colores disponibles para que la aplicación los use.</span><span class="sxs-lookup"><span data-stu-id="9bedb-107">This value specifies the count of colors available for use by the application.</span></span> <span data-ttu-id="9bedb-108">Normalmente, este recuento corresponde a una propiedad física del dispositivo de salida, como el número de tintas de la impresora o el número de señales de color distintas que el adaptador de pantalla puede transmitir al monitor.</span><span class="sxs-lookup"><span data-stu-id="9bedb-108">Usually, this count corresponds to a physical property of the output device, such as the number of inks in the printer or the number of distinct color signals the display adapter can transmit to the monitor.</span></span>

<span data-ttu-id="9bedb-109">Aunque el valor NUMCOLORS especifica el número de colores, no identifica Cuáles son los colores disponibles.</span><span class="sxs-lookup"><span data-stu-id="9bedb-109">Although the NUMCOLORS value specifies the count of colors, it does not identify what the available colors are.</span></span> <span data-ttu-id="9bedb-110">Una aplicación puede detectar qué colores están disponibles enumerando todos los lápices que tienen el \_ tipo sólido de PS.</span><span class="sxs-lookup"><span data-stu-id="9bedb-110">An application can discover what colors are available by enumerating all pens having the PS\_SOLID type.</span></span> <span data-ttu-id="9bedb-111">Dado que el controlador de dispositivo que admite un dispositivo determinado normalmente tiene una gama completa de lápices sólidos y porque el sistema requiere que los lápices sólidos solo tengan colores que el dispositivo pueda generar, la enumeración de estos lápices suele ser equivalente a la enumeración de los colores.</span><span class="sxs-lookup"><span data-stu-id="9bedb-111">Because the device driver that supports a given device usually has a full range of solid pens and because the system requires that solid pens have only colors that the device can generate, enumerating these pens is often equivalent to enumerating the colors.</span></span> <span data-ttu-id="9bedb-112">Una aplicación puede enumerar los lápices mediante la función [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) .</span><span class="sxs-lookup"><span data-stu-id="9bedb-112">An application can enumerate the pens by using the [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) function.</span></span> <span data-ttu-id="9bedb-113">Para obtener un ejemplo de código, vea [enumerar colores](enumerating-colors.md).</span><span class="sxs-lookup"><span data-stu-id="9bedb-113">For a code example, see [Enumerating Colors](enumerating-colors.md).</span></span>

<span data-ttu-id="9bedb-114">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="9bedb-114">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="9bedb-115">Valores de color</span><span class="sxs-lookup"><span data-stu-id="9bedb-115">Color Values</span></span>](color-values.md)
-   [<span data-ttu-id="9bedb-116">Aproximaciones de color y interpolación</span><span class="sxs-lookup"><span data-stu-id="9bedb-116">Color Approximations and Dithering</span></span>](color-approximations-and-dithering.md)
-   [<span data-ttu-id="9bedb-117">Color en mapas de bits</span><span class="sxs-lookup"><span data-stu-id="9bedb-117">Color in Bitmaps</span></span>](color-in-bitmaps.md)
-   [<span data-ttu-id="9bedb-118">Combinación de colores</span><span class="sxs-lookup"><span data-stu-id="9bedb-118">Color Mixing</span></span>](color-mixing.md)

 

 



