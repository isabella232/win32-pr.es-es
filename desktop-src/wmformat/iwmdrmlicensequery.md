---
title: Interfaz IWMDRMLicenseQuery
description: La interfaz IWMDRMLicenseQuery permite que las aplicaciones consulten los derechos y el estado de la licencia de un archivo protegido.
ms.assetid: 4ec8ff9f-0acb-4389-8995-65f24736491b
keywords:
- Interfaz IWMDRMLicenseQuery formato de Windows Media
- Interfaz IWMDRMLicenseQuery formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6463f405bf50d4d4ecb037dc542e3af0e5b7df46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792687"
---
# <a name="iwmdrmlicensequery-interface"></a><span data-ttu-id="bac86-105">Interfaz IWMDRMLicenseQuery</span><span class="sxs-lookup"><span data-stu-id="bac86-105">IWMDRMLicenseQuery interface</span></span>

<span data-ttu-id="bac86-106">La interfaz **IWMDRMLicenseQuery** permite que las aplicaciones consulten los derechos y el estado de la licencia de un archivo protegido.</span><span class="sxs-lookup"><span data-stu-id="bac86-106">The **IWMDRMLicenseQuery** interface enables applications to query the rights and license state for a protected file.</span></span> <span data-ttu-id="bac86-107">Esta interfaz usa el identificador de clave para realizar consultas en el almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="bac86-107">This interface uses the Key ID to perform queries on the local license store.</span></span>

<span data-ttu-id="bac86-108">Para obtener una instancia de esta interfaz, llame a [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="bac86-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="bac86-109">Pase el **IID \_ IWMDRMLicenseQuery** como parámetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="bac86-109">Pass **IID\_IWMDRMLicenseQuery** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="bac86-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="bac86-110">Members</span></span>

<span data-ttu-id="bac86-111">La interfaz **IWMDRMLicenseQuery** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bac86-111">The **IWMDRMLicenseQuery** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bac86-112">**IWMDRMLicenseQuery** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bac86-112">**IWMDRMLicenseQuery** also has these types of members:</span></span>

-   [<span data-ttu-id="bac86-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="bac86-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bac86-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="bac86-114">Methods</span></span>

<span data-ttu-id="bac86-115">La interfaz **IWMDRMLicenseQuery** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bac86-115">The **IWMDRMLicenseQuery** interface has these methods.</span></span>



| <span data-ttu-id="bac86-116">Método</span><span class="sxs-lookup"><span data-stu-id="bac86-116">Method</span></span>                                                                                | <span data-ttu-id="bac86-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="bac86-117">Description</span></span>                                                                                      |
|:--------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bac86-118">**QueryActionAllowed**</span><span class="sxs-lookup"><span data-stu-id="bac86-118">**QueryActionAllowed**</span></span>](iwmdrmlicensequery-queryactionallowed.md)                   | <span data-ttu-id="bac86-119">Consulta el almacén de licencias local para obtener los permisos para realizar acciones por identificador de clave.</span><span class="sxs-lookup"><span data-stu-id="bac86-119">Queries the local license store for permissions to perform actions by Key ID.</span></span><br/>         |
| [<span data-ttu-id="bac86-120">**QueryLicenseState**</span><span class="sxs-lookup"><span data-stu-id="bac86-120">**QueryLicenseState**</span></span>](iwmdrmlicensequery-querylicensestate.md)                     | <span data-ttu-id="bac86-121">Consulta el almacén de licencias local para los datos de estado de licencia por identificador de clave y derechos específicos.</span><span class="sxs-lookup"><span data-stu-id="bac86-121">Queries the local license store for license state data by Key ID and specific rights.</span></span><br/> |
| [<span data-ttu-id="bac86-122">**SetActionAllowedQueryParams**</span><span class="sxs-lookup"><span data-stu-id="bac86-122">**SetActionAllowedQueryParams**</span></span>](iwmdrmlicensequery-setactionallowedqueryparams.md) | <span data-ttu-id="bac86-123">Establece parámetros de entorno para mejorar la precisión de las consultas de licencia.</span><span class="sxs-lookup"><span data-stu-id="bac86-123">Sets environmental parameters to improve the accuracy of license queries.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="bac86-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bac86-124">Remarks</span></span>

<span data-ttu-id="bac86-125">Los métodos de **IWMDRMLicenseQuery** no proporcionan información sobre licencias individuales.</span><span class="sxs-lookup"><span data-stu-id="bac86-125">The methods of **IWMDRMLicenseQuery** do not provide information about individual licenses.</span></span> <span data-ttu-id="bac86-126">En su lugar, los datos de la licencia se agregan mediante el subsistema DRM antes de que se devuelvan los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="bac86-126">Instead, the license data is aggregated by the DRM subsystem before the query results are returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="bac86-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="bac86-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bac86-128">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="bac86-128">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

