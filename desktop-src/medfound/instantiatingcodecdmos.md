---
description: Crear instancias del códec DMOs
ms.assetid: e031d0d4-dd70-409e-8a2e-5a1433fe909e
title: Crear instancias del códec DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b98848b3e3fee5b3c28389294869eb39005c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001118"
---
# <a name="instantiating-codec-dmos"></a><span data-ttu-id="2d18f-103">Crear instancias del códec DMOs</span><span class="sxs-lookup"><span data-stu-id="2d18f-103">Instantiating Codec DMOs</span></span>

<span data-ttu-id="2d18f-104">Puede crear un códec DMO mediante una llamada a la función com [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="2d18f-104">You can create a codec DMO by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM function.</span></span> <span data-ttu-id="2d18f-105">Debe pasar el identificador de clase de DMO, el identificador de interfaz de **IMediaObject** y un puntero a un puntero **IMediaObject** .</span><span class="sxs-lookup"><span data-stu-id="2d18f-105">You must pass the class identifier of the DMO, the interface identifier of **IMediaObject**, and a pointer to an **IMediaObject** pointer.</span></span>

<span data-ttu-id="2d18f-106">Los identificadores de clase del códec DMOs se definen como constantes en el archivo de encabezado wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="2d18f-106">The class identifiers of the codec DMOs are defined as constants in the wmcodecdsp.h header file.</span></span>

<span data-ttu-id="2d18f-107">La constante para el identificador de la interfaz **IMediaObject** es IID \_ IMediaObject.</span><span class="sxs-lookup"><span data-stu-id="2d18f-107">The constant for the **IMediaObject** interface identifier is IID\_IMediaObject.</span></span>

<span data-ttu-id="2d18f-108">En el ejemplo de código siguiente se muestra cómo crear una instancia de un códec DMO:</span><span class="sxs-lookup"><span data-stu-id="2d18f-108">The following code example demonstrates how to create an instance of a codec DMO:</span></span>


```
HRESULT CreateVideoEncoderDMO(IMediaObject** ppDMO)
{
    if(ppDMO == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMediaObject, 
                            (void**)ppDMO);
}
```



## <a name="related-topics"></a><span data-ttu-id="2d18f-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2d18f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d18f-110">Trabajar con códec DMOs</span><span class="sxs-lookup"><span data-stu-id="2d18f-110">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
