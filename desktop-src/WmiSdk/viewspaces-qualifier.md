---
description: El calificador ViewSpaces define los nombres y la ubicación de los espacios de nombres donde se encuentran las instancias de origen. Puede especificar cualquier combinación de espacios de nombres en equipos locales o remotos.
ms.assetid: 15d71bb6-842d-4f5a-b2e3-e9f60f0aea3b
ms.tgt_platform: multiple
title: Calificador ViewSpaces
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSpaces
api_type:
- NA
api_location: ''
ms.openlocfilehash: 683f5596497f3c1e1ad0f2b85eaaa1460177a0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279096"
---
# <a name="viewspaces-qualifier"></a><span data-ttu-id="335aa-104">Calificador ViewSpaces</span><span class="sxs-lookup"><span data-stu-id="335aa-104">ViewSpaces Qualifier</span></span>

<span data-ttu-id="335aa-105">El **calificador ViewSpaces** define los nombres y la ubicación de los espacios de nombres donde se encuentran las instancias de origen.</span><span class="sxs-lookup"><span data-stu-id="335aa-105">The **ViewSpaces qualifier** defines the names and location of the namespaces where the source instances are located.</span></span> <span data-ttu-id="335aa-106">Puede especificar cualquier combinación de espacios de nombres en equipos locales o remotos.</span><span class="sxs-lookup"><span data-stu-id="335aa-106">You can specify any combination of namespaces on local or remote computers.</span></span>

<span data-ttu-id="335aa-107">En el ejemplo siguiente se muestran dos espacios de nombres en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="335aa-107">The following example lists two namespaces on the local computer.</span></span>


```mof
ViewSpaces{"\\\\.\\root\\LocalNamespace",
     "\\\\.\\root\\RemoteNamespace"}
```



<span data-ttu-id="335aa-108">El [proveedor de vistas](view-provider.md) hace coincidir las consultas de origen del [calificador ViewSources](viewsources-qualifier.md) con los espacios de nombres enumerados en el calificador **ViewSpaces** en el orden en que se muestran las consultas y los espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="335aa-108">The [View provider](view-provider.md) matches the source queries in the [ViewSources qualifier](viewsources-qualifier.md) to the namespaces listed in the **ViewSpaces** qualifier in the order the queries and namespaces are listed.</span></span> <span data-ttu-id="335aa-109">Normalmente, hay una relación uno a uno entre el número de espacios de nombres enumerados en el calificador **ViewSpaces** y las consultas enumeradas en el calificador **ViewSources** .</span><span class="sxs-lookup"><span data-stu-id="335aa-109">Normally, there is a one-to-one relationship between the number of namespaces listed in the **ViewSpaces** qualifier and the queries listed in the **ViewSources** qualifier.</span></span> <span data-ttu-id="335aa-110">En algunos casos, puede que desee que las consultas enumeradas en el calificador ViewSources se ejecuten en dos o más espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="335aa-110">In some cases, you may want the queries listed in the ViewSources qualifier to execute against two or more namespaces.</span></span> <span data-ttu-id="335aa-111">Puede usar un signo de dos puntos dobles "::" para separar varios espacios de nombres que se evaluarán mediante una de las consultas de la matriz **ViewSources** .</span><span class="sxs-lookup"><span data-stu-id="335aa-111">You can use a double colon "::" to separate multiple namespaces that will be evaluated by one of the queries in the **ViewSources** array.</span></span>

<span data-ttu-id="335aa-112">En el ejemplo siguiente, la primera consulta de la matriz [**ViewSources**](viewsources-qualifier.md) se ejecutará en el espacio de nombres en el primer par de Comillas, en la segunda consulta con los tres espacios de nombres en el segundo par de Comillas, y en la tercera consulta con los dos espacios de nombres del tercer par de Comillas.</span><span class="sxs-lookup"><span data-stu-id="335aa-112">In the following example, the first query in the [**ViewSources**](viewsources-qualifier.md) array will be run against the namespace in the first pair of quotes, the second query against the three namespaces in the second pair of quotes, and the third query against the two namespaces in the third pair of quotes.</span></span>


```mof
ViewSpaces
    {
    "\\\\.\\root\\LocalNamespace",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace2::
        \\\\.\\root\\RemoteNamespace3",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace3"
    }
```



## <a name="requirements"></a><span data-ttu-id="335aa-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="335aa-113">Requirements</span></span>



| <span data-ttu-id="335aa-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="335aa-114">Requirement</span></span> | <span data-ttu-id="335aa-115">Value</span><span class="sxs-lookup"><span data-stu-id="335aa-115">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="335aa-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="335aa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="335aa-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="335aa-117">Windows Vista</span></span><br/>       |
| <span data-ttu-id="335aa-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="335aa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="335aa-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="335aa-119">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="335aa-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="335aa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="335aa-121">**Calificadores específicos del proveedor de vistas**</span><span class="sxs-lookup"><span data-stu-id="335aa-121">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




