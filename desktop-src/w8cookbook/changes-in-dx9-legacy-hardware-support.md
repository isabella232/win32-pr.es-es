---
title: Cambios en la compatibilidad con hardware heredado de DX9
description: Cambios en la compatibilidad con hardware heredado de DX9
ms.assetid: 25C7DFC7-58F4-4F6D-8D26-6DBA92424A0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1ae5c4b15a2019450cc5b209f34561d8ec672d
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "105695776"
---
# <a name="changes-in-dx9-legacy-hardware-support"></a><span data-ttu-id="f2d06-103">Cambios en la compatibilidad con hardware heredado de DX9</span><span class="sxs-lookup"><span data-stu-id="f2d06-103">Changes in DX9 legacy hardware support</span></span>

## <a name="platform"></a><span data-ttu-id="f2d06-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="f2d06-104">Platform</span></span>

<span data-ttu-id="f2d06-105">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="f2d06-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="f2d06-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2d06-106">Description</span></span>

<span data-ttu-id="f2d06-107">Intel y AMD/ATI ya no admiten las piezas de gráficos de DX9 y no actualizarán los controladores de estos dispositivos para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f2d06-107">Intel and AMD/ATI no longer support their DX9 graphics parts and will not be updating drivers for these devices for Windows 8.</span></span> <span data-ttu-id="f2d06-108">Además, estos dispositivos no se incluyen en la caja para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f2d06-108">Furthermore, these devices are not covered in-box for Windows 8.</span></span> <span data-ttu-id="f2d06-109">Los últimos controladores de estos dispositivos son los disponibles en WU y en los sitios web de OEM/IHV; muchas fechas de vista y muchos de estos controladores de versión finales muestran problemas en Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f2d06-109">The last drivers for these devices are those available on WU and on the OEM/IHV’s websites; many date from Vista, and many of these final version drivers exhibit problems on Windows 8.</span></span> <span data-ttu-id="f2d06-110">Además, nVidia ha indicado recientemente que no admitirán sus componentes móviles de DX9 (vista y anterior) para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f2d06-110">In addition, nVidia has recently stated that they will not support their DX9 (Vista and older) mobile (notebook) parts for Windows 8.</span></span> <span data-ttu-id="f2d06-111">Continúan admitiendo sus componentes de su escritorio.</span><span class="sxs-lookup"><span data-stu-id="f2d06-111">They continue to support their desktop DX9 parts.</span></span>

<span data-ttu-id="f2d06-112">Todas estas combinaciones de controlador/parte se encuentran en la lista de reserva de software de Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f2d06-112">All of these driver/part combinations are on the Internet Explorer 9 software fallback list.</span></span> <span data-ttu-id="f2d06-113">Esto significa que, por motivos de rendimiento o de estabilidad, Internet Explorer 9 usa la representación de software en estos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f2d06-113">This means that for either performance or stability reasons, Internet Explorer 9 uses software rendering on these devices.</span></span> <span data-ttu-id="f2d06-114">Esta es una buena indicación de que la experiencia con las aplicaciones de la tienda Windows no será satisfactoria en estos controladores y partes.</span><span class="sxs-lookup"><span data-stu-id="f2d06-114">This is a good indication that the experience with Windows Store apps will not be satisfactory on these drivers and parts.</span></span>

## <a name="manifestation"></a><span data-ttu-id="f2d06-115">Manifestación</span><span class="sxs-lookup"><span data-stu-id="f2d06-115">Manifestation</span></span>

<span data-ttu-id="f2d06-116">Como no hay compatibilidad integrada para estos dispositivos, muchos usuarios con estas partes se cargarán en ejecución en el controlador de pantalla básico de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f2d06-116">As there is no in-box support for these devices, many users with these parts will wind up running on the Microsoft Basic Display Driver.</span></span> <span data-ttu-id="f2d06-117">Se trata de una GPU de software WDDM 1,2 basada en WARP y, en realidad, es más rápida que algunas de las partes de esta clase, por ejemplo, la serie GMA500 de Intel).</span><span class="sxs-lookup"><span data-stu-id="f2d06-117">This is a WARP-based WDDM 1.2 software GPU, and is actually faster than some of the parts in this class, for example, the Intel GMA500 series).</span></span> <span data-ttu-id="f2d06-118">Admite Aero-Glass y DWM, y puede ejecutar aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="f2d06-118">It supports aero-glass and DWM, and can run Windows Store apps.</span></span>

<span data-ttu-id="f2d06-119">Sin embargo, tiene algunas limitaciones importantes:</span><span class="sxs-lookup"><span data-stu-id="f2d06-119">However, it has some important limitations:</span></span>

-   <span data-ttu-id="f2d06-120">No admite varios monitores o proyección</span><span class="sxs-lookup"><span data-stu-id="f2d06-120">It doesn’t support multiple monitors or projection</span></span>
-   <span data-ttu-id="f2d06-121">No admite la suspensión, aunque admite la hibernación</span><span class="sxs-lookup"><span data-stu-id="f2d06-121">It doesn’t support sleep, though it does support hibernation</span></span>
-   <span data-ttu-id="f2d06-122">A menudo, no permite cambiar la resolución de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="f2d06-122">It often will not allow changing screen resolution</span></span>

## <a name="mitigation"></a><span data-ttu-id="f2d06-123">Mitigación</span><span class="sxs-lookup"><span data-stu-id="f2d06-123">Mitigation</span></span>

<span data-ttu-id="f2d06-124">Si después de la prueba, observa que la experiencia del usuario no es aceptable, puede elegir establecer los requisitos de hardware para sus productos que excluyan estas piezas antiguas de Intel y AMD.</span><span class="sxs-lookup"><span data-stu-id="f2d06-124">If after testing, you find that the user experience is not acceptable, you may choose to set hardware requirements for their products that exclude these older DX9 Intel and AMD parts.</span></span> <span data-ttu-id="f2d06-125">También puede optar por avisar a los clientes de que pueden tener una experiencia inaceptable en estas partes.</span><span class="sxs-lookup"><span data-stu-id="f2d06-125">You may also choose to alert your customers that they may have an unacceptable experience on these parts.</span></span>

## <a name="tests"></a><span data-ttu-id="f2d06-126">Pruebas</span><span class="sxs-lookup"><span data-stu-id="f2d06-126">Tests</span></span>

<span data-ttu-id="f2d06-127">Evalúe el rendimiento y la experiencia en estos dispositivos:</span><span class="sxs-lookup"><span data-stu-id="f2d06-127">Evaluate the performance and experience on these devices:</span></span>

-   <span data-ttu-id="f2d06-128">¿Cuál es la experiencia como en la versión de controlador final disponible?</span><span class="sxs-lookup"><span data-stu-id="f2d06-128">What is the experience like on the final driver version available?</span></span>
-   <span data-ttu-id="f2d06-129">¿Cuál es la experiencia como en el MSBDD?</span><span class="sxs-lookup"><span data-stu-id="f2d06-129">What is the experience like on the MSBDD?</span></span>

 

 




