---
title: Uso compartido de ancho de banda
description: Uso compartido de ancho de banda
ms.assetid: d33f3454-d20a-4b4d-9902-dabc5b806ad6
keywords:
- SDK de Windows Media Format, uso compartido de ancho de banda
- Advanced Systems Format (ASF), uso compartido de ancho de banda
- ASF (formato de sistemas avanzados), uso compartido de ancho de banda
- Windows Media Format SDK, secuencias
- Advanced Systems Format (ASF), streams
- ASF (formato de sistemas avanzados), secuencias
- uso compartido de ancho de banda, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2221d2fbc44654af7f12acf6e45fb85ca32b7d2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077336"
---
# <a name="bandwidth-sharing"></a><span data-ttu-id="8dc4d-110">Uso compartido de ancho de banda</span><span class="sxs-lookup"><span data-stu-id="8dc4d-110">Bandwidth Sharing</span></span>

<span data-ttu-id="8dc4d-111">Puede especificar flujos en un archivo que, cuando se tomen juntos, utilicen menos ancho de banda que la suma de las velocidades de bits indicadas.</span><span class="sxs-lookup"><span data-stu-id="8dc4d-111">You can specify streams in a file that, when taken together, use less bandwidth than the sum of their stated bit rates combined.</span></span> <span data-ttu-id="8dc4d-112">Al especificar el uso compartido del ancho de banda en el perfil, se aclara a la lectura de las aplicaciones que el ancho de banda disponible necesario para transmitir por secuencias el archivo no es lo que podría parecer.</span><span class="sxs-lookup"><span data-stu-id="8dc4d-112">By specifying bandwidth sharing in the profile, you clarify to reading applications that the available bandwidth needed to stream the file is not what it might otherwise seem.</span></span>

<span data-ttu-id="8dc4d-113">Ninguno de los objetos del SDK de Windows Media Format cambia su comportamiento en respuesta a la información de uso compartido del ancho de banda, que se proporciona únicamente para que la lectura de las aplicaciones pueda tener en cuenta a la hora de determinar si un archivo se puede reproducir con la entrega de ancho de banda restringida.</span><span class="sxs-lookup"><span data-stu-id="8dc4d-113">None of the objects of the Windows Media Format SDK change their behavior in response to bandwidth sharing information, which is provided solely so that reading applications can take it into account when determining whether a file can be played with restricted bandwidth delivery.</span></span>

<span data-ttu-id="8dc4d-114">El uso compartido de ancho de banda se configura con un objeto de uso compartido de ancho de banda y se agrega a un perfil antes de empezar a escribir un archivo.</span><span class="sxs-lookup"><span data-stu-id="8dc4d-114">Bandwidth sharing is configured with a bandwidth sharing object and is added to a profile before beginning to write a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8dc4d-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8dc4d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dc4d-116">**Características de archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="8dc4d-116">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="8dc4d-117">**Objeto de uso compartido de ancho de banda**</span><span class="sxs-lookup"><span data-stu-id="8dc4d-117">**Bandwidth Sharing Object**</span></span>](bandwidth-sharing-object.md)
</dt> <dt>

[<span data-ttu-id="8dc4d-118">**Interfaz IWMBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="8dc4d-118">**IWMBandwidthSharing Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="8dc4d-119">**Interfaz IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="8dc4d-119">**IWMProfile3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)
</dt> <dt>

[<span data-ttu-id="8dc4d-120">**Uso del uso compartido de ancho de banda**</span><span class="sxs-lookup"><span data-stu-id="8dc4d-120">**Using Bandwidth Sharing**</span></span>](using-bandwidth-sharing.md)
</dt> </dl>

 

 




