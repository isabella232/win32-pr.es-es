---
description: Entradas generales del registro
ms.assetid: 6a140c7f-df8c-4a8e-9e4d-dbb38901e14f
title: Entradas generales del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7c3514adcc0aeaaf9adadd2b71dfdffcd8d408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706623"
---
# <a name="general-registry-entries"></a><span data-ttu-id="5bac3-103">Entradas generales del registro</span><span class="sxs-lookup"><span data-stu-id="5bac3-103">General Registry Entries</span></span>


<span data-ttu-id="5bac3-104">Las siguientes entradas del registro deben realizarse por separado para el descodificador y el codificador:</span><span class="sxs-lookup"><span data-stu-id="5bac3-104">The following registry entries must be made separately for both the decoder and the encoder:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Encoder/Decoder CLSID}
         Author = Author's Name
         Description = Your Codec Description
         DeviceManufacturer = Manufacturer's Name
         DeviceModels = Device,Device
         FriendlyName = Codec Friendly Name
         Date = mm-dd-yyyy
         Vendor = {GUID_Vendor}
         ContainerFormat = {GUID_ContainerFormat}
         Version = Major.Minor.Build.Number
         SpecVersion = Major.Minor.Build.Number
         MimeTypes = Your Mime Type
         SupportAnimation = 0|1
         SupportChromakey = 0|1
         SupportLossless = 0|1
         SupportMultiframe = 0|1
         Formats
            {Supported PixelFormat GUID 1}
            {Supported PixelFormat GUID ...}
            {Supported PixelFormat GUID N}
         ArbitrationPriority  = 0-10
```

<span data-ttu-id="5bac3-105">Se requieren las entradas FriendlyName, VendorGUID, ContainerFormat, MimeTypes, FileExtensions y Formats.</span><span class="sxs-lookup"><span data-stu-id="5bac3-105">The FriendlyName, VendorGUID, ContainerFormat, MimeTypes, FileExtensions, and Formats entries are required.</span></span> <span data-ttu-id="5bac3-106">Todos los demás son opcionales.</span><span class="sxs-lookup"><span data-stu-id="5bac3-106">All of the others are optional.</span></span>

<span data-ttu-id="5bac3-107">Tenga en cuenta que las entradas DeviceManufacturer y DeviceModels son específicas de los códecs sin formato y hacen referencia al fabricante de la cámara y a los modelos de cámara a los que se aplica el códec.</span><span class="sxs-lookup"><span data-stu-id="5bac3-107">Note that the DeviceManufacturer and DeviceModels entries are specific to raw codecs and refer to the camera manufacturer and camera models that the codec is applicable to.</span></span> <span data-ttu-id="5bac3-108">La versión de la especificación es la versión de la especificación de formato de imagen con la que el códec es compatible.</span><span class="sxs-lookup"><span data-stu-id="5bac3-108">The spec version is the version of the image format specification with which the codec complies.</span></span> <span data-ttu-id="5bac3-109">La entrada Formats especifica los formatos de píxel admitidos por el códec.</span><span class="sxs-lookup"><span data-stu-id="5bac3-109">The Formats entry specifies the pixel formats supported by the codec.</span></span> <span data-ttu-id="5bac3-110">Un códec puede admitir más de un formato de píxel.</span><span class="sxs-lookup"><span data-stu-id="5bac3-110">A codec may support more than one pixel format.</span></span> <span data-ttu-id="5bac3-111">En ese caso, escribiría varias claves en \_ las clases HKEY \_ raíz \\ CLSID \\ {Encoder/descodificador CLSID} \\ formatos.</span><span class="sxs-lookup"><span data-stu-id="5bac3-111">In that case, you would enter multiple keys under HKEY\_CLASSES\_ROOT\\CLSID\\{Encoder/Decoder CLSID}\\Formats.</span></span>

## <a name="arbitrationpriority"></a><span data-ttu-id="5bac3-112">ArbitrationPriority</span><span class="sxs-lookup"><span data-stu-id="5bac3-112">ArbitrationPriority</span></span>

<span data-ttu-id="5bac3-113">A partir de Windows 8, ArbitrationPriority es una nueva entrada del registro.</span><span class="sxs-lookup"><span data-stu-id="5bac3-113">Starting in Windows 8, ArbitrationPriority is a new registry entry.</span></span> <span data-ttu-id="5bac3-114">Los valores válidos son de 0 a 10.</span><span class="sxs-lookup"><span data-stu-id="5bac3-114">Valid values are 0 through 10.</span></span> <span data-ttu-id="5bac3-115">Cuando la clave ArbitrationPriority está presente, el valor de esta clave indicará a WIC que dé prioridad al códec asociado detrás de cualquier otro códec con un valor de ArbitrationPriority inferior.</span><span class="sxs-lookup"><span data-stu-id="5bac3-115">When the ArbitrationPriority key is present, the value of this key will instruct WIC to prioritize the associated codec behind any other codecs with a lower ArbitrationPriority value.</span></span> <span data-ttu-id="5bac3-116">Esta evaluación se produce antes de que se produzca el arbitraje del códec de WIC existente, y garantiza que el códec asociado tiene prioridad por debajo de cualquier códec de la competencia, incluso si es igual o más capaz.</span><span class="sxs-lookup"><span data-stu-id="5bac3-116">This evaluation occurs before the existing WIC codec arbitration occurs, and ensures the associated codec is prioritized below any competing codec, even if it is as or more capable.</span></span> <span data-ttu-id="5bac3-117">Cualquier códec que no tenga un valor ArbitrationPriority explícito definido en el registro se establecerá de forma predeterminada en Priority 0.</span><span class="sxs-lookup"><span data-stu-id="5bac3-117">Any codec that doesn’t have an explicit ArbitrationPriority value defined in the registry will default to Priority 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5bac3-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5bac3-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5bac3-119">**Vista**</span><span class="sxs-lookup"><span data-stu-id="5bac3-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5bac3-120">Instalación y registro de CÓDECs</span><span class="sxs-lookup"><span data-stu-id="5bac3-120">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="5bac3-121">Entradas del registro específicas del codificador</span><span class="sxs-lookup"><span data-stu-id="5bac3-121">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)
</dt> <dt>

[<span data-ttu-id="5bac3-122">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="5bac3-122">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="5bac3-123">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="5bac3-123">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="5bac3-124">**Funcionamiento del componente de creación de imágenes de Windows: detección y arbitraje de códecs**</span><span class="sxs-lookup"><span data-stu-id="5bac3-124">**How the Windows Imaging Component Works: Codec Discovery and Arbitration**</span></span>](-wic-howwicworks.md)
</dt> </dl>

 

 



