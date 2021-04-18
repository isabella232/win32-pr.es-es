---
title: Protección de archivos con DRM versión 1
description: Protección de archivos con DRM versión 1
ms.assetid: 91de1c20-e926-4ff6-b0cd-e90fc9cbaad2
keywords:
- SDK de Windows Media Format, crear archivos protegidos
- SDK de Windows Media Format, archivos protegidos
- Advanced Systems Format (ASF), crear archivos protegidos
- ASF (formato de sistemas avanzados), crear archivos protegidos
- Advanced Systems Format (ASF), archivos protegidos
- ASF (formato de sistemas avanzados), archivos protegidos
- Advanced Systems Format (ASF), WMStubDRM. lib
- ASF (formato de sistemas avanzados), WMStubDRM. lib
- WMStubDRM. lib, crear archivos protegidos
- WMStubDRM. lib, archivos protegidos
- Administración de derechos digitales (DRM), WMStubDRM. lib
- DRM (administración de derechos digitales), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3e4d1ae9c0d3835c20f75b4e61c262a85a26f4
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104358767"
---
# <a name="protecting-files-with-drm-version-1"></a><span data-ttu-id="a8d8e-115">Protección de archivos con DRM versión 1</span><span class="sxs-lookup"><span data-stu-id="a8d8e-115">Protecting Files with DRM Version 1</span></span>

<span data-ttu-id="a8d8e-116">Cuando se aplica este tipo de protección, se genera una licencia de DRM versión 1 que solo es válida en el equipo desde el que se realizó la solicitud de licencia.</span><span class="sxs-lookup"><span data-stu-id="a8d8e-116">When this kind of protection is applied, a DRM version 1 license is generated that is valid only on the machine from which the license request was made.</span></span> <span data-ttu-id="a8d8e-117">Dado que no se establece ninguna inicialización de clave o clave, no hay ninguna manera de generar licencias portátiles para el contenido protegido con esta técnica.</span><span class="sxs-lookup"><span data-stu-id="a8d8e-117">Because no key or key seed is set, there is no way to generate portable licenses for content protected using this technique.</span></span> <span data-ttu-id="a8d8e-118">Sin embargo, al usar el SDK de Windows Media Format 7,1 o posterior, las licencias se pueden recuperar en el servicio de migración de licencias de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a8d8e-118">However, when using the Windows Media Format SDK 7.1 or later, the licenses are recoverable at the Microsoft License Migration service.</span></span>

<span data-ttu-id="a8d8e-119">Para proteger los archivos ASF con DRM versión 1, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a8d8e-119">To protect ASF files using DRM version 1, perform the following steps:</span></span>

