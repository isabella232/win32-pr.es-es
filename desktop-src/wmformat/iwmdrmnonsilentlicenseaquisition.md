---
title: Interfaz IWMDRMNonSilentLicenseAquisition
description: La interfaz IWMDRMNonSilentLicenseAquisition proporciona métodos que permiten adquirir licencias que requieren la intervención del usuario. Esta interfaz se puede obtener realizando una adquisición de licencias no silenciosa.
ms.assetid: 57dc3daa-d457-49b0-b589-a72ba180e75e
keywords:
- Interfaz IWMDRMNonSilentLicenseAquisition formato de Windows Media
- Interfaz IWMDRMNonSilentLicenseAquisition formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89fce7764b755231812c761778131c159ddd860b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792682"
---
# <a name="iwmdrmnonsilentlicenseaquisition-interface"></a><span data-ttu-id="a560b-105">Interfaz IWMDRMNonSilentLicenseAquisition</span><span class="sxs-lookup"><span data-stu-id="a560b-105">IWMDRMNonSilentLicenseAquisition interface</span></span>

<span data-ttu-id="a560b-106">La interfaz **IWMDRMNonSilentLicenseAquisition** proporciona métodos que permiten adquirir licencias que requieren la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="a560b-106">The **IWMDRMNonSilentLicenseAquisition** interface provides methods that enable license acquisition requiring user intervention.</span></span>

<span data-ttu-id="a560b-107">Esta interfaz se puede obtener realizando una adquisición de licencias no silenciosa.</span><span class="sxs-lookup"><span data-stu-id="a560b-107">This interface can be obtained by performing non-silent license acquisition.</span></span> <span data-ttu-id="a560b-108">Después de llamar a [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) , se generará un evento **MEWMDRMLicenseAcquisitionCompleted** .</span><span class="sxs-lookup"><span data-stu-id="a560b-108">After you call [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) an **MEWMDRMLicenseAcquisitionCompleted** event will be generated.</span></span> <span data-ttu-id="a560b-109">Llame al método **IMFMediaEvent:: GetValue** del evento para obtener un puntero a una interfaz **IUnknown** que se puede consultar para un puntero a una instancia de esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="a560b-109">Call the **IMFMediaEvent::GetValue** method of the event to get a pointer to an **IUnknown** interface that can be queried for a pointer to an instance of this interface.</span></span>

## <a name="members"></a><span data-ttu-id="a560b-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="a560b-110">Members</span></span>

<span data-ttu-id="a560b-111">La interfaz **IWMDRMNonSilentLicenseAquisition** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a560b-111">The **IWMDRMNonSilentLicenseAquisition** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a560b-112">**IWMDRMNonSilentLicenseAquisition** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a560b-112">**IWMDRMNonSilentLicenseAquisition** also has these types of members:</span></span>

-   [<span data-ttu-id="a560b-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="a560b-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a560b-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="a560b-114">Methods</span></span>

<span data-ttu-id="a560b-115">La interfaz **IWMDRMNonSilentLicenseAquisition** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a560b-115">The **IWMDRMNonSilentLicenseAquisition** interface has these methods.</span></span>



| <span data-ttu-id="a560b-116">Método</span><span class="sxs-lookup"><span data-stu-id="a560b-116">Method</span></span>                                                                | <span data-ttu-id="a560b-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a560b-117">Description</span></span>                                                                             |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="a560b-118">**GetChallenge**</span><span class="sxs-lookup"><span data-stu-id="a560b-118">**GetChallenge**</span></span>](iwmdrmnonsilentlicenseaquisition-getchallenge.md) | <span data-ttu-id="a560b-119">Recupera el desafío de la licencia que debe publicarse en el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="a560b-119">Retrieves the license challenge that should be posted to the license server.</span></span><br/> |
| [<span data-ttu-id="a560b-120">**GetURL**</span><span class="sxs-lookup"><span data-stu-id="a560b-120">**GetURL**</span></span>](iwmdrmnonsilentlicenseaquisition-geturl.md)             | <span data-ttu-id="a560b-121">Recupera la dirección URL a la que se debe publicar el desafío de licencia.</span><span class="sxs-lookup"><span data-stu-id="a560b-121">Retrieves the URL to which the license challenge should be posted.</span></span><br/>           |



 

## <a name="see-also"></a><span data-ttu-id="a560b-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a560b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a560b-123">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="a560b-123">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a560b-124">**Adquisición de licencias no silenciosa**</span><span class="sxs-lookup"><span data-stu-id="a560b-124">**Non-Silent License Acquisition**</span></span>](non-silent-license-acquisition.md)
</dt> </dl>

 

