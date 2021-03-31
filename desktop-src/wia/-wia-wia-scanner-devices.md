---
description: El dispositivo de analizador de adquisición de imágenes de Windows (WIA) se implementa como un árbol jerárquico de objetos IWiaItem.
ms.assetid: d716faec-9ace-422d-b6eb-ad4d86c1b0fd
title: Dispositivos WIA Scanner en WIA 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443277b0b580a481b523739cd5bc21642d827252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809968"
---
# <a name="wia-scanner-devices-in-wia-10"></a><span data-ttu-id="9552d-103">Dispositivos WIA Scanner en WIA 1,0</span><span class="sxs-lookup"><span data-stu-id="9552d-103">WIA Scanner Devices in WIA 1.0</span></span>

> [!Note]  
> <span data-ttu-id="9552d-104">En este tema se describe el árbol de dispositivos del escáner para las aplicaciones que usan el servicio de adquisición de imágenes de Windows (WIA) 1,0 (que es compatible con Windows XP o versiones anteriores).</span><span class="sxs-lookup"><span data-stu-id="9552d-104">This topic discusses the scanner device tree for applications that use the Windows Image Acquisition (WIA) 1.0 service (which is supported on Windows XP or earlier).</span></span> <span data-ttu-id="9552d-105">Para obtener información sobre el árbol de dispositivos de elementos de adquisición de imágenes de Windows (WIA) 2,0 (que son compatibles con Windows Vista o versiones posteriores), consulte [acerca del árbol de elementos IWiaItem2](-wia-about-item-tree.md).</span><span class="sxs-lookup"><span data-stu-id="9552d-105">For information on the device tree of Windows Image Acquisition (WIA) 2.0 items (which are supported on Windows Vista or later), see [About the IWiaItem2 Item Tree](-wia-about-item-tree.md).</span></span>

 

<span data-ttu-id="9552d-106">El dispositivo de analizador de adquisición de imágenes de Windows (WIA) se implementa como un árbol jerárquico de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="9552d-106">The Windows Image Acquisition (WIA) scanner device is implemented as a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) objects.</span></span> <span data-ttu-id="9552d-107">En el elemento raíz, una aplicación puede:</span><span class="sxs-lookup"><span data-stu-id="9552d-107">From the root item an application may:</span></span>

-   <span data-ttu-id="9552d-108">Capacidades del analizador de consultas</span><span class="sxs-lookup"><span data-stu-id="9552d-108">Query scanner capabilities</span></span>
-   <span data-ttu-id="9552d-109">Establecer propiedades de dispositivo de escáner</span><span class="sxs-lookup"><span data-stu-id="9552d-109">Set scanner device properties</span></span>
-   <span data-ttu-id="9552d-110">Controlar el alimentador de documentos</span><span class="sxs-lookup"><span data-stu-id="9552d-110">Control the document feeder</span></span>

<span data-ttu-id="9552d-111">Un dispositivo WIA Scanner es diferente de un dispositivo de cámara WIA porque, en general, no almacena varias imágenes en la memoria.</span><span class="sxs-lookup"><span data-stu-id="9552d-111">A WIA scanner device is different from a WIA camera device because, in general, it does not store multiple images in memory.</span></span>

<span data-ttu-id="9552d-112">Debajo del elemento raíz, un objeto Scanner típico tiene un objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) único que representa la funcionalidad de recopilación de datos del dispositivo, el elemento de examen.</span><span class="sxs-lookup"><span data-stu-id="9552d-112">Underneath the root item, a typical scanner object has a single [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object that represents the data collecting functionality of the device, the Scan Item.</span></span> <span data-ttu-id="9552d-113">Este elemento tiene la marca [**WiaItemTypeFile**](-wia-wia-item-type-flags.md) establecida para indicar que las transferencias de datos en este elemento son posibles.</span><span class="sxs-lookup"><span data-stu-id="9552d-113">This item has the [**WiaItemTypeFile**](-wia-wia-item-type-flags.md) flag set to indicate that data transfers on this item are possible.</span></span> <span data-ttu-id="9552d-114">Una aplicación configura un examen mediante el establecimiento de las propiedades del elemento de análisis y, a continuación, realiza el análisis y transfiere los datos mediante una interfaz de transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="9552d-114">An application sets up a scan by setting the properties of the scan item, then performs the scan and transfers the data using a data transfer interface.</span></span>

<span data-ttu-id="9552d-115">En el diagrama siguiente se ilustra la implementación de WIA para un escáner típico:</span><span class="sxs-lookup"><span data-stu-id="9552d-115">The following diagram illustrates the WIA implementation for a typical scanner:</span></span>

![implementación de WIA de un escáner típico](images/wiscantr.gif)

<span data-ttu-id="9552d-117">Un escáner dúplex normal se representa en WIA con un objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="9552d-117">A typical duplex scanner is represented in WIA by having one [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object.</span></span> <span data-ttu-id="9552d-118">Se tiene acceso a los datos de la página frontal y posterior secuencialmente una transferencia de datos por página.</span><span class="sxs-lookup"><span data-stu-id="9552d-118">Front- and back-page data is accessed sequentially one data transfer per page.</span></span> <span data-ttu-id="9552d-119">Por lo tanto, la representación de un escáner dúplex es idéntica a la representación de un escáner típico.</span><span class="sxs-lookup"><span data-stu-id="9552d-119">Therefore, the representation of a duplex scanner is identical to the representation of a typical scanner.</span></span>

<span data-ttu-id="9552d-120">Un escáner de diapositivas capaz de digitalizar varias diapositivas en una sola operación de examen representa cada imagen independiente como un objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) independiente.</span><span class="sxs-lookup"><span data-stu-id="9552d-120">A slide scanner capable of scanning multiple slides in a single scan operation represents each separate image as a separate [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object.</span></span>

<span data-ttu-id="9552d-121">En el diagrama siguiente se muestra la representación de WIA de un escáner de diapositivas:</span><span class="sxs-lookup"><span data-stu-id="9552d-121">The following diagram illustrates the WIA representation of a slide scanner:</span></span>

![escáner de diapositivas](images/wislscan.gif)

 

 



