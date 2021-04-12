---
title: Entrada del registro FormatCode
description: Entrada del registro FormatCode
ms.assetid: cc444eaa-6898-48ab-9573-9e7d5e25d6db
keywords:
- Windows Media Player, entradas del registro de FormatCode
- Windows Media Player, extensiones de nombre de archivo
- Media Player de Windows, registro
- registro, extensiones de nombre de archivo
- registro, entradas FormatCode
- registro, configuración para Windows Media Player
- configuración del registro de la extensión de nombre de archivo
- Entradas del registro de FormatCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2318d32e9d7a08a2ae23b24e7acd2674b9eecb2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104270751"
---
# <a name="formatcode-registry-entry"></a><span data-ttu-id="1f8dc-111">Entrada del registro FormatCode</span><span class="sxs-lookup"><span data-stu-id="1f8dc-111">FormatCode Registry Entry</span></span>

<span data-ttu-id="1f8dc-112">Cuando Windows Media Player encuentra una extensión de nombre de archivo personalizada, busca una subclave del registro que coincida con la extensión.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="1f8dc-113">La subclave se describe en [configuración del registro](file-name-extension-registry-settings.md)de la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="1f8dc-114">Una de las entradas del registro que pueden aparecer bajo la subclave de la extensión es la entrada **FormatCode** .</span><span class="sxs-lookup"><span data-stu-id="1f8dc-114">One of the registry entries that can appear under the extension's subkey is the **FormatCode** entry.</span></span>

<span data-ttu-id="1f8dc-115">La entrada del registro **FormatCode** especifica el código de formato del Protocolo de transporte multimedia (MTP) para los archivos que tienen la extensión personalizada.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-115">The **FormatCode** registry entry specifies the Media Transport Protocol (MTP) format code for files that have the custom extension.</span></span> <span data-ttu-id="1f8dc-116">La entrada del registro **FormatCode** tiene el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-116">The **FormatCode** registry entry has the following form.</span></span>



| <span data-ttu-id="1f8dc-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="1f8dc-117">Name</span></span>       | <span data-ttu-id="1f8dc-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="1f8dc-118">Type</span></span>           | <span data-ttu-id="1f8dc-119">Value</span><span class="sxs-lookup"><span data-stu-id="1f8dc-119">Value</span></span>                                                             |
|------------|----------------|-------------------------------------------------------------------|
| <span data-ttu-id="1f8dc-120">FormatCode</span><span class="sxs-lookup"><span data-stu-id="1f8dc-120">FormatCode</span></span> | <span data-ttu-id="1f8dc-121">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="1f8dc-121">**REG\_DWORD**</span></span> | <span data-ttu-id="1f8dc-122">Entero positivo de 16 bits que identifica el formato del archivo.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-122">A 16-bit positive integer that identifies the format of the file.</span></span> |



 

<span data-ttu-id="1f8dc-123">Cuando el usuario intenta copiar un archivo multimedia digital que tiene una extensión de nombre de archivo personalizada en un dispositivo portátil, Windows Media Player busca en el registro para encontrar un código de formato asociado a la extensión de nombre de archivo personalizada.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-123">When the user attempts to copy a digital media file that has a custom file name extension to a portable device, Windows Media Player looks in the registry to find a format code associated with the custom file name extension.</span></span> <span data-ttu-id="1f8dc-124">Si Windows Media Player encuentra un código de formato, utiliza MTP para determinar si el dispositivo admite el formato de archivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-124">If Windows Media Player finds a format code, it uses MTP to determine whether the device supports the custom file format.</span></span> <span data-ttu-id="1f8dc-125">Si el dispositivo admite el formato, el archivo multimedia se copia en el dispositivo sin ser transcodificado.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-125">If the device supports the format, the media file is copied to the device without being transcoded.</span></span>

<span data-ttu-id="1f8dc-126">Un dispositivo que admite MTP puede proporcionar Windows Media Player con un conjunto de DeviceInfo, que contiene, entre otras cosas, una lista de códigos de formato admitidos por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-126">A device that supports MTP can supply Windows Media Player with a DeviceInfo dataset, which contains, among other things, a list of format codes supported by the device.</span></span>

<span data-ttu-id="1f8dc-127">Si está en el proceso de desarrollar un formato de archivo personalizado, puede solicitar un código de formato de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1f8dc-127">If you are in the process of developing a custom file format, you can request a format code from Microsoft.</span></span> <span data-ttu-id="1f8dc-128">Para obtener información acerca de cómo solicitar un código de formato, vea el kit de migración de protocolo de transporte de multimedia de Microsoft, que está disponible en el [Centro para desarrolladores de Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="1f8dc-128">For information about how to request a format code, see the Microsoft Media Transport Protocol Porting Kit, which is available at the [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f8dc-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f8dc-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f8dc-130">**Configuración del registro de la extensión de nombre de archivo**</span><span class="sxs-lookup"><span data-stu-id="1f8dc-130">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




