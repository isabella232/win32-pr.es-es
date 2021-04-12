---
description: Requisitos generales para el desarrollo de aplicaciones
ms.assetid: 8ac88d6f-fc4b-4253-932d-aaa3c801b18f
title: Requisitos generales para el desarrollo de aplicaciones (API de WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16be9656f72324b8f3687bca72146320561b0d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277610"
---
# <a name="general-requirements-for-application-development-wpd-api"></a><span data-ttu-id="ca553-103">Requisitos generales para el desarrollo de aplicaciones (API de WPD)</span><span class="sxs-lookup"><span data-stu-id="ca553-103">General Requirements for Application Development (WPD API)</span></span>

<span data-ttu-id="ca553-104">Para crear una aplicación de dispositivos portátiles de Windows, debe tener instalado en el equipo el [Kit de desarrollo de software (SDK) de Windows](https://developer.microsoft.com/windows/downloads) .</span><span class="sxs-lookup"><span data-stu-id="ca553-104">To create a Windows Portable Devices application, you must have the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads) installed on your computer.</span></span> <span data-ttu-id="ca553-105">Los encabezados y las bibliotecas necesarios aparecen en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="ca553-105">The required headers and libraries appear in the following list.</span></span>

-   <span data-ttu-id="ca553-106">PortableDeviceGuids. lib</span><span class="sxs-lookup"><span data-stu-id="ca553-106">PortableDeviceGuids.lib</span></span>
-   <span data-ttu-id="ca553-107">PortableDevice. h</span><span class="sxs-lookup"><span data-stu-id="ca553-107">PortableDevice.h</span></span>
-   <span data-ttu-id="ca553-108">PortableDeviceTypes. h</span><span class="sxs-lookup"><span data-stu-id="ca553-108">PortableDeviceTypes.h</span></span>
-   <span data-ttu-id="ca553-109">PortableDeviceApi. h</span><span class="sxs-lookup"><span data-stu-id="ca553-109">PortableDeviceApi.h</span></span>
-   <span data-ttu-id="ca553-110">Cualquier otra biblioteca y encabezado necesarios que necesite la aplicación para consumir o representar archivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="ca553-110">Any other required libraries and headers required by your application to consume or render media files.</span></span>

<span data-ttu-id="ca553-111">Si la aplicación admite las nuevas interfaces de servicios de dispositivo, también incluirá uno o varios de los siguientes archivos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="ca553-111">If your application supports the new Device Services interfaces, it will also include one or more of the following header files.</span></span>

-   <span data-ttu-id="ca553-112">AnchorSyncDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="ca553-112">AnchorSyncDeviceService.h</span></span>
-   <span data-ttu-id="ca553-113">BridgeDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="ca553-113">BridgeDeviceService.h</span></span>
-   <span data-ttu-id="ca553-114">CalendarDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="ca553-114">CalendarDeviceService.h</span></span>
-   <span data-ttu-id="ca553-115">ContactDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="ca553-115">ContactDeviceService.h</span></span>
-   <span data-ttu-id="ca553-116">DeviceServices. h</span><span class="sxs-lookup"><span data-stu-id="ca553-116">DeviceServices.h</span></span>
-   <span data-ttu-id="ca553-117">FullEnumSyncDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="ca553-117">FullEnumSyncDeviceService.h</span></span>
-   <span data-ttu-id="ca553-118">HintsDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="ca553-118">HintsDeviceService.h</span></span>
-   <span data-ttu-id="ca553-119">MessageDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="ca553-119">MessageDeviceService.h</span></span>
-   <span data-ttu-id="ca553-120">MetadataDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="ca553-120">MetadataDeviceService.h</span></span>
-   <span data-ttu-id="ca553-121">NotesDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="ca553-121">NotesDeviceService.h</span></span>
-   <span data-ttu-id="ca553-122">RingtoneDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="ca553-122">RingtoneDeviceService.h</span></span>
-   <span data-ttu-id="ca553-123">StatusDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="ca553-123">StatusDeviceService.h</span></span>
-   <span data-ttu-id="ca553-124">SyncDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="ca553-124">SyncDeviceService.h</span></span>
-   <span data-ttu-id="ca553-125">TaskDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="ca553-125">TaskDeviceService.h</span></span>

<span data-ttu-id="ca553-126">De los archivos de la lista anterior, se necesitan BridgeDeviceService. h y DeviceService. h para casi cualquier aplicación que admita servicios de dispositivo. los otros archivos definen diferentes tipos de servicios de dispositivo y se incluirán según corresponda.</span><span class="sxs-lookup"><span data-stu-id="ca553-126">Of the files in the previous list, BridgeDeviceService.h and DeviceService.h are required for almost any application that supports Device Services; the other files define different types of device services and would be included as appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca553-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ca553-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca553-128">**Dispositivos portátiles de Windows**</span><span class="sxs-lookup"><span data-stu-id="ca553-128">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
