---
description: La interfaz IWiaPropertyStorage proporciona métodos para leer y escribir las propiedades de un elemento de adquisición de imágenes de Windows (WIA). Las propiedades del elemento incluyen comandos del dispositivo, información de formato del elemento e información del dispositivo.
ms.assetid: 268d2298-bc9c-479b-b078-a8180cd38bc3
title: Leer y establecer propiedades de WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51df3e8fdb4b29abb6f64743ab8f7f2dd3776358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154388"
---
# <a name="reading-and-setting-wia-properties"></a><span data-ttu-id="b2a59-104">Leer y establecer propiedades de WIA</span><span class="sxs-lookup"><span data-stu-id="b2a59-104">Reading and Setting WIA Properties</span></span>

<span data-ttu-id="b2a59-105">La interfaz [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) proporciona métodos para leer y escribir las propiedades de un elemento de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="b2a59-105">The [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface provides methods for reading and writing a Windows Image Acquisition (WIA) item's properties.</span></span> <span data-ttu-id="b2a59-106">Las propiedades del elemento incluyen comandos del dispositivo, información de formato del elemento e información del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2a59-106">Item properties include device commands, item format information, and device information.</span></span>

<span data-ttu-id="b2a59-107">Una aplicación puede obtener un puntero a una interfaz [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) de un elemento, ya sea enumerando la información del dispositivo o la información del evento del elemento llamando a [**IWiaItem:: EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) o [**IWiaItem:: EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) o consultando la interfaz [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) del elemento.</span><span class="sxs-lookup"><span data-stu-id="b2a59-107">An application can obtain a pointer to an [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface of an item either by enumerating the item's device information or event information by calling [**IWiaItem::EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) or [**IWiaItem::EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) or by querying the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface of the item.</span></span> <span data-ttu-id="b2a59-108">(En WIA 2,0, haga esto llamando a [**IWiaItem2:: EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) o [**IWiaItem2:: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) o consultando la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) del elemento).</span><span class="sxs-lookup"><span data-stu-id="b2a59-108">(In WIA 2.0, do this by calling [**IWiaItem2::EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) or [**IWiaItem2::EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) or by querying the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item.)</span></span>

<span data-ttu-id="b2a59-109">[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) hereda de [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) y los métodos heredados se implementan como se describe en la sección de referencia de almacenamiento estructurado en el kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="b2a59-109">[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) inherits from [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) and the inherited methods are implemented as described in the reference section of Structured Storage in the Windows Software Development Kit (SDK).</span></span>

> [!Note]
>
> <span data-ttu-id="b2a59-110">Las aplicaciones WIA siempre deberían leer los encabezados de datos de imagen para obtener información precisa sobre la imagen.</span><span class="sxs-lookup"><span data-stu-id="b2a59-110">WIA applications should always read image data headers for accurate image information.</span></span> <span data-ttu-id="b2a59-111">El controlador WIA puede modificar las propiedades de WIA y los encabezados de datos de imagen durante la transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="b2a59-111">The WIA driver can alter the WIA properties and image data headers during data transfer.</span></span>
>
> <span data-ttu-id="b2a59-112">Si no se proporciona ningún encabezado de datos de imagen con el formato especificado, la aplicación WIA debe usar las propiedades de WIA como origen de información sobre la transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="b2a59-112">If there is no image data header supplied with the specified format, the WIA application should use the WIA properties as an information source about the data transfer.</span></span> <span data-ttu-id="b2a59-113">La aplicación WIA debe volver a leer las propiedades de WIA necesarias después de que se complete el examen o la captura para obtener la configuración actualizada.</span><span class="sxs-lookup"><span data-stu-id="b2a59-113">The WIA application should reread the needed WIA properties after the scan or capture completes to get the updated settings.</span></span>

 

<span data-ttu-id="b2a59-114">En las secciones siguientes se describen las distintas propiedades de WIA:</span><span class="sxs-lookup"><span data-stu-id="b2a59-114">The following sections describe the various WIA properties:</span></span>

-   [<span data-ttu-id="b2a59-115">Validación de propiedades de WIA</span><span class="sxs-lookup"><span data-stu-id="b2a59-115">WIA Property Validation</span></span>](-wia-wia-property-validation.md)
-   [<span data-ttu-id="b2a59-116">Propiedades de información del dispositivo</span><span class="sxs-lookup"><span data-stu-id="b2a59-116">Device Information Properties</span></span>](-wia-device-information-properties-wia-dip-xxxx.md)
-   [<span data-ttu-id="b2a59-117">Propiedades de dispositivos</span><span class="sxs-lookup"><span data-stu-id="b2a59-117">Device Properties</span></span>](-wia-device-properties.md)
-   [<span data-ttu-id="b2a59-118">Propiedades del elemento</span><span class="sxs-lookup"><span data-stu-id="b2a59-118">Item Properties</span></span>](-wia-item-properties.md)
-   [<span data-ttu-id="b2a59-119">Propiedades de WIA adicionales</span><span class="sxs-lookup"><span data-stu-id="b2a59-119">Additional WIA Properties</span></span>](-wia-additional-wia-properties.md)
-   [<span data-ttu-id="b2a59-120">Definir propiedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="b2a59-120">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
-   [<span data-ttu-id="b2a59-121">Usar propiedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="b2a59-121">Using Custom Properties</span></span>](-wia-using-custom-properties.md)
-   [<span data-ttu-id="b2a59-122">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="b2a59-122">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)

 

 
