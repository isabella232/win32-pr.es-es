---
description: Lo llama la interfaz IeAxiSystemInstaller para comprobar que se puede instalar un objeto ActiveX.
ms.assetid: d5cd6263-d07e-4261-9463-b9a06e883f16
title: Interfaz IeAxiServiceCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3ad276126548ac6d5fdc2c828f722c90b43ad679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913642"
---
# <a name="ieaxiservicecallback-interface"></a><span data-ttu-id="9abea-103">Interfaz IeAxiServiceCallback</span><span class="sxs-lookup"><span data-stu-id="9abea-103">IeAxiServiceCallback interface</span></span>

<span data-ttu-id="9abea-104">La interfaz [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) llama a la interfaz **IeAxiServiceCallback** para comprobar que se puede instalar un objeto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="9abea-104">The **IeAxiServiceCallback** interface is called by the [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) interface to verify that an ActiveX object can be installed.</span></span>

<span data-ttu-id="9abea-105">La clase [**CIeAxiInstallerService**](cieaxiinstallerservice.md) implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="9abea-105">The [**CIeAxiInstallerService**](cieaxiinstallerservice.md) class implements this interface.</span></span>

<span data-ttu-id="9abea-106">Esta interfaz no está declarada en un encabezado público.</span><span class="sxs-lookup"><span data-stu-id="9abea-106">This interface is not declared in a public header.</span></span> <span data-ttu-id="9abea-107">Las aplicaciones deben definirla.</span><span class="sxs-lookup"><span data-stu-id="9abea-107">Applications must define it themselves.</span></span> <span data-ttu-id="9abea-108">El siguiente fragmento del lenguaje de definición de interfaz (IDL) describe esta interfaz, incluido su IID.</span><span class="sxs-lookup"><span data-stu-id="9abea-108">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(1823E7BA-EC36-447a-9B2E-B4912E15AFE7),
    dual,
    nonextensible,
    pointer_default(unique)
]

interface IeAxiServiceCallback : IUnknown
{
    HRESULT VerifyFile(
                       [in] BSTR bstrFileUrl,
                       [out] BSTR * bstrApprovedFileName);
}

```

## <a name="members"></a><span data-ttu-id="9abea-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9abea-109">Members</span></span>

<span data-ttu-id="9abea-110">La interfaz **IeAxiServiceCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9abea-110">The **IeAxiServiceCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9abea-111">**IeAxiServiceCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9abea-111">**IeAxiServiceCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="9abea-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9abea-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9abea-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="9abea-113">Methods</span></span>

<span data-ttu-id="9abea-114">La interfaz **IeAxiServiceCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9abea-114">The **IeAxiServiceCallback** interface has these methods.</span></span>



| <span data-ttu-id="9abea-115">Método</span><span class="sxs-lookup"><span data-stu-id="9abea-115">Method</span></span>                                                | <span data-ttu-id="9abea-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="9abea-116">Description</span></span>                                                                                                                                    |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9abea-117">**VerifyFile**</span><span class="sxs-lookup"><span data-stu-id="9abea-117">**VerifyFile**</span></span>](ieaxiservicecallback-verifyfile.md) | <span data-ttu-id="9abea-118">Realiza comprobaciones de seguridad en el objeto ActiveX especificado y devuelve la ubicación donde se descargó el archivo. CAB correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9abea-118">Performs security checks on the specified ActiveX object and returns the location where the corresponding .cab file was downloaded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9abea-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9abea-119">Requirements</span></span>



| <span data-ttu-id="9abea-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9abea-120">Requirement</span></span> | <span data-ttu-id="9abea-121">Value</span><span class="sxs-lookup"><span data-stu-id="9abea-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9abea-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9abea-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9abea-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="9abea-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9abea-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9abea-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9abea-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9abea-125">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="9abea-126">IID</span><span class="sxs-lookup"><span data-stu-id="9abea-126">IID</span></span><br/>                      | <span data-ttu-id="9abea-127">IID \_ IeAxiServiceCallback se define como 1823E7BA-EC36-447A-9B2E-B4912E15AFE7</span><span class="sxs-lookup"><span data-stu-id="9abea-127">IID\_IeAxiServiceCallback is defined as 1823E7BA-EC36-447a-9B2E-B4912E15AFE7</span></span><br/>                   |



 

