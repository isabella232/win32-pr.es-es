---
title: Detección de dispositivos
description: Puede buscar dispositivos de tres maneras por tipo, por UDN, y por búsqueda asincrónica (que es una búsqueda por tipo de dispositivo).
ms.assetid: 511fb119-ad4e-406a-8a1e-fb508eceff2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055d08db76edd5bcc5591d3254613462c00fc974
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903777"
---
# <a name="discovering-devices"></a><span data-ttu-id="451be-103">Detección de dispositivos</span><span class="sxs-lookup"><span data-stu-id="451be-103">Discovering Devices</span></span>

<span data-ttu-id="451be-104">Puede buscar dispositivos de tres maneras: por tipo, por UDN, y por búsqueda asincrónica (que es una búsqueda por tipo de dispositivo).</span><span class="sxs-lookup"><span data-stu-id="451be-104">You can search for devices in three ways: by type, by UDN, and by asynchronous search (which is a search by device type).</span></span>

![ventana detectar dispositivos](images/ucp-disc.png)

<span data-ttu-id="451be-106">**Para detectar dispositivos**</span><span class="sxs-lookup"><span data-stu-id="451be-106">**To discover devices**</span></span>

1.  <span data-ttu-id="451be-107">Seleccione el tipo de búsqueda que quiere usar: **Buscar por tipo**, **Buscar por UDN** o **Async Find**.</span><span class="sxs-lookup"><span data-stu-id="451be-107">Select the type of search you want to use: **Find by Type**, **Find by UDN**, or **Async Find**.</span></span>
2.  <span data-ttu-id="451be-108">Seleccione el tipo de dispositivo o UDN que desea buscar en la lista (para búsquedas por tipo o por UDN).</span><span class="sxs-lookup"><span data-stu-id="451be-108">Select the type of device or the UDN you want to find from the list (for searches by type or by UDN).</span></span> <span data-ttu-id="451be-109">El contenido de la lista se basa en el contenido de los archivos udn.txt y devtype.txt que editó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="451be-109">The contents of the list is based on the contents of the udn.txt and devtype.txt files you edited earlier.</span></span>
3.  <span data-ttu-id="451be-110">Haga clic en **Iniciar detección**.</span><span class="sxs-lookup"><span data-stu-id="451be-110">Click **Start Discovery**.</span></span> <span data-ttu-id="451be-111">La búsqueda se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="451be-111">The search is started.</span></span> <span data-ttu-id="451be-112">Los resultados se muestran en la lista **dispositivos encontrados** .</span><span class="sxs-lookup"><span data-stu-id="451be-112">The results are displayed in the **Devices Found** list.</span></span> <span data-ttu-id="451be-113">Si no se encuentra ningún dispositivo, se muestra un mensaje que indica esta condición.</span><span class="sxs-lookup"><span data-stu-id="451be-113">If no devices are found, a message is displayed indicating this condition.</span></span> <span data-ttu-id="451be-114">El estado del progreso de la búsqueda se muestra en el campo **Estado** .</span><span class="sxs-lookup"><span data-stu-id="451be-114">The status of the search progress is displayed in the **Status** field.</span></span>

<span data-ttu-id="451be-115">Cuando se usa la búsqueda asincrónica, los nuevos dispositivos encontrados se muestran en la lista **dispositivos encontrados** y en la barra de **Estado** .</span><span class="sxs-lookup"><span data-stu-id="451be-115">When you use the asynchronous search, new devices that are found are displayed in the **Devices Found** list and in the **Status** bar.</span></span> <span data-ttu-id="451be-116">Una vez finalizada la búsqueda asincrónica, la barra de **Estado** muestra un mensaje que indica esto.</span><span class="sxs-lookup"><span data-stu-id="451be-116">When the asynchronous search is finished, the **Status** bar displays a message noting this.</span></span> <span data-ttu-id="451be-117">Sin embargo, dado que una búsqueda asincrónica se ejecuta hasta que se detiene manualmente, aparecen nuevos dispositivos en la lista **dispositivos encontrados** y en la barra de **Estado** a medida que los dispositivos aparecen en la red.</span><span class="sxs-lookup"><span data-stu-id="451be-117">However, because an asynchronous search runs until it is manually stopped, new devices appear in the **Devices Found** list and the **Status** bar as the devices appear on the network.</span></span>

<span data-ttu-id="451be-118">Una vez que haya detectado dispositivos, puede [controlarlos](controlling-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="451be-118">Once you have discovered devices, you can [control them](controlling-a-device.md).</span></span>

 

 




