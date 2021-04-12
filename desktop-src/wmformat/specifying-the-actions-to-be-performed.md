---
title: Especificar las acciones que se van a realizar
description: Especificar las acciones que se van a realizar
ms.assetid: b6b094b1-276d-4f90-adc7-0f3507fdfe27
keywords:
- Advanced Systems Format (ASF), especificar acciones
- ASF (formato de sistemas avanzados), especificación de acciones
- Administración de derechos digitales (DRM), especificación de acciones
- DRM (administración de derechos digitales), especificación de acciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2bd39a04d9ac87c4492749ca5e250d587c0e25
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420297"
---
# <a name="specifying-the-actions-to-be-performed"></a><span data-ttu-id="9f799-107">Especificar las acciones que se van a realizar</span><span class="sxs-lookup"><span data-stu-id="9f799-107">Specifying the Actions To Be Performed</span></span>

<span data-ttu-id="9f799-108">La primera vez que se llama a [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) para crear el objeto de lector, el segundo parámetro es **una operación OR bit a bit** de los valores de los [**\_ derechos de WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) .</span><span class="sxs-lookup"><span data-stu-id="9f799-108">When you first call [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) to create the reader object, the second parameter is a bitwise **OR** of [**WMT\_RIGHTS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) values.</span></span> <span data-ttu-id="9f799-109">Use este parámetro para especificar las acciones que realizará la aplicación en el primer archivo que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="9f799-109">Use this parameter to specify which action(s) the application will take on the first file to be opened.</span></span> <span data-ttu-id="9f799-110">Estas acciones se corresponden directamente con los derechos que se pueden especificar en la licencia.</span><span class="sxs-lookup"><span data-stu-id="9f799-110">These actions correspond directly to rights that can be specified in the license.</span></span> <span data-ttu-id="9f799-111">En las llamadas subsiguientes a [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), puede modificar los derechos que está solicitando llamando a [**IWMDRMReader:: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), especificando la constante definida para la propiedad [**\_ derechos DRM**](drm-rights.md) y usando literales de cadena (de tipo **WCHAR**) separados por punto y coma para identificar los derechos.</span><span class="sxs-lookup"><span data-stu-id="9f799-111">On subsequent calls to [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), you can modify the rights that you are requesting by calling [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), specifying the defined constant for the [**DRM\_Rights**](drm-rights.md) property, and using string literals (of type **WCHAR**) separated by semicolons to identify the rights.</span></span> <span data-ttu-id="9f799-112">El fragmento de código siguiente solicita cuatro derechos: reproducir el archivo, copiarlo en un dispositivo y reproducirlo como parte de una lista de reproducción colaborativa.</span><span class="sxs-lookup"><span data-stu-id="9f799-112">The following code snippet requests four rights: play the file, copy it to a device, and play it as part of a collaborative playlist.</span></span>


```C++
WCHAR wszRights[] = L"Play;Copy;CollaborativePlay";
p_WMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
                              (BYTE*)wszRights, sizeof(wszRights));
```



> [!Note]  
> <span data-ttu-id="9f799-113">No confunda la propiedad [**\_ derechos DRM**](drm-rights.md) con la propiedad [**\_ marcas DRM**](drm-flags.md) , que es un **valor DWORD** que se usa para especificar los derechos que se aplicarán a una licencia local de DRM versión 1 al copiar contenido desde un CD.</span><span class="sxs-lookup"><span data-stu-id="9f799-113">Do not confuse the [**DRM\_Rights**](drm-rights.md) property with the [**DRM\_Flags**](drm-flags.md) property, which is a **DWORD** used to specify which rights to apply to a local DRM version 1 license when copying content from a CD.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9f799-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9f799-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f799-115">**Leer archivos protegidos**</span><span class="sxs-lookup"><span data-stu-id="9f799-115">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




