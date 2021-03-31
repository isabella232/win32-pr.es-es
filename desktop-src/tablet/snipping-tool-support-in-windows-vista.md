---
description: En este tema se describe cómo la aplicación puede especificar qué dirección URL debe obtener la herramienta de recortes de Tablet PC al capturar la aplicación.
ms.assetid: e31e63e8-8f6b-41f7-8bd6-afc5ca32456b
title: Compatibilidad con recortes en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046dd6c8a97d1dacc20065dc1f741610fec13865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911713"
---
# <a name="snipping-tool-support-in-windows-vista"></a><span data-ttu-id="7139a-103">Compatibilidad con recortes en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7139a-103">Snipping Tool Support in Windows Vista</span></span>

<span data-ttu-id="7139a-104">En este tema se describe cómo la aplicación puede especificar qué dirección URL debe obtener la herramienta de recortes de Tablet PC al capturar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7139a-104">This topic describes how your application can specify what URL the Tablet PC Snipping Tool should obtain when capturing your application.</span></span>

## <a name="specifying-the-url-via-registry-key"></a><span data-ttu-id="7139a-105">Especificación de la dirección URL mediante la clave del registro</span><span class="sxs-lookup"><span data-stu-id="7139a-105">Specifying the URL via Registry Key</span></span>

<span data-ttu-id="7139a-106">Recortes permite a los usuarios capturar un recorte (captura de pantalla) de cualquier objeto en la pantalla y, a continuación, anotar, guardar o compartir la imagen.</span><span class="sxs-lookup"><span data-stu-id="7139a-106">Snipping Tool allows users to capture a snip (screen shot) of any object on the screen and then annotate, save, or share the image.</span></span> <span data-ttu-id="7139a-107">Cuando los datos se guardan en formato HTML o cuando se envían a un cliente de correo electrónico que admite HTML en línea, la herramienta recortes puede Agregar una dirección URL al recorte si la aplicación proporciona información sobre cómo obtener la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="7139a-107">When the data is saved in HTML format, or when it is sent to an email client that supports inline HTML, Snipping Tool can add a URL to the snip if the application provides information on how to obtain the URL.</span></span>

<span data-ttu-id="7139a-108">Recortes obtiene la dirección URL a través de objetos de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="7139a-108">Snipping Tool obtains the URL via accessibility objects.</span></span> <span data-ttu-id="7139a-109">Las aplicaciones deben especificar la información necesaria en las siguientes claves del registro:</span><span class="sxs-lookup"><span data-stu-id="7139a-109">Applications should specify the necessary information under the following registry keys:</span></span>

<span data-ttu-id="7139a-110">HKLM \\ software \\ Microsoft \\ Windows \\ TabletPC \\ recortes Tool \\ LinkFingerprints,</span><span class="sxs-lookup"><span data-stu-id="7139a-110">HKLM\\Software\\Microsoft\\Windows\\TabletPC\\Snipping Tool\\LinkFingerprints,</span></span>

<span data-ttu-id="7139a-111">Y deben crear una subclave cuyo nombre sea el mismo que el de la clase de ventana de la que se debe obtener el vínculo.</span><span class="sxs-lookup"><span data-stu-id="7139a-111">And should create a subkey whose name is the same as the window class from which the link should be obtained.</span></span> <span data-ttu-id="7139a-112">El nombre de la clase de ventana debe ser la ventana superior de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7139a-112">The window class name should be the topmost window of the application.</span></span>

<span data-ttu-id="7139a-113">HKLM \\ software \\ Microsoft \\ Windows \\ TabletPC \\ recortes Tool \\ LinkFingerprints\\<Window Class Name></span><span class="sxs-lookup"><span data-stu-id="7139a-113">HKLM\\Software\\Microsoft\\Windows\\TabletPC\\Snipping Tool\\LinkFingerprints\\<Window Class Name></span></span>

