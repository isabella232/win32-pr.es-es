---
description: La adquisición de imágenes de Windows (WIA) proporciona objetos de automatización para su uso en lenguajes de scripting, como el software de desarrollo de Microsoft JScript y Microsoft Visual Basic Scripting Edition (VBScript), y lenguajes de programación de alto nivel, como el sistema de desarrollo de Microsoft Visual Basic.
ms.assetid: 3d294db3-3349-4b26-aae1-1e3f588a0f0e
title: Modelo de scripting de WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e70863e60e0d7aa6172bd9c93240f38cac27c6be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715173"
---
# <a name="wia-scripting-model"></a><span data-ttu-id="3055b-103">Modelo de scripting de WIA</span><span class="sxs-lookup"><span data-stu-id="3055b-103">WIA Scripting Model</span></span>

<span data-ttu-id="3055b-104">La adquisición de imágenes de Windows (WIA) proporciona objetos de automatización para su uso en lenguajes de scripting, como el software de desarrollo de Microsoft JScript y Microsoft Visual Basic Scripting Edition (VBScript), y lenguajes de programación de alto nivel, como el sistema de desarrollo de Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3055b-104">Windows Image Acquisition (WIA) provides automation objects for use in scripting languages, such as Microsoft JScript and Microsoft Visual Basic Scripting Edition (VBScript) development software, and high-level programming languages such as Microsoft Visual Basic development system.</span></span>

> [!Note]  
> <span data-ttu-id="3055b-105">Este sistema de scripting se ha reemplazado por el nivel de automatización de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="3055b-105">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="3055b-106">Consulte [nivel de automatización de adquisición de imágenes de Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="3055b-106">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="3055b-107">En la tabla siguiente se describen los objetos de scripting de WIA y cómo se usan.</span><span class="sxs-lookup"><span data-stu-id="3055b-107">The following table describes WIA scripting objects and how they are used.</span></span> 

| <span data-ttu-id="3055b-108">Object</span><span class="sxs-lookup"><span data-stu-id="3055b-108">Object</span></span>                                | <span data-ttu-id="3055b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3055b-109">Description</span></span>                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3055b-110">**WIA**</span><span class="sxs-lookup"><span data-stu-id="3055b-110">**Wia**</span></span>](-wia-wia.md)               | <span data-ttu-id="3055b-111">Objeto de scripting de WIA de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="3055b-111">The top-level WIA scripting object.</span></span> <span data-ttu-id="3055b-112">Use el objeto [**WIA**](-wia-wia.md) para enumerar y conectarse a los dispositivos, así como para controlar los eventos de los dispositivos de hardware.</span><span class="sxs-lookup"><span data-stu-id="3055b-112">Use the [**Wia**](-wia-wia.md) object to enumerate and connect to devices, and to handle hardware device events.</span></span>                                        |
| [<span data-ttu-id="3055b-113">**DeviceInfo**</span><span class="sxs-lookup"><span data-stu-id="3055b-113">**DeviceInfo**</span></span>](-wia-deviceinfo.md) | <span data-ttu-id="3055b-114">El objeto [**DeviceInfo**](-wia-deviceinfo.md) proporciona acceso a información sobre las propiedades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3055b-114">The [**DeviceInfo**](-wia-deviceinfo.md) object provides access to information about device properties.</span></span>                                                                                     |
| [<span data-ttu-id="3055b-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3055b-115">**Item**</span></span>](-wia-item.md)             | <span data-ttu-id="3055b-116">Este objeto representa los elementos de dispositivo, archivo y carpeta de WIA.</span><span class="sxs-lookup"><span data-stu-id="3055b-116">This object represents WIA device, file, and folder items.</span></span> <span data-ttu-id="3055b-117">Un dispositivo de hardware WIA y sus imágenes o escaneado de lecho se representan como un árbol jerárquico de objetos de [**elemento**](-wia-item.md) .</span><span class="sxs-lookup"><span data-stu-id="3055b-117">A WIA hardware device and its images or scanning beds is represented as a hierarchical tree of [**Item**](-wia-item.md) objects.</span></span> |



 

<span data-ttu-id="3055b-118">Tanto el objeto [**DeviceInfo**](-wia-deviceinfo.md) como el objeto [**Item**](-wia-item.md) están asociados a objetos de colección.</span><span class="sxs-lookup"><span data-stu-id="3055b-118">Both the [**DeviceInfo**](-wia-deviceinfo.md) object and the [**Item**](-wia-item.md) object are associated with collection objects.</span></span> <span data-ttu-id="3055b-119">Para obtener información sobre el uso de objetos de colección, vea usar objetos de colección de WIA.</span><span class="sxs-lookup"><span data-stu-id="3055b-119">For information about using collection objects, see Using WIA Collection Objects.</span></span>

<span data-ttu-id="3055b-120">En los siguientes temas se incluye información general sobre el uso del modelo de scripting de WIA:</span><span class="sxs-lookup"><span data-stu-id="3055b-120">The following topics cover general information about using the WIA scripting model:</span></span>

-   [<span data-ttu-id="3055b-121">Convenciones de sintaxis</span><span class="sxs-lookup"><span data-stu-id="3055b-121">Syntax Conventions</span></span>](-wia-syntax-conventions.md)
-   [<span data-ttu-id="3055b-122">Usar objetos de colección de WIA</span><span class="sxs-lookup"><span data-stu-id="3055b-122">Using WIA Collection Objects</span></span>](-wia-using-wia-collection-objects.md)
-   [<span data-ttu-id="3055b-123">Definiciones de constantes de propiedades de WIA</span><span class="sxs-lookup"><span data-stu-id="3055b-123">WIA Property Constant Definitions</span></span>](-wia-wia-property-constant-definitions.md)

 

 
