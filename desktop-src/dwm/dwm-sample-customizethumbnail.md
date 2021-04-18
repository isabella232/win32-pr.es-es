---
title: Personalización de una miniatura icónica y un mapa de bits de vista previa dinámica
description: Muestra cómo personalizar una miniatura de iconos y un mapa de bits de vista previa dinámica (también denominado vista previa de inspección).
ms.assetid: 43fe71e7-4e5c-46fb-876b-e26996071665
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 8fceb94727257b51a2e6235cbfcc44b155635343
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105718590"
---
# <a name="customize-an-iconic-thumbnail-and-a-live-preview-bitmap"></a><span data-ttu-id="24599-103">Personalización de una miniatura icónica y un mapa de bits de vista previa dinámica</span><span class="sxs-lookup"><span data-stu-id="24599-103">Customize an Iconic Thumbnail and a Live Preview Bitmap</span></span>

## <a name="description"></a><span data-ttu-id="24599-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="24599-104">Description</span></span>

<span data-ttu-id="24599-105">Puede personalizar una miniatura de iconos y un mapa de bits de *vista previa dinámica* (o *vista previa de PEEK*) mediante el uso de funciones y mensajes que se introducen en las api de Windows 7 administrador de ventanas de escritorio (DWM).</span><span class="sxs-lookup"><span data-stu-id="24599-105">You can customize an iconic thumbnail and a *live preview* (or *Peek preview*) bitmap by using functions and messages that are introduced in the Windows 7 Desktop Window Manager (DWM) APIs.</span></span>

<span data-ttu-id="24599-106">En concreto, use la función [**DwmSetIconicThumbnail**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) y el [**mensaje \_ SENDICONICTHUMBNAILBITMAP de WM**](wm-dwmsendiconicthumbnail.md) para personalizar una miniatura de iconos.</span><span class="sxs-lookup"><span data-stu-id="24599-106">Specifically, you use the [**DwmSetIconicThumbnail**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) function and the [**WM\_SENDICONICTHUMBNAILBITMAP**](wm-dwmsendiconicthumbnail.md) message to customize an iconic thumbnail.</span></span> <span data-ttu-id="24599-107">También puede usar la función [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) y el mensaje [**de \_ SENDICONICLIVEPREVIEWBITMAP de WM**](wm-dwmsendiconiclivepreviewbitmap.md) para establecer un mapa de bits de vista previa de iconos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="24599-107">You can also use the [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function and the [**WM\_SENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md) message to set an iconic live preview bitmap.</span></span>

<span data-ttu-id="24599-108">Para obtener una aplicación de ejemplo que usa la función **DwmSetIconicThumbnail** , vea el [ejemplo TabThumbnails](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).</span><span class="sxs-lookup"><span data-stu-id="24599-108">For a sample application that uses the **DwmSetIconicThumbnail** function, see [TabThumbnails sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).</span></span>

<span data-ttu-id="24599-109">En la ilustración siguiente se muestra una miniatura predeterminada transformada en una miniatura personalizada.</span><span class="sxs-lookup"><span data-stu-id="24599-109">The following illustration shows a default thumbnail transformed into a customized thumbnail.</span></span>

![Ilustración de una imagen en miniatura original y una imagen de miniatura modificada con un mapa de bits personalizado](images/customthumbnail.jpg)

## <a name="requirements"></a><span data-ttu-id="24599-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24599-111">Requirements</span></span>

| <span data-ttu-id="24599-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="24599-112">Requirement</span></span> | <span data-ttu-id="24599-113">Value</span><span class="sxs-lookup"><span data-stu-id="24599-113">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24599-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24599-114">Minimum supported client</span></span> | <span data-ttu-id="24599-115">Windows 7 o Windows Vista con Service Pack 2 (SP2) y la actualización de la plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24599-115">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista</span></span>                          |
| <span data-ttu-id="24599-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24599-116">Minimum supported server</span></span> | <span data-ttu-id="24599-117">Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) y la actualización de la plataforma para Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24599-117">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008</span></span> |
| <span data-ttu-id="24599-118">Windows SDK mínimo</span><span class="sxs-lookup"><span data-stu-id="24599-118">Minimum Windows SDK</span></span>      | [<span data-ttu-id="24599-119">Kit de desarrollo de software (SDK) de Windows para Windows 7</span><span class="sxs-lookup"><span data-stu-id="24599-119">Windows Software Development Kit (SDK) for Windows 7</span></span>](https://msdn.microsoft.com/windows/bb980924.aspx)             |

## <a name="building-the-tabthumbnails-sample"></a><span data-ttu-id="24599-120">Compilación del ejemplo TabThumbnails</span><span class="sxs-lookup"><span data-stu-id="24599-120">Building the TabThumbnails sample</span></span>

<span data-ttu-id="24599-121">**Para compilar el ejemplo mediante Microsoft Visual Studio (método preferido)**</span><span class="sxs-lookup"><span data-stu-id="24599-121">**To build the sample by using Microsoft Visual Studio (preferred method)**</span></span>

1.  <span data-ttu-id="24599-122">Abra el explorador de Windows y vaya a la carpeta donde se encuentra el archivo TabThumbnails. sln.</span><span class="sxs-lookup"><span data-stu-id="24599-122">Open Windows Explorer and browse to the folder where the TabThumbnails.sln file is located.</span></span>
2.  <span data-ttu-id="24599-123">Haga doble clic en el archivo de solución (. sln) para abrir el archivo en Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="24599-123">Double-click the solution file (.sln) to open the file in Microsoft Visual Studio.</span></span>
3.  <span data-ttu-id="24599-124">En el menú **Compilar** , haga clic en **Compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="24599-124">On the **Build** menu, click **Build Solution**.</span></span> <span data-ttu-id="24599-125">La aplicación se genera en el \\ Directorio de depuración o \\ versión predeterminado.</span><span class="sxs-lookup"><span data-stu-id="24599-125">The application is built in the default \\Debug or \\Release directory.</span></span>

<span data-ttu-id="24599-126">**Para generar el ejemplo mediante el símbolo del sistema**</span><span class="sxs-lookup"><span data-stu-id="24599-126">**To build the sample by using the command prompt**</span></span>

1.  <span data-ttu-id="24599-127">Abra una ventana del símbolo del sistema y vaya al directorio de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="24599-127">Open a Command Prompt window and browse to the sample directory.</span></span>
2.  <span data-ttu-id="24599-128">Escriba `msbuild TabThumbnails.sln`.</span><span class="sxs-lookup"><span data-stu-id="24599-128">Enter `msbuild TabThumbnails.sln`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24599-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="24599-129">Related topics</span></span>

[<span data-ttu-id="24599-130">Administrador de ventanas de escritorio</span><span class="sxs-lookup"><span data-stu-id="24599-130">Desktop Window Manager</span></span>](dwm-overview.md)

[<span data-ttu-id="24599-131">Desarrollo de Windows</span><span class="sxs-lookup"><span data-stu-id="24599-131">Windows Development</span></span>](/windows/desktop/win32-and-com-development)