### <a name="window-class-key-details"></a><span data-ttu-id="7139a-114">Detalles de la clave de clase de ventana</span><span class="sxs-lookup"><span data-stu-id="7139a-114">Window Class Key Details</span></span>

<span data-ttu-id="7139a-115">En la clave de clase de ventana, se deben establecer los valores adecuados para indicar que la herramienta recortes debe detectar el objeto de accesibilidad correcto.</span><span class="sxs-lookup"><span data-stu-id="7139a-115">Under the window class key, the appropriate values should be set in order to indicate Snipping Tool should detect the correct accessibility object.</span></span>



| <span data-ttu-id="7139a-116">VALOR</span><span class="sxs-lookup"><span data-stu-id="7139a-116">VALUE</span></span>                        | <span data-ttu-id="7139a-117">TYPE</span><span class="sxs-lookup"><span data-stu-id="7139a-117">TYPE</span></span>                  | <span data-ttu-id="7139a-118">MÁSCARA</span><span class="sxs-lookup"><span data-stu-id="7139a-118">MASK</span></span>            | <span data-ttu-id="7139a-119">INFORMACIÓN ALMACENADA</span><span class="sxs-lookup"><span data-stu-id="7139a-119">INFORMATION STORED</span></span>                                          |
|------------------------------|-----------------------|-----------------|-------------------------------------------------------------|
| <span data-ttu-id="7139a-120">Máscara</span><span class="sxs-lookup"><span data-stu-id="7139a-120">Mask</span></span><br/>              | <span data-ttu-id="7139a-121">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="7139a-121">REG\_DWORD</span></span><br/> |                 | <span data-ttu-id="7139a-122">Indica cuál de los siguientes campos se va a comprobar</span><span class="sxs-lookup"><span data-stu-id="7139a-122">Indicates which of the following fields to check</span></span><br/> |
| <span data-ttu-id="7139a-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="7139a-123">Name</span></span><br/>              | <span data-ttu-id="7139a-124">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="7139a-124">REG\_SZ</span></span><br/>    | <span data-ttu-id="7139a-125">0x02</span><span class="sxs-lookup"><span data-stu-id="7139a-125">0x02</span></span><br/> | <span data-ttu-id="7139a-126">Nombre de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="7139a-126">Accessibility name</span></span><br/>                               |
| <span data-ttu-id="7139a-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="7139a-127">Description</span></span><br/>       | <span data-ttu-id="7139a-128">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="7139a-128">REG\_SZ</span></span><br/>    | <span data-ttu-id="7139a-129">0x04</span><span class="sxs-lookup"><span data-stu-id="7139a-129">0x04</span></span><br/> | <span data-ttu-id="7139a-130">Descripción de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="7139a-130">Accessibility description</span></span><br/>                        |
| <span data-ttu-id="7139a-131">Role</span><span class="sxs-lookup"><span data-stu-id="7139a-131">Role</span></span><br/>              | <span data-ttu-id="7139a-132">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="7139a-132">REG\_DWORD</span></span><br/> | <span data-ttu-id="7139a-133">0x08</span><span class="sxs-lookup"><span data-stu-id="7139a-133">0x08</span></span><br/> | <span data-ttu-id="7139a-134">Rol de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="7139a-134">Accessibility role</span></span><br/>                               |
| <span data-ttu-id="7139a-135">ParentName</span><span class="sxs-lookup"><span data-stu-id="7139a-135">ParentName</span></span><br/>        | <span data-ttu-id="7139a-136">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="7139a-136">REG\_SZ</span></span><br/>    | <span data-ttu-id="7139a-137">0x10</span><span class="sxs-lookup"><span data-stu-id="7139a-137">0x10</span></span><br/> | <span data-ttu-id="7139a-138">Nombre de accesibilidad del elemento primario</span><span class="sxs-lookup"><span data-stu-id="7139a-138">Accessibility name of parent</span></span><br/>                     |
| <span data-ttu-id="7139a-139">ParentValue</span><span class="sxs-lookup"><span data-stu-id="7139a-139">ParentValue</span></span><br/>       | <span data-ttu-id="7139a-140">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="7139a-140">REG\_SZ</span></span><br/>    | <span data-ttu-id="7139a-141">0x20</span><span class="sxs-lookup"><span data-stu-id="7139a-141">0x20</span></span><br/> | <span data-ttu-id="7139a-142">Valor de accesibilidad de primario</span><span class="sxs-lookup"><span data-stu-id="7139a-142">Accessibility value of parent</span></span><br/>                    |
| <span data-ttu-id="7139a-143">ParentRole</span><span class="sxs-lookup"><span data-stu-id="7139a-143">ParentRole</span></span><br/>        | <span data-ttu-id="7139a-144">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="7139a-144">REG\_DWORD</span></span><br/> | <span data-ttu-id="7139a-145">0x40</span><span class="sxs-lookup"><span data-stu-id="7139a-145">0x40</span></span><br/> | <span data-ttu-id="7139a-146">Rol de accesibilidad del elemento primario</span><span class="sxs-lookup"><span data-stu-id="7139a-146">Accessibility role of parent</span></span><br/>                     |
| <span data-ttu-id="7139a-147">ParentDescription</span><span class="sxs-lookup"><span data-stu-id="7139a-147">ParentDescription</span></span><br/> | <span data-ttu-id="7139a-148">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="7139a-148">REG\_SZ</span></span><br/>    | <span data-ttu-id="7139a-149">0x80</span><span class="sxs-lookup"><span data-stu-id="7139a-149">0x80</span></span><br/> | <span data-ttu-id="7139a-150">Descripción de accesibilidad de la principal</span><span class="sxs-lookup"><span data-stu-id="7139a-150">Accessibility description of parent</span></span><br/>              |



 

