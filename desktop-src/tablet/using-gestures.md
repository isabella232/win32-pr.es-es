---
description: Información general sobre el uso de gestos.
ms.assetid: 5bc80086-7acf-4f86-a9fb-a663de489f8b
title: Usar gestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c267cff446d1bb6d092ba50bde21c1b3e25184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001113"
---
# <a name="using-gestures"></a><span data-ttu-id="39864-103">Usar gestos</span><span class="sxs-lookup"><span data-stu-id="39864-103">Using Gestures</span></span>

<span data-ttu-id="39864-104">La plataforma de Tablet PC proporciona el reconocedor de gestos de Microsoft para admitir los gestos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="39864-104">The Tablet PC platform provides the Microsoft gesture recognizer for supporting application gestures.</span></span> <span data-ttu-id="39864-105">Para obtener una lista de los gestos admitidos por el reconocedor de gestos de Microsoft, consulte la tabla de gestos de aplicación en la enumeración [**ApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="39864-105">For a list of gestures supported by the Microsoft gesture recognizer, see the table of application gestures in the [**ApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration.</span></span> <span data-ttu-id="39864-106">Tablet PC también admite gestos del sistema.</span><span class="sxs-lookup"><span data-stu-id="39864-106">The Tablet PC also supports system gestures.</span></span> <span data-ttu-id="39864-107">Para obtener una lista de los gestos del sistema compatibles con Tablet PC, vea la tabla de gestos del sistema en la enumeración [**SystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .</span><span class="sxs-lookup"><span data-stu-id="39864-107">For a list of system gestures supported by the Tablet PC, see the table of system gestures in the [**SystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration.</span></span>

## <a name="microsoft-gesture-recognizer"></a><span data-ttu-id="39864-108">Reconocedor de gestos de Microsoft</span><span class="sxs-lookup"><span data-stu-id="39864-108">Microsoft Gesture Recognizer</span></span>

<span data-ttu-id="39864-109">Puede emplear el reconocedor de gestos de Microsoft mediante la propiedad [**si CollectionMode es**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) del objeto [**InkCollector**](inkcollector-class.md) , el objeto [**InkOverlay**](inkoverlay-class.md) o el control [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="39864-109">You can employ the Microsoft gesture recognizer by using the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) property of the [**InkCollector**](inkcollector-class.md) object, the [**InkOverlay**](inkoverlay-class.md) object, or the [InkPicture](inkpicture-control-reference.md) control.</span></span> <span data-ttu-id="39864-110">De forma predeterminada, al establecer la propiedad **si CollectionMode es** en modo mixto (**InkAndGesture**) o en modo de solo gesto (**GestureOnly**), se pasa la entrada manuscrita al reconocedor de gestos de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="39864-110">Setting the **CollectionMode** property to mixed mode (**InkAndGesture**) or gesture-only mode (**GestureOnly**) passes ink to the Microsoft gesture recognizer by default.</span></span> <span data-ttu-id="39864-111">Puede emplear el reconocedor de gestos de Microsoft con el control [InkEdit](inkedit-control-reference.md) si establece la propiedad [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) en **InkAndGesture**.</span><span class="sxs-lookup"><span data-stu-id="39864-111">You can employ the Microsoft gesture recognizer with the [InkEdit](inkedit-control-reference.md) control by setting the [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property to **InkAndGesture**.</span></span> <span data-ttu-id="39864-112">También puede usar el reconocimiento de gestos con el objeto [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) agregando un objeto [**GestureRecognizer**](gesturerecognizer-class.md) a una de sus colecciones de complementos.</span><span class="sxs-lookup"><span data-stu-id="39864-112">You can also use gesture recognition with the [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) object by adding a [**GestureRecognizer**](gesturerecognizer-class.md) object to one of its plug-in collections.</span></span>

<span data-ttu-id="39864-113">Sin embargo, si los gestos que quiere usar no son compatibles con la versión actual del reconocedor de gestos de Microsoft, puede crear su propio reconocedor y usarlo junto con el reconocedor de gestos de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="39864-113">However, if the gestures that you want to use are not supported by the current version of the Microsoft gesture recognizer, you can build your own recognizer and use it in conjunction with the Microsoft gesture recognizer.</span></span> <span data-ttu-id="39864-114">Esto permite la compatibilidad total con los gestos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39864-114">This allows full support for the gestures in your application.</span></span>

<span data-ttu-id="39864-115">Tablet PC usa un lápiz para algunos o todos los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="39864-115">The Tablet PC uses a pen for some or all input.</span></span> <span data-ttu-id="39864-116">Esto facilita enormemente la escritura de tinta.</span><span class="sxs-lookup"><span data-stu-id="39864-116">This makes it extremely easy to write ink.</span></span> <span data-ttu-id="39864-117">La plataforma de Tablet PC ofrece una arquitectura para la entrada manuscrita que admite una estructura en capas de gestos.</span><span class="sxs-lookup"><span data-stu-id="39864-117">The Tablet PC platform delivers architecture for pen input that supports a tiered structure of gestures.</span></span> <span data-ttu-id="39864-118">Los gestos y la asignación se definen para permitir que el usuario escriba e invoque gestos avanzados en nuevas superficies, al tiempo que se reservan gestos que invoquen los mensajes de mouse tradicionales de otras aplicaciones basadas en Windows.</span><span class="sxs-lookup"><span data-stu-id="39864-118">Gestures and mapping are defined to allow the user to write and invoke advanced gestures on new surfaces, while reserving gestures that invoke traditional mouse messages of other Windows-based applications.</span></span>

<span data-ttu-id="39864-119">La plataforma de Tablet PC presenta dos niveles de gestos: gestos del sistema, también conocidos como eventos del sistema y gestos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="39864-119">The Tablet PC platform introduces two levels of gestures: system gestures, also known as system events, and application gestures.</span></span> <span data-ttu-id="39864-120">La arquitectura del lápiz admite movimientos del sistema y de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39864-120">The pen architecture supports both system and application gestures.</span></span> <span data-ttu-id="39864-121">Se admiten los movimientos de aplicación de un solo trazo y de varios trazos.</span><span class="sxs-lookup"><span data-stu-id="39864-121">Both single-stroke and multiple-stroke application gestures are supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39864-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="39864-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39864-123">Gestos de aplicación</span><span class="sxs-lookup"><span data-stu-id="39864-123">Application Gestures</span></span>](application-gestures.md)
</dt> <dt>

[<span data-ttu-id="39864-124">Gestos de gestos</span><span class="sxs-lookup"><span data-stu-id="39864-124">Flicks Gestures</span></span>](flicks-gestures.md)
</dt> <dt>

[<span data-ttu-id="39864-125">Gestos del sistema</span><span class="sxs-lookup"><span data-stu-id="39864-125">System Gestures</span></span>](system-gestures.md)
</dt> </dl>

 

 



