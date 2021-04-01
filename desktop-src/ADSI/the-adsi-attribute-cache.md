---
title: La caché de atributos ADSI
description: El modelo de objetos ADSI proporciona una caché de atributos de cliente para cada objeto ADSI.
ms.assetid: 0d2b4117-11f2-4b39-8fe5-3b176e4256f4
ms.tgt_platform: multiple
keywords:
- La caché de atributos ADSI ADSI
- ADSI ADSI, uso, acceso y manipulación de datos con ADSI, caché de atributos
- atributos ADSI, almacenamiento en caché de atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df3062ed5862f11e9db5dadd83b80ac624218c81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772912"
---
# <a name="the-adsi-attribute-cache"></a><span data-ttu-id="bdfa7-106">La caché de atributos ADSI</span><span class="sxs-lookup"><span data-stu-id="bdfa7-106">The ADSI Attribute Cache</span></span>

<span data-ttu-id="bdfa7-107">El modelo de objetos ADSI proporciona una caché de atributos de cliente para cada objeto ADSI.</span><span class="sxs-lookup"><span data-stu-id="bdfa7-107">The ADSI object model provides a client-side attribute cache for each ADSI object.</span></span> <span data-ttu-id="bdfa7-108">La caché de atributos es comparable a una tabla en memoria que contiene los nombres y los valores de la mayoría de los atributos de objeto que se han descargado.</span><span class="sxs-lookup"><span data-stu-id="bdfa7-108">The attribute cache is comparable to a table in memory that contains the names and values of most object attributes that have been downloaded.</span></span> <span data-ttu-id="bdfa7-109">Algunos atributos, como los atributos operativos, no se almacenan en caché.</span><span class="sxs-lookup"><span data-stu-id="bdfa7-109">Some attributes, such as operational attributes, are not cached.</span></span> <span data-ttu-id="bdfa7-110">ADSI usa el almacenamiento en caché de propiedades para mejorar el rendimiento de la manipulación de atributos y agregar la capacidad de transacción para las operaciones de lectura y escritura de atributos.</span><span class="sxs-lookup"><span data-stu-id="bdfa7-110">ADSI uses property caching to enhance the performance of attribute manipulation and add transactioning capability for attribute read and write operations.</span></span> <span data-ttu-id="bdfa7-111">Esta funcionalidad es fundamental para los clientes escritos en lenguajes que no tienen ningún mecanismo de procesamiento por lotes nativo para establecer atributos, como el sistema de desarrollo de Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bdfa7-111">This capability is critical for clients written in languages that have no native batching mechanism for setting attributes, such as Microsoft Visual Basic development system.</span></span> <span data-ttu-id="bdfa7-112">Sin la memoria caché de propiedades ADSI, estos clientes tendrían que acceder al servidor cada vez que se lee o escribe un atributo.</span><span class="sxs-lookup"><span data-stu-id="bdfa7-112">Without the ADSI property cache, such clients would have to access the server every time an attribute is read or written.</span></span>

<span data-ttu-id="bdfa7-113">Cuando se crea un objeto o se enlaza primero a, la memoria caché de propiedades del objeto está vacía.</span><span class="sxs-lookup"><span data-stu-id="bdfa7-113">When an object is created or first bound to, the property cache for the object is empty.</span></span> <span data-ttu-id="bdfa7-114">Cuando se llama al método [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) , ADSI carga los atributos solicitados para el objeto desde el servicio de directorio subyacente en la caché local.</span><span class="sxs-lookup"><span data-stu-id="bdfa7-114">When the [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is called, ADSI loads the requested attributes for the object from the underlying directory service into the local cache.</span></span> <span data-ttu-id="bdfa7-115">Cuando se lee un valor de atributo concreto y la memoria caché está vacía, ADSI realiza una llamada implícita al método **IADs:: GetInfo** .</span><span class="sxs-lookup"><span data-stu-id="bdfa7-115">When a specific attribute value is read and the cache is empty, ADSI makes an implicit call to the **IADs::GetInfo** method.</span></span> <span data-ttu-id="bdfa7-116">Cuando se rellena la memoria caché, todas las operaciones de lectura de atributo solo funcionan en el contenido de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="bdfa7-116">When the cache is filled, all attribute read operations work on the contents of the cache only.</span></span>

<span data-ttu-id="bdfa7-117">Cuando se escribe un valor de atributo, el nuevo valor se almacena en la memoria caché local hasta que se llama al método [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="bdfa7-117">When an attribute value is written, the new value is stored in the local cache until the [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span> <span data-ttu-id="bdfa7-118">Cuando se llama al método **IADs:: SetInfo** , los atributos de la memoria caché se confirman en el servicio de directorio subyacente.</span><span class="sxs-lookup"><span data-stu-id="bdfa7-118">When the **IADs::SetInfo** method is called, the attributes in the cache are committed to the underlying directory service.</span></span> <span data-ttu-id="bdfa7-119">Después de llamar al método **IADs:: SetInfo** , los valores permanecen en la memoria caché hasta que se actualizan explícitamente con otra llamada al método [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) .</span><span class="sxs-lookup"><span data-stu-id="bdfa7-119">After the **IADs::SetInfo** method is called, the values remain in the cache until explicitly refreshed with another call to the [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bdfa7-120">El método [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) debe utilizarse con cuidado, ya que este método siempre sobrescribirá los valores de atributo en la memoria caché del servicio de directorio subyacente, incluso si se ha cambiado el valor almacenado en caché.</span><span class="sxs-lookup"><span data-stu-id="bdfa7-120">The [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method must be used carefully because this method will always overwrite the attribute values in the cache from the underlying directory service, even if the cached value has been changed.</span></span> <span data-ttu-id="bdfa7-121">Es decir, sobrescribirá los valores de atributo que se han modificado en la memoria caché, pero que no se han confirmado en el servicio de directorio subyacente con una llamada al método [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="bdfa7-121">That is, it will overwrite attribute values that have been changed in the cache, but not committed to the underlying directory service with a call to the [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span>

 

<span data-ttu-id="bdfa7-122">En la siguiente ilustración se muestran los distintos métodos que se usan para operar en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="bdfa7-122">The following figure shows the different methods used to operate on the cache.</span></span>

![caché de atributos ADSI](images/ds2propc.png)

 

 




