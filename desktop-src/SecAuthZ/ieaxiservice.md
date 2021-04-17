---
description: Inicializa un objeto de servicio de sistema para instalar un objeto ActiveX cuando el usuario actual no tiene permiso para instalar el objeto.
ms.assetid: 42f7cf83-789b-42ea-bb1a-4b79137188ea
title: Interfaz IeAxiService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService
api_type:
- COM
api_location: ''
ms.openlocfilehash: 34c4743327b2539616dee6b09c34d9f479aa3303
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668053"
---
# <a name="ieaxiservice-interface"></a><span data-ttu-id="2da8d-103">Interfaz IeAxiService</span><span class="sxs-lookup"><span data-stu-id="2da8d-103">IeAxiService interface</span></span>

<span data-ttu-id="2da8d-104">La interfaz **IAxiService** Inicializa un objeto de servicio de sistema para instalar un objeto ActiveX cuando el usuario actual no tiene permiso para instalar el objeto.</span><span class="sxs-lookup"><span data-stu-id="2da8d-104">The **IAxiService** interface initializes a system service object to install an ActiveX object when the current user does not have permission to install the object.</span></span>

<span data-ttu-id="2da8d-105">La clase [**CIeAxiInstallerService**](cieaxiinstallerservice.md) implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="2da8d-105">The [**CIeAxiInstallerService**](cieaxiinstallerservice.md) class implements this interface.</span></span>

<span data-ttu-id="2da8d-106">Esta interfaz no está declarada en un encabezado público.</span><span class="sxs-lookup"><span data-stu-id="2da8d-106">This interface is not declared in a public header.</span></span> <span data-ttu-id="2da8d-107">Las aplicaciones deben definirla.</span><span class="sxs-lookup"><span data-stu-id="2da8d-107">Applications must define it themselves.</span></span> <span data-ttu-id="2da8d-108">El siguiente fragmento del lenguaje de definición de interfaz (IDL) describe esta interfaz, incluido su IID.</span><span class="sxs-lookup"><span data-stu-id="2da8d-108">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(E9E92380-9ECD-4982-A0EB-6815A56CCF27),
    pointer_default(unique)
]

interface IeAxiService : IUnknown{

    
    HRESULT Initialize(
            [in]        HWND            hwndParent,
            [in]        DWORD           dwClientPID,
            [in]        BSTR            bstrDesktop,
            [in]        BSTR            bstrClsID,              
            [in]        BSTR            bstrURL,                
            [out]       BSTR *          pbstrNonce,            
            [out]       IUnknown**      ppISyncBrokerInterface  
            );  
 
    HRESULT Cleanup();
};
```

## <a name="members"></a><span data-ttu-id="2da8d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2da8d-109">Members</span></span>

<span data-ttu-id="2da8d-110">La interfaz **IeAxiService** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2da8d-110">The **IeAxiService** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2da8d-111">**IeAxiService** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2da8d-111">**IeAxiService** also has these types of members:</span></span>

-   [<span data-ttu-id="2da8d-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="2da8d-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2da8d-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="2da8d-113">Methods</span></span>

<span data-ttu-id="2da8d-114">La interfaz **IeAxiService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2da8d-114">The **IeAxiService** interface has these methods.</span></span>



| <span data-ttu-id="2da8d-115">Método</span><span class="sxs-lookup"><span data-stu-id="2da8d-115">Method</span></span>                                        | <span data-ttu-id="2da8d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2da8d-116">Description</span></span>                                                        |
|:----------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="2da8d-117">**Limpieza**</span><span class="sxs-lookup"><span data-stu-id="2da8d-117">**Cleanup**</span></span>](ieaxiservice-cleanup.md)       | <span data-ttu-id="2da8d-118">Libera los recursos utilizados por la interfaz **IeAxiService** .</span><span class="sxs-lookup"><span data-stu-id="2da8d-118">Frees resources used by the **IeAxiService** interface.</span></span><br/> |
| [<span data-ttu-id="2da8d-119">**Inicialización**</span><span class="sxs-lookup"><span data-stu-id="2da8d-119">**Initialize**</span></span>](ieaxiservice-initialize.md) | <span data-ttu-id="2da8d-120">Comprueba y descarga un objeto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="2da8d-120">Checks and downloads an ActiveX object.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="2da8d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2da8d-121">Requirements</span></span>



| <span data-ttu-id="2da8d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2da8d-122">Requirement</span></span> | <span data-ttu-id="2da8d-123">Value</span><span class="sxs-lookup"><span data-stu-id="2da8d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2da8d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2da8d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2da8d-125">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="2da8d-125">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2da8d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2da8d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2da8d-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2da8d-127">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="2da8d-128">IID</span><span class="sxs-lookup"><span data-stu-id="2da8d-128">IID</span></span><br/>                      | <span data-ttu-id="2da8d-129">IID \_ IeAxiService se define como E9E92380-9ECD-4982-A0EB-6815A56CCF27</span><span class="sxs-lookup"><span data-stu-id="2da8d-129">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



 