1.  <span data-ttu-id="a8d8e-120">Vincule el archivo WMStubDRM. lib al proyecto y, si es necesario, desvincule wmvcore. lib.</span><span class="sxs-lookup"><span data-stu-id="a8d8e-120">Link the WMStubDRM.lib file to your project and, if necessary, unlink wmvcore.lib.</span></span>
2.  <span data-ttu-id="a8d8e-121">Llame a la función [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) para crear el escritor.</span><span class="sxs-lookup"><span data-stu-id="a8d8e-121">Call the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function to create the writer.</span></span> <span data-ttu-id="a8d8e-122">El primer argumento está reservado y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="a8d8e-122">The first argument is reserved and must be set to **NULL**.</span></span>
3.  <span data-ttu-id="a8d8e-123">Establezca un perfil para que lo use el escritor llamando a [**IWMWriter:: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) o [**IWMWriter:: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid).</span><span class="sxs-lookup"><span data-stu-id="a8d8e-123">Set a profile for the writer to use by calling [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) or [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid).</span></span> <span data-ttu-id="a8d8e-124">Debe establecer un perfil en el escritor antes de establecer cualquier atributo DRM.</span><span class="sxs-lookup"><span data-stu-id="a8d8e-124">You must set a profile in the writer before setting any DRM attributes.</span></span> <span data-ttu-id="a8d8e-125">DRM solo es compatible con los perfiles que usan los códecs Windows Media Audio o Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="a8d8e-125">DRM is supported only for profiles that use the Windows Media Audio or Windows Media Video codecs.</span></span>
4.  <span data-ttu-id="a8d8e-126">Con el método [**IWMHeaderInfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) , establezca las siguientes propiedades de DRM.</span><span class="sxs-lookup"><span data-stu-id="a8d8e-126">Using the [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) method, set the following DRM properties.</span></span> <span data-ttu-id="a8d8e-127">La propiedad **usar \_ DRM** indica a los componentes de DRM que protejan el contenido mediante DRM versión 1.</span><span class="sxs-lookup"><span data-stu-id="a8d8e-127">The **Use\_DRM** property instructs the DRM components to protect the content using DRM version 1.</span></span> <span data-ttu-id="a8d8e-128">La **propiedad \_ marcas DRM** especifica los derechos que se van a incluir en la licencia local que se creará para el contenido.</span><span class="sxs-lookup"><span data-stu-id="a8d8e-128">The **DRM\_Flags** property specifies the rights to be included in the local license that will be created for the content.</span></span> <span data-ttu-id="a8d8e-129">El valor de **\_ nivel DRM** también se almacena en la licencia; especifica el nivel mínimo necesario para tener acceso al contenido.</span><span class="sxs-lookup"><span data-stu-id="a8d8e-129">The **DRM\_LEVEL** value is also stored in the license; it specifies the minimum level required to access the content.</span></span> <span data-ttu-id="a8d8e-130">150 es el nivel recomendado para el contenido de la versión 1 de DRM.</span><span class="sxs-lookup"><span data-stu-id="a8d8e-130">150 is the recommended level for DRM version 1 content.</span></span>

    | <span data-ttu-id="a8d8e-131">Atributo</span><span class="sxs-lookup"><span data-stu-id="a8d8e-131">Attribute</span></span>      | <span data-ttu-id="a8d8e-132">Value</span><span class="sxs-lookup"><span data-stu-id="a8d8e-132">Value</span></span>                                                                                       |
    |----------------|---------------------------------------------------------------------------------------------|
    | <span data-ttu-id="a8d8e-133">**Usar \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="a8d8e-133">**Use\_DRM**</span></span>   | <span data-ttu-id="a8d8e-134">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a8d8e-134">**TRUE**</span></span>                                                                                    |
    | <span data-ttu-id="a8d8e-135">**\_Marcas DRM**</span><span class="sxs-lookup"><span data-stu-id="a8d8e-135">**DRM\_Flags**</span></span> | <span data-ttu-id="a8d8e-136">la \_ reproducción de la \_ \| \_ \_ \_ \_ \_ \_ \| \_ \_ \_ \_ caja derecha de WMT y la copia correcta en el dispositivo no de SDMI.</span><span class="sxs-lookup"><span data-stu-id="a8d8e-136">WMT\_RIGHT\_PLAYBACK \| WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE \| WMT\_RIGHT\_COPY\_TO\_CD</span></span> |
    | <span data-ttu-id="a8d8e-137">**nivel de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="a8d8e-137">**DRM\_LEVEL**</span></span> | <span data-ttu-id="a8d8e-138">150</span><span class="sxs-lookup"><span data-stu-id="a8d8e-138">150</span></span>                                                                                         |

    

     

<span data-ttu-id="a8d8e-139">En el ejemplo de código siguiente se muestra cómo crear un escritor habilitado para DRM para DRM versión 1 y cómo establecer las propiedades de DRM.</span><span class="sxs-lookup"><span data-stu-id="a8d8e-139">The following example code shows how to create a DRM-enabled writer for DRM version 1 and set the DRM properties.</span></span> <span data-ttu-id="a8d8e-140">La comprobación de errores se ha omitido por motivos de claridad.</span><span class="sxs-lookup"><span data-stu-id="a8d8e-140">Error checking has been omitted for the sake of clarify.</span></span>


```C++
BOOL  fUseDRM    = TRUE;
// These are the rights we will apply to the file. See WMT_RIGHTS for
// the full set of possible rights.

DWORD dwDRMFlags = WMT_RIGHT_PLAYBACK | 
                   WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE | 
                   WMT_RIGHT_COPY_TO_CD;

// Set the minimum required DRM level low enough
// to allow older players to access the content.
DWORD dwDRMLevel = 150;

IWMDRMWriter*  pWMDRMWriter  = NULL;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer object.
hr = WMCreateWriter( NULL, &pWMDRMWriter);

// Obtain the IWMHeaderInfo interface.
hr = pWMDRMWriter -> QueryInterface(IID_IWMHeaderInfo, 
                                   (void**) &pWMHeaderInfo);

// Tell the SDK runtime to protect the file using DRM version 1.
hr= pWMHeaderInfo-> SetAttribute(0,
                                 g_wszWMUse_DRM,
                                 WMT_TYPE_BOOL,
                                 (BYTE*)&fUseDRM,
                                 sizeof(BOOL));

// Specify the rights that will be stored in the local license that is
// created automatically for the content.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Flags, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMFlags,
                                 sizeof(DWORD) );

// Set the DRM_Level attribute in the file's DRM header.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Level, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMLevel,
                                 sizeof(DWORD) );
```



 

 