<span data-ttu-id="7139a-151">Además, si se establece el valor de bit de máscara 0x1, la dirección URL debe tomarse del nombre de accesibilidad; de lo contrario, la dirección URL debe tomarse del valor de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="7139a-151">Additionally, if the mask bit value 0x1 is set, then the URL should be taken from the accessibility name; otherwise, the URL should be taken from the accessibility value.</span></span>

<span data-ttu-id="7139a-152">Si la aplicación utiliza cadenas localizadas para los valores de REG \_ SZ anteriores, se debe proporcionar la cadena como una cadena indirecta con el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="7139a-152">If the application uses localized strings for the REG\_SZ values above, the string should be provided as an indirect string by using the following format:</span></span>

<span data-ttu-id="7139a-153">@filename, recurso</span><span class="sxs-lookup"><span data-stu-id="7139a-153">@filename,resource</span></span>

<span data-ttu-id="7139a-154">La cadena se extrae del archivo denominado, utilizando el valor de recurso como localizador.</span><span class="sxs-lookup"><span data-stu-id="7139a-154">The string is extracted from the file named, using the resource value as a locator.</span></span> <span data-ttu-id="7139a-155">Si el valor del recurso es cero o mayor, el número se convierte en el índice de la cadena en el archivo binario.</span><span class="sxs-lookup"><span data-stu-id="7139a-155">If the resource value is zero or greater, the number becomes the index of the string in the binary file.</span></span> <span data-ttu-id="7139a-156">Si el número es negativo, se convierte en un identificador de recursos (ID.).</span><span class="sxs-lookup"><span data-stu-id="7139a-156">If the number is negative, it becomes a resource identifier (ID).</span></span>

> [!Note]  
> <span data-ttu-id="7139a-157">Las constantes de rol se pueden encontrar en oleacc. h en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7139a-157">Role constants can be found in oleacc.h in the Windows SDK.</span></span> <span data-ttu-id="7139a-158">Los valores del registro descritos son específicos de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7139a-158">The registry values described are specific to Windows Vista.</span></span>

 

 

 




