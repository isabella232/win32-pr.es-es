---
description: .
ms.assetid: 49E0D0C2-E6EC-4849-A44F-36FDEFBB9838
title: Introducción a los gráficos de DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5278e759ea0faf04ac8b247ad3ea1c687dd205c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082736"
---
# <a name="getting-started-with-directx-graphics"></a><span data-ttu-id="b65c2-103">Introducción a los gráficos de DirectX</span><span class="sxs-lookup"><span data-stu-id="b65c2-103">Getting started with DirectX Graphics</span></span>

<span data-ttu-id="b65c2-104">Microsoft DirectX Graphics proporciona un conjunto de API que puede usar para crear juegos y otras aplicaciones multimedia de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b65c2-104">Microsoft DirectX graphics provides a set of APIs that you can use to create games and other high-performance multimedia applications.</span></span> <span data-ttu-id="b65c2-105">DirectX Graphics incluye compatibilidad con gráficos 2D y 3D de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b65c2-105">DirectX graphics includes support for high-performance 2-D and 3-D graphics.</span></span>

<span data-ttu-id="b65c2-106">En el caso de los gráficos 3D, use la API de Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="b65c2-106">For 3-D graphics, use the Microsoft Direct3D 11 API.</span></span> <span data-ttu-id="b65c2-107">Aunque tenga hardware de nivel de Microsoft Direct3D 9 o Microsoft Direct3D 10, puede usar la API de Direct3D 11 y tener como [destino un](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) dispositivo de nivel de \_ característica 9 x o 10 x de nivel de características \_ .</span><span class="sxs-lookup"><span data-stu-id="b65c2-107">Even if you have Microsoft Direct3D 9-level or Microsoft Direct3D 10-level hardware, you can use the Direct3D 11 API and target a [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x or feature level 10\_x device.</span></span> <span data-ttu-id="b65c2-108">Para obtener información sobre cómo desarrollar gráficos 3D con DirectX, vea [crear gráficos 3D con DirectX](/previous-versions/windows/apps/hh465137(v=win.10)
).</span><span class="sxs-lookup"><span data-stu-id="b65c2-108">For info about how to develop 3-D graphics with DirectX, see [Create 3D graphics with DirectX](/previous-versions/windows/apps/hh465137(v=win.10)
).</span></span>

<span data-ttu-id="b65c2-109">En el caso de texto y gráficos 2D, use Direct2D y [DirectWrite](./directwrite/direct-write-portal.md) en lugar de Windows interfaz de dispositivo gráfico (GDI).</span><span class="sxs-lookup"><span data-stu-id="b65c2-109">For 2-D graphics and text, use Direct2D and [DirectWrite](./directwrite/direct-write-portal.md) rather than Windows Graphics Device Interface (GDI).</span></span>

<span data-ttu-id="b65c2-110">Para crear mapas de bits rellenados por Direct3D 11 o Direct2D, use [DirectComposition](./directcomp/directcomposition-portal.md).</span><span class="sxs-lookup"><span data-stu-id="b65c2-110">To compose bitmaps that Direct3D 11 or Direct2D populated, use [DirectComposition](./directcomp/directcomposition-portal.md).</span></span>

<span data-ttu-id="b65c2-111">Para obtener información sobre cómo crear una aplicación de la tienda Windows que use DirectX, consulte [crear la primera aplicación de la tienda Windows con DirectX](/previous-versions/windows/apps/br229580(v=win.10)
).</span><span class="sxs-lookup"><span data-stu-id="b65c2-111">To learn about how to create a Windows Store app that uses DirectX, see [Create your first Windows Store app using DirectX](/previous-versions/windows/apps/br229580(v=win.10)
).</span></span> <span data-ttu-id="b65c2-112">Puede usar la clase [**Windows. UI:: XAML:: Controls:: SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) para crear aplicaciones de DirectX de alto rendimiento con una superposición de la interfaz de usuario XAML.</span><span class="sxs-lookup"><span data-stu-id="b65c2-112">You can use the [**Windows.UI::Xaml::Controls::SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) class to create high-performance DirectX apps with a XAML UI overlay.</span></span> <span data-ttu-id="b65c2-113">Para obtener más información sobre la combinación de XAML y DirectX en una aplicación de Windows, consulte [interoperabilidad de DirectX y XAML](/previous-versions/windows/apps/hh825871(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="b65c2-113">For more info about combining XAML and DirectX in a Windows app, see [DirectX and XAML interop](/previous-versions/windows/apps/hh825871(v=win.10)).</span></span>

<span data-ttu-id="b65c2-114">Para obtener información sobre cómo crear un controlador de pantalla para Windows 8, consulte [el mapa de ruta del modelo de controladores de pantalla de Windows (WDDM)](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo).</span><span class="sxs-lookup"><span data-stu-id="b65c2-114">To learn about how to build a display driver for Windows 8, see [Roadmap for the Windows Display Driver Model (WDDM)](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo).</span></span>

<span data-ttu-id="b65c2-115">Si necesita la documentación de las versiones anteriores de DirectX, consulte [gráficos clásicos de DirectX](/windows/desktop/classic-directx-graphics).</span><span class="sxs-lookup"><span data-stu-id="b65c2-115">If you need the documentation for previous DirectX versions, see [Classic DirectX Graphics](/windows/desktop/classic-directx-graphics).</span></span>


 

 
