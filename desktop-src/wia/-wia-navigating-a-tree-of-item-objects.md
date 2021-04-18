---
description: Más información sobre cómo navegar por un árbol de objetos de elemento
ms.assetid: e91f72c8-3ad6-49e8-88cc-aa99c13cd4c2
title: Navegar por un árbol de objetos de elemento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 04e87444c2b9c473268c5e97dd9c26d04d95b93b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715187"
---
# <a name="navigating-a-tree-of-item-objects"></a><span data-ttu-id="42249-103">Navegar por un árbol de objetos de elemento</span><span class="sxs-lookup"><span data-stu-id="42249-103">Navigating a Tree of Item Objects</span></span>

> [!Note]  
> <span data-ttu-id="42249-104">Este sistema de scripting se ha reemplazado por el nivel de automatización de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="42249-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="42249-105">Consulte [nivel de automatización de adquisición de imágenes de Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="42249-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="42249-106">Una aplicación o un script navega por un árbol de elementos del dispositivo de adquisición de imágenes de Windows (WIA) para buscar y seleccionar imágenes en ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42249-106">An application or script navigates a Windows Image Acquisition (WIA) device's item tree to find and select images on that device.</span></span> <span data-ttu-id="42249-107">Con esta técnica, una aplicación selecciona y adquiere una imagen sin el uso de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="42249-107">Using this technique, an application selects and acquires an image without the use of a dialog box.</span></span>

<span data-ttu-id="42249-108">Un dispositivo WIA se representa como el elemento raíz en un árbol de objetos de [**elemento**](-wia-item.md) .</span><span class="sxs-lookup"><span data-stu-id="42249-108">A WIA device is represented as the root item in a tree of [**Item**](-wia-item.md) objects.</span></span> <span data-ttu-id="42249-109">Los elementos secundarios en el árbol representan carpetas e imágenes para una cámara o escanear camas para un escáner.</span><span class="sxs-lookup"><span data-stu-id="42249-109">The child items in the tree represent folders and images for a camera or scan beds for a scanner.</span></span>

<span data-ttu-id="42249-110">Después de conectarse a un dispositivo, llame a la propiedad [**Children**](-wia-iwiadispatchitem-children.md) del objeto de [**elemento**](-wia-item.md) que representa el dispositivo (el elemento raíz del árbol) para obtener una colección de los elementos secundarios (las imágenes o las camas de digitalización) del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42249-110">After connecting to a device, call the [**Children**](-wia-iwiadispatchitem-children.md) property of the [**Item**](-wia-item.md) object that represents the device (the root item of the tree) to obtain a collection of the child items (the images or scan beds) of the device.</span></span>

<span data-ttu-id="42249-111">Enumerar esta colección (de forma recursiva, si es necesario) para navegar por el árbol de elementos.</span><span class="sxs-lookup"><span data-stu-id="42249-111">Enumerate this collection (recursively, if necessary) to navigate item tree.</span></span>

 

 
