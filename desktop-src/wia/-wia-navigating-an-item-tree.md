---
description: Una aplicación navega por un árbol de elementos del dispositivo de adquisición de imágenes de Windows (WIA) para buscar y seleccionar imágenes en ese dispositivo. Con esta técnica, una aplicación selecciona y adquiere una imagen sin presentar un cuadro de diálogo al usuario.
ms.assetid: 1f124b4a-45fb-4181-b45a-e810a61ac37d
title: Navegar por un árbol de elementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787ff3b53690ae7db4ff69fd5de2f4f4186f8e43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541934"
---
# <a name="navigating-an-item-tree"></a><span data-ttu-id="b0fbf-104">Navegar por un árbol de elementos</span><span class="sxs-lookup"><span data-stu-id="b0fbf-104">Navigating an Item Tree</span></span>

<span data-ttu-id="b0fbf-105">Una aplicación navega por un árbol de elementos del dispositivo de adquisición de imágenes de Windows (WIA) para buscar y seleccionar imágenes en ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0fbf-105">An application navigates a Windows Image Acquisition (WIA) device's item tree to find and select images on that device.</span></span> <span data-ttu-id="b0fbf-106">Con esta técnica, una aplicación selecciona y adquiere una imagen sin presentar un cuadro de diálogo al usuario.</span><span class="sxs-lookup"><span data-stu-id="b0fbf-106">Using this technique, an application selects and acquires an image without presenting a dialog box to the user.</span></span>

<span data-ttu-id="b0fbf-107">Un dispositivo WIA se representa como el elemento raíz en un árbol de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="b0fbf-107">A WIA device is represented as the root item in a tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="b0fbf-108">Los elementos secundarios del árbol representan las imágenes de una cámara o escanean las camas de un escáner.</span><span class="sxs-lookup"><span data-stu-id="b0fbf-108">The child items in the tree represent images for a camera or scan beds for a scanner.</span></span>

<span data-ttu-id="b0fbf-109">Una vez que se selecciona un dispositivo WIA, una aplicación llama al método [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) de la interfaz [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) del dispositivo para enumerar los elementos secundarios (las imágenes o las camas de digitalización) del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0fbf-109">After a WIA device is selected, an application calls the [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) method of the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) interface of the device to enumerate the child items (the images or scan beds) of the device.</span></span> <span data-ttu-id="b0fbf-110">Para obtener instrucciones, consulte [seleccionar un dispositivo](-wia-selecting-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="b0fbf-110">For instructions, see [Selecting a Device](-wia-selecting-a-device.md).</span></span>

<span data-ttu-id="b0fbf-111">El método [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) crea un objeto de enumeración para los elementos secundarios del dispositivo y devuelve un puntero a la interfaz [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) de ese objeto.</span><span class="sxs-lookup"><span data-stu-id="b0fbf-111">The [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) method creates an enumeration object for the child items of the device, and returns a pointer to that object's [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) interface.</span></span> <span data-ttu-id="b0fbf-112">A continuación, la aplicación puede usar los métodos de la interfaz **IEnumWiaItem** para obtener punteros a los elementos del árbol de elementos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0fbf-112">The application can then use the methods of the **IEnumWiaItem** interface to obtain pointers to the items in the device's item tree.</span></span>

 

 



