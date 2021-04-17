---
title: Aplicación de punto de control de usuario genérico
description: La aplicación de punto de control de usuario (UCP) genérico permite detectar dispositivos, controlar esos dispositivos detectados y ver la información de eventos relacionados, todo ello mediante una interfaz gráfica.
ms.assetid: 18ac23df-9d69-4a28-91e5-991eb4f3e6ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee56710cc1fafcc8551b34cb53df531f1f8cb601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104566591"
---
# <a name="generic-user-control-point-application"></a><span data-ttu-id="a5187-103">Aplicación de punto de control de usuario genérico</span><span class="sxs-lookup"><span data-stu-id="a5187-103">Generic User Control Point Application</span></span>

<span data-ttu-id="a5187-104">La aplicación de punto de control de usuario (UCP) genérico permite detectar dispositivos, controlar esos dispositivos detectados y ver la información de eventos relacionados, todo ello mediante una interfaz gráfica.</span><span class="sxs-lookup"><span data-stu-id="a5187-104">The generic user control point (UCP) application allows you to discover devices, control those discovered devices, and view the related eventing information, all using a graphical interface.</span></span>

<span data-ttu-id="a5187-105">**Para iniciar la aplicación de UCP genérica**</span><span class="sxs-lookup"><span data-stu-id="a5187-105">**To start the generic UCP application**</span></span>

1.  <span data-ttu-id="a5187-106">Cree y configure el \\ archivo Samples netds \\ UPnP \\ GenericUCP \\ CPP \\devtype.txt (o el \\ archivo dedevtype.txt de VisualBasic \\ ) con la información del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5187-106">Create and configure the samples\\netds\\upnp\\GenericUCP\\CPP\\devtype.txt file (or the \\VisualBasic\\devtype.txt file) with device information.</span></span> <span data-ttu-id="a5187-107">Este archivo le permite configurar el UCP genérico para las búsquedas "Buscar por tipo" y "búsqueda asincrónica".</span><span class="sxs-lookup"><span data-stu-id="a5187-107">This file allows you to configure the generic UCP for the "find by type" and "async find" searches.</span></span> <span data-ttu-id="a5187-108">Cada línea del archivo debe contener un tipo de dispositivo y la descripción relacionada.</span><span class="sxs-lookup"><span data-stu-id="a5187-108">Each line of the file must contain a device type and the related description.</span></span> <span data-ttu-id="a5187-109">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a5187-109">For example:</span></span>

    ``` syntax
    upnp:rootdevice All Root Devices
    urn:schemas-upnp-org:device:mediaplayer:1    Media Player
    ```

    <span data-ttu-id="a5187-110">Este ejemplo es para un dispositivo de reproductor multimedia ficticio.</span><span class="sxs-lookup"><span data-stu-id="a5187-110">This example is for a fictitious media player device.</span></span> <span data-ttu-id="a5187-111">La "Media Player" al final de la segunda línea no forma parte del tipo de dispositivo, sino con fines informativos en la aplicación de UCP genérica.</span><span class="sxs-lookup"><span data-stu-id="a5187-111">The "Media Player" at the end of the second line is not a part of the device type, it is for informational purposes in the Generic UCP application.</span></span> <span data-ttu-id="a5187-112">Lo mismo se aplica a "todos los dispositivos raíz" en la primera línea.</span><span class="sxs-lookup"><span data-stu-id="a5187-112">The same applies to "All Root Devices" in the first line.</span></span>

    <span data-ttu-id="a5187-113">Agregue una línea que contenga su tipo de dispositivo específico y la descripción de cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5187-113">Add a line that contains your specific device type and description for each device.</span></span>

2.  <span data-ttu-id="a5187-114">Cree y configure el \\ archivo Samples netds \\ UPnP \\ GenericUCP \\ CPP \\udn.txt (o el \\ archivo deudn.txt de VisualBasic \\ ) con información de UDN para los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a5187-114">Create and configure the samples\\netds\\upnp\\GenericUCP\\CPP\\udn.txt file (or the \\VisualBasic\\udn.txt file) with UDN information for your devices.</span></span> <span data-ttu-id="a5187-115">Este archivo le permite configurar el UCP genérico para la búsqueda "Buscar por UDN".</span><span class="sxs-lookup"><span data-stu-id="a5187-115">This file allows you to configure the generic UCP for the "find by UDN" search.</span></span> <span data-ttu-id="a5187-116">Cada línea utiliza el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="a5187-116">Each line uses the following form:</span></span>

    ``` syntax
    uuid:{7d50b574-4213-4b88-84d9-e5c9241fcb3a}
    ```

    <span data-ttu-id="a5187-117">Agregue una línea que contenga su UDN específico para cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5187-117">Add a line that contains your specific UDN for each device.</span></span>

3.  <span data-ttu-id="a5187-118">Ejecute GenericUCP.exe.</span><span class="sxs-lookup"><span data-stu-id="a5187-118">Run GenericUCP.exe.</span></span> <span data-ttu-id="a5187-119">Aparece la ventana de **UCP genérica** .</span><span class="sxs-lookup"><span data-stu-id="a5187-119">The **Generic UCP** window appears.</span></span>

    ![ventana de UCP genérica](images/generic-ucp.png)

> [!Note]  
> <span data-ttu-id="a5187-121">La funcionalidad **ver presentación** y **Ver servicio desc.** no se implementa en el código de ejemplo de C++.</span><span class="sxs-lookup"><span data-stu-id="a5187-121">The **View Presentation** and **View Service Desc.** functionality is not implemented in the C++ sample code.</span></span>

 

 

 




