---
description: Tema de referencia sobre el control InkPicture para Tablet PC.
ms.assetid: 1ced9779-dae5-4f9a-8a68-b2c0d041d5b4
title: InkPicture (control)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded5295d48e4bb14b3c0d83713f33939a360cff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668391"
---
# <a name="inkpicture-control"></a><span data-ttu-id="de9c8-103">InkPicture (control)</span><span class="sxs-lookup"><span data-stu-id="de9c8-103">InkPicture Control</span></span>

<span data-ttu-id="de9c8-104">El control [InkPicture](inkpicture-control-reference.md) le permite colocar una imagen (formato. jpg,. bmp,. png o. gif) en una aplicación a la que los usuarios pueden agregar tinta.</span><span class="sxs-lookup"><span data-stu-id="de9c8-104">The [InkPicture](inkpicture-control-reference.md) control enables you to place an image (.jpg, .bmp, .png, or .gif format) in an application that users can add ink to.</span></span> <span data-ttu-id="de9c8-105">Está diseñado para escenarios en los que no es necesario reconocer la tinta como texto, sino que se almacena como entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="de9c8-105">It is intended for scenarios in which ink need not be recognized as text but is stored as ink.</span></span>

<span data-ttu-id="de9c8-106">Los usuarios agregan tinta a una capa transparente con un lápiz.</span><span class="sxs-lookup"><span data-stu-id="de9c8-106">Users add ink to a transparent layer using a pen.</span></span> <span data-ttu-id="de9c8-107">Los usuarios pueden cambiar el tamaño de una ventana de [InkPicture](inkpicture-control-reference.md) sin perder ninguna información de la tinta, incluso si se recorta la tinta al cambiar el tamaño.</span><span class="sxs-lookup"><span data-stu-id="de9c8-107">Users can re-size an [InkPicture](inkpicture-control-reference.md) window without losing any ink information, even if the ink is cropped when re-sizing.</span></span>

<span data-ttu-id="de9c8-108">El control [InkPicture](inkpicture-control-reference.md) incluye compatibilidad básica con la impresión. sin embargo, depende de usted implementar la vista previa de impresión u otras capacidades de impresión avanzadas.</span><span class="sxs-lookup"><span data-stu-id="de9c8-108">The [InkPicture](inkpicture-control-reference.md) control includes basic printing support; however, it is up to you to implement print preview or other advanced printing capabilities.</span></span>

<span data-ttu-id="de9c8-109">La implementación administrada (.NET Framework) de [InkPicture](/previous-versions/ms583740(v=vs.100)) hereda de la clase [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="de9c8-109">The managed (.NET Framework) implementation of [InkPicture](/previous-versions/ms583740(v=vs.100)) inherits from the [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) class.</span></span>

<span data-ttu-id="de9c8-110">De forma predeterminada, la tinta está coloreada en negro Si no está en modo de contraste alto; de lo contrario, se establece en el valor de la configuración de color del sistema actual (COLOR \_ WINDOWTEXT).</span><span class="sxs-lookup"><span data-stu-id="de9c8-110">By default, ink is colored black if not in high-contrast mode; otherwise, it is set to the current system color setting (COLOR\_WINDOWTEXT) value.</span></span> <span data-ttu-id="de9c8-111">Además, de forma predeterminada, [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) es **false**.</span><span class="sxs-lookup"><span data-stu-id="de9c8-111">Also, by default [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) is **FALSE**.</span></span>

<span data-ttu-id="de9c8-112">En el control [InkPicture](inkpicture-control-reference.md) , use el objeto de [**entrada manuscrita**](inkdisp-class.md) para cargar y guardar la entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="de9c8-112">Within the [InkPicture](inkpicture-control-reference.md) control, use the [**Ink**](inkdisp-class.md) object to load and save ink.</span></span>

> [!Note]  
> <span data-ttu-id="de9c8-113">Cuando se establece [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) en **Delete** o **Select**, se desencadenan otros eventos (como el evento [**Stroke**](inkpicture-stroke.md) ).</span><span class="sxs-lookup"><span data-stu-id="de9c8-113">When you set the [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) to **Delete** or **Select**, other events (such as the [**Stroke**](inkpicture-stroke.md) event) are triggered.</span></span> <span data-ttu-id="de9c8-114">Estos eventos son útiles si desea implementar sus propios modos de eliminación o selección.</span><span class="sxs-lookup"><span data-stu-id="de9c8-114">These events are useful if you want to implement your own delete or select modes.</span></span>

 

<span data-ttu-id="de9c8-115">Para obtener información de referencia detallada sobre el control [InkPicture](inkpicture-control-reference.md) , vea InkPicture.</span><span class="sxs-lookup"><span data-stu-id="de9c8-115">For detailed reference information about the [InkPicture](inkpicture-control-reference.md) control, see InkPicture.</span></span>

<span data-ttu-id="de9c8-116">En las secciones siguientes se detalla el uso del control [InkPicture](inkpicture-control-reference.md) :</span><span class="sxs-lookup"><span data-stu-id="de9c8-116">The following sections detail the use of the [InkPicture](inkpicture-control-reference.md) control:</span></span>

-   [<span data-ttu-id="de9c8-117">Trabajar con imágenes</span><span class="sxs-lookup"><span data-stu-id="de9c8-117">Working with Pictures</span></span>](working-with-pictures.md)
-   [<span data-ttu-id="de9c8-118">Usar InkPicture en versiones anteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="de9c8-118">Using InkPicture on Earlier Versions of Windows</span></span>](using-inkpicture-on-earlier-versions-of-windows.md)

 

 
