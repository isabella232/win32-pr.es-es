---
title: Para el uso de perfiles con Writer
description: Para el uso de perfiles con Writer
ms.assetid: 8805bc57-5f19-4544-bcb8-5af880ba8ea0
keywords:
- SDK de Windows Media Format, escribir archivos ASF
- SDK de Windows Media Format, crear archivos ASF
- Windows Media Format SDK, Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), escribir archivos
- ASF (formato de sistemas avanzados), escribir archivos
- Advanced Systems Format (ASF), crear archivos
- ASF (formato de sistemas avanzados), crear archivos
- perfiles, crear archivos ASF
- perfiles, escribir archivos ASF
- perfiles, creación de archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d027e6ea0e669d2a5206901faefab1f5a9583153
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104077437"
---
# <a name="to-use-profiles-with-the-writer"></a><span data-ttu-id="ee4ba-113">Para el uso de perfiles con Writer</span><span class="sxs-lookup"><span data-stu-id="ee4ba-113">To Use Profiles with the Writer</span></span>

<span data-ttu-id="ee4ba-114">El escritor usa datos de perfil para crear archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="ee4ba-114">The writer uses profile data to create ASF files.</span></span> <span data-ttu-id="ee4ba-115">Debe especificar un perfil para usarlo antes de hacer nada más con el escritor.</span><span class="sxs-lookup"><span data-stu-id="ee4ba-115">You must specify a profile for use before doing anything else with the writer.</span></span>

<span data-ttu-id="ee4ba-116">Puede establecer un perfil del sistema para usarlo con el escritor pasando el ID. de perfil al método [**IWMWriter:: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) .</span><span class="sxs-lookup"><span data-stu-id="ee4ba-116">You can set a system profile for use with the writer by passing the profile ID to the [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) method.</span></span>

<span data-ttu-id="ee4ba-117">Para especificar un perfil personalizado para usarlo con el escritor, debe obtener una interfaz [**IWMProfile**](iwmprofile.md) para un objeto que contenga los datos de perfil deseados.</span><span class="sxs-lookup"><span data-stu-id="ee4ba-117">To specify a custom profile for use with the writer, you must obtain an [**IWMProfile**](iwmprofile.md) interface to an object containing the desired profile data.</span></span> <span data-ttu-id="ee4ba-118">Puede usar uno de los métodos de carga de la interfaz [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) para lograr esto.</span><span class="sxs-lookup"><span data-stu-id="ee4ba-118">You can use one of the loading methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface to accomplish this.</span></span> <span data-ttu-id="ee4ba-119">Una vez que tenga una interfaz **IWMProfile** válida, puede pasarle un puntero al método [**IWMWriter:: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) .</span><span class="sxs-lookup"><span data-stu-id="ee4ba-119">After you have a valid **IWMProfile** interface, you can pass a pointer to it to the [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) method.</span></span> <span data-ttu-id="ee4ba-120">Para obtener más información acerca de la configuración del perfil, consulte [trabajar con perfiles](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="ee4ba-120">For more information about profile settings, see [Working with Profiles](working-with-profiles.md).</span></span>

<span data-ttu-id="ee4ba-121">Si realiza cambios en el objeto de perfil mediante la interfaz **IWMProfile** después de configurar el perfil en el escritor, debe llamar de nuevo a **SetProfile** o, de lo contrario, los cambios no se reflejarán en el escritor.</span><span class="sxs-lookup"><span data-stu-id="ee4ba-121">If you make changes to the profile object by using the **IWMProfile** interface after setting the profile in the writer, you must call **SetProfile** again, or else the changes will not be reflected in the writer.</span></span> <span data-ttu-id="ee4ba-122">Sin embargo, al llamar a **SetProfile** se restablecerán todos los atributos de encabezado, por lo que debe asegurarse de establecer los atributos de encabezado necesarios después de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="ee4ba-122">However, calling **SetProfile** will reset all header attributes, so be sure to set any required header attributes after calling this method.</span></span>

<span data-ttu-id="ee4ba-123">La siguiente función de ejemplo establece el perfil en "Windows Media Video 8 para módems de acceso telefónico (56 kbps)":</span><span class="sxs-lookup"><span data-stu-id="ee4ba-123">The following example function sets the profile to "Windows Media Video 8 for Dial-up Modems (56 Kbps)":</span></span>


```C++
#include <wmsysprf.h>

HRESULT SetProfileExample()
{
  HRESULT hr;
  IWMWriter *pWriter = NULL;
  hr = WMCreateWriter(NULL, &pWriter);
  if (FAILED(hr)) return hr;
  hr = pWriter->SetProfileByID(WMProfile_V80_56Video);
  return hr;
}

```



> [!Note]  
> <span data-ttu-id="ee4ba-124">No hay ningún perfil de sistema predefinido que use los códecs de la serie Windows Media Audio y vídeo 9.</span><span class="sxs-lookup"><span data-stu-id="ee4ba-124">There are no predefined system profiles that use the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="ee4ba-125">Para obtener más información, vea [reutilizar las configuraciones de Stream](reusing-stream-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="ee4ba-125">For more information, see [Reusing Stream Configurations](reusing-stream-configurations.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ee4ba-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ee4ba-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee4ba-127">**IWMWriter::SetProfileByID**</span><span class="sxs-lookup"><span data-stu-id="ee4ba-127">**IWMWriter::SetProfileByID**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)
</dt> <dt>

[<span data-ttu-id="ee4ba-128">**Trabajar con perfiles**</span><span class="sxs-lookup"><span data-stu-id="ee4ba-128">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> <dt>

[<span data-ttu-id="ee4ba-129">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="ee4ba-129">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




