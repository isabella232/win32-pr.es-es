---
title: La estructura STGMEDIUM
description: La estructura STGMEDIUM
ms.assetid: ff1e1128-d228-45a6-a19d-2875b6c4e003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86faf52ab93bab39b8413ea2eb6381da24b643b5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "104078586"
---
# <a name="the-stgmedium-structure"></a><span data-ttu-id="db96c-103">La estructura STGMEDIUM</span><span class="sxs-lookup"><span data-stu-id="db96c-103">The STGMEDIUM Structure</span></span>

<span data-ttu-id="db96c-104">Del mismo modo que la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) es una mejora del identificador de formato del portapapeles de Windows, por lo que la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) es una mejora del identificador de memoria global que se usa para transferir los datos.</span><span class="sxs-lookup"><span data-stu-id="db96c-104">Just as the [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) structure is an enhancement of the Windows clipboard format identifier, so the [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure is an improvement of the global memory handle used to transfer the data.</span></span> <span data-ttu-id="db96c-105">La estructura **STGMEDIUM** incluye un miembro, **tymed**, que indica el medio que se va a usar y una Unión que incluye punteros y un identificador para obtener el medio especificado en **tymed**.</span><span class="sxs-lookup"><span data-stu-id="db96c-105">The **STGMEDIUM** structure includes a member, **tymed**, which indicates the medium to be used, and a union comprising pointers and a handle for getting whichever medium is specified in **tymed**.</span></span>

<span data-ttu-id="db96c-106">La estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) permite a los orígenes de datos y a los consumidores elegir el medio de Exchange más eficaz para cada representación.</span><span class="sxs-lookup"><span data-stu-id="db96c-106">The [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure enables both data sources and consumers to choose the most efficient exchange medium on a per-rendering basis.</span></span> <span data-ttu-id="db96c-107">Si los datos son tan grandes que deben mantenerse en el disco, el origen de datos puede indicar un medio basado en disco en su formato preferido, usando solo la memoria global como copia de seguridad si ese es el único medio que entiende el consumidor.</span><span class="sxs-lookup"><span data-stu-id="db96c-107">If the data is so large that it should be kept on disk, the data source can indicate a disk-based medium in its preferred format, only using global memory as a backup if that's the only medium the consumer understands.</span></span> <span data-ttu-id="db96c-108">Poder usar el mejor medio para los intercambios como valor predeterminado mejora el rendimiento general del intercambio de datos entre aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="db96c-108">Being able to use the best medium for exchanges as the default improves overall performance of data exchange between applications.</span></span> <span data-ttu-id="db96c-109">Por ejemplo, si algunos de los datos que se van a transferir ya están en el disco, la aplicación de origen puede moverla o copiarlos en un nuevo destino, ya sea en la misma aplicación o en otros, sin tener que cargar primero los datos en la memoria global.</span><span class="sxs-lookup"><span data-stu-id="db96c-109">For example, if some of the data to be transferred is already on disk, the source application can move or copy it to a new destination, either in the same application or in some other, without having first to load the data into global memory.</span></span> <span data-ttu-id="db96c-110">En el extremo receptor, el consumidor de los datos no tiene que volver a escribirlo en el disco.</span><span class="sxs-lookup"><span data-stu-id="db96c-110">At the receiving end, the consumer of the data does not have to write it back to disk.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db96c-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="db96c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db96c-112">Formatos de datos y medios de transferencia</span><span class="sxs-lookup"><span data-stu-id="db96c-112">Data Formats and Transfer Media</span></span>](data-formats-and-transfer-media.md)
</dt> </dl>

 

 




