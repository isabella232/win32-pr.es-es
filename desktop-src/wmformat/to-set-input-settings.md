---
title: Para establecer la configuración de entrada
description: Para establecer la configuración de entrada
ms.assetid: 288801a7-793f-43bd-9c5a-f9e1bd86ecc3
keywords:
- Advanced Systems Format (ASF), configuración de entrada
- ASF (formato de sistemas avanzados), configuración de entrada
- perfiles, configuración de entrada
- códecs, configuración de entrada
- flujos, configuración de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e7b2db64a7346cc8b9d46c48f0add79dafcac95
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994957"
---
# <a name="to-set-input-settings"></a><span data-ttu-id="4803e-108">Para establecer la configuración de entrada</span><span class="sxs-lookup"><span data-stu-id="4803e-108">To Set Input Settings</span></span>

<span data-ttu-id="4803e-109">La estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) define las propiedades básicas de los medios de entrada y de secuencia.</span><span class="sxs-lookup"><span data-stu-id="4803e-109">The basic properties of input media and stream media are defined by the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="4803e-110">En el caso de los formatos de entrada, la aplicación establece la información de tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="4803e-110">For input formats, the media type information is set by your application.</span></span> <span data-ttu-id="4803e-111">En el caso de los formatos de secuencia, la información de tipo de medio se establece en el perfil que se asigna al escritor.</span><span class="sxs-lookup"><span data-stu-id="4803e-111">For stream formats, the media type information is set in the profile you assign to the writer.</span></span> <span data-ttu-id="4803e-112">Algunas propiedades son independientes del tipo de medio y se deben establecer para una entrada antes de comenzar la escritura.</span><span class="sxs-lookup"><span data-stu-id="4803e-112">Some properties are independent of media type and must be set for an input before writing begins.</span></span> <span data-ttu-id="4803e-113">Estas propiedades son características de códec y escritor que son independientes del tipo de secuencia y deben establecerse después de que el perfil se haya asignado en el escritor, pero antes de que empiece la escritura.</span><span class="sxs-lookup"><span data-stu-id="4803e-113">These properties are codec and writer features that are independent of stream type, and must be set after the profile is assigned in the writer but before writing begins.</span></span>

<span data-ttu-id="4803e-114">Establecer una configuración de entrada requiere una llamada a [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span><span class="sxs-lookup"><span data-stu-id="4803e-114">Setting an input setting requires a call to [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span></span> <span data-ttu-id="4803e-115">También puede comprobar el valor actual de una configuración con una llamada a [**IWMWriterAdvanced2:: GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).</span><span class="sxs-lookup"><span data-stu-id="4803e-115">You can also check the current value of a setting with a call to [**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4803e-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4803e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4803e-117">**Para el uso de perfiles con Writer**</span><span class="sxs-lookup"><span data-stu-id="4803e-117">**To Use Profiles with the Writer**</span></span>](to-use-profiles-with-the-writer.md)
</dt> <dt>

[<span data-ttu-id="4803e-118">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="4803e-118">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> <dt>

[<span data-ttu-id="4803e-119">**Escribir secuencias de imagen**</span><span class="sxs-lookup"><span data-stu-id="4803e-119">**Writing Image Streams**</span></span>](writing-image-streams.md)
</dt> </dl>

 

 




