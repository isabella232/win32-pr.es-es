---
title: Operaciones de Access Control y escritura
description: Se producirá un error en las modificaciones de propiedad si el autor de la llamada no tiene derechos suficientes.
ms.assetid: eb5b97fb-4654-444e-9f5a-9a4be27ef1a3
ms.tgt_platform: multiple
keywords:
- AD operaciones de Access Control y Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b8ecab475cd5696a98c985f92ccc24b1dd6072
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904463"
---
# <a name="access-control-and-write-operations"></a><span data-ttu-id="0c074-104">Operaciones de Access Control y escritura</span><span class="sxs-lookup"><span data-stu-id="0c074-104">Access Control and Write Operations</span></span>

<span data-ttu-id="0c074-105">Se producirá un error en las modificaciones de propiedad si el autor de la llamada no tiene derechos suficientes.</span><span class="sxs-lookup"><span data-stu-id="0c074-105">Property modifications fail if the caller does not have sufficient rights.</span></span> <span data-ttu-id="0c074-106">En el caso de las operaciones de escritura que realizan modificaciones por lotes en varias propiedades, se produce un error en toda la operación si el llamador no tiene los derechos necesarios en una sola de las propiedades modificadas.</span><span class="sxs-lookup"><span data-stu-id="0c074-106">For write operations that batch modifications to multiple properties, the entire operation fails if the caller does not have the necessary rights to a single one of the modified properties.</span></span> <span data-ttu-id="0c074-107">Por ejemplo, puede crear varias llamadas [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) para establecer varias propiedades en un objeto.</span><span class="sxs-lookup"><span data-stu-id="0c074-107">For example, you can make multiple [**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put) calls to set multiple properties on an object.</span></span> <span data-ttu-id="0c074-108">Sin embargo, al llamar a [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para escribir los datos nuevos de la memoria caché local en el directorio, se producirá un error en **SetInfo** si el autor de la llamada no tiene acceso de escritura a todas las propiedades modificadas.</span><span class="sxs-lookup"><span data-stu-id="0c074-108">However, when you call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to write the new data from the local cache to the directory, **SetInfo** will fail if the caller does not have write access to all the modified properties.</span></span> <span data-ttu-id="0c074-109">Del mismo modo, el método [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) no establece ninguna propiedad si el autor de la llamada no tiene acceso a todas las propiedades que se están configurando.</span><span class="sxs-lookup"><span data-stu-id="0c074-109">Similarly, the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) method fails to set any properties if the caller does not have access to all the properties being set.</span></span> <span data-ttu-id="0c074-110">Por lo tanto, debe procesar varias operaciones de modificación solo si sabe que todas las modificaciones se realizarán correctamente.</span><span class="sxs-lookup"><span data-stu-id="0c074-110">So you should batch multiple modify operations only if you know that all modifications will succeed.</span></span> <span data-ttu-id="0c074-111">Para determinar los atributos de un objeto de directorio que el autor de la llamada tiene la capacidad de modificar, lea el atributo **allowedAttributesEffective** del objeto.</span><span class="sxs-lookup"><span data-stu-id="0c074-111">To determine the attributes of a directory object that the caller has the ability to modify, read the object's **allowedAttributesEffective** attribute.</span></span>

<span data-ttu-id="0c074-112">Si el autor de la llamada no tiene derechos suficientes para modificar una propiedad, se pueden devolver los siguientes códigos de retorno:</span><span class="sxs-lookup"><span data-stu-id="0c074-112">If the caller does not have sufficient rights to modify a property, the following return codes may be returned:</span></span>

<span data-ttu-id="0c074-113">\_propiedad de \_ ADS \_ no \_ establecida e \_ ADS \_ propiedad \_ no \_ modificada</span><span class="sxs-lookup"><span data-stu-id="0c074-113">E\_ADS\_PROPERTY\_NOT\_SET E\_ADS\_PROPERTY\_NOT\_MODIFIED</span></span>

 

 