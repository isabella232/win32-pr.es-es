---
description: Instala un objeto ActiveX.
ms.assetid: 0eb725a9-ceb8-40e5-808d-ac2b286a48b6
title: Interfaz IeAxiSystemInstaller
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 391088a70aa845cd685511f10e4eb6e809dc7fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083253"
---
# <a name="ieaxisysteminstaller-interface"></a><span data-ttu-id="cd598-103">Interfaz IeAxiSystemInstaller</span><span class="sxs-lookup"><span data-stu-id="cd598-103">IeAxiSystemInstaller interface</span></span>

<span data-ttu-id="cd598-104">La interfaz **IeAxiSystemInstaller** instala un objeto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="cd598-104">The **IeAxiSystemInstaller** interface installs an ActiveX object.</span></span>

<span data-ttu-id="cd598-105">Esta interfaz no está declarada en un encabezado público.</span><span class="sxs-lookup"><span data-stu-id="cd598-105">This interface is not declared in a public header.</span></span> <span data-ttu-id="cd598-106">Las aplicaciones deben definirla.</span><span class="sxs-lookup"><span data-stu-id="cd598-106">Applications must define it themselves.</span></span> <span data-ttu-id="cd598-107">El siguiente fragmento del lenguaje de definición de interfaz (IDL) describe esta interfaz, incluido su IID.</span><span class="sxs-lookup"><span data-stu-id="cd598-107">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(a50ea6f8-4764-4299-b309-022b2a8b4d8d),
    
]
interface IeAxiSystemInstaller : IUnknown
{
    
    HRESULT InitializeSystemInstaller(  [in] BSTR bstrUrl,
                                  [in] DWORD dwClientPID,
                                  [in] IUnknown* pCallback,
                                  [out] BSTR * pbstrNonce);
}

```

## <a name="members"></a><span data-ttu-id="cd598-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="cd598-108">Members</span></span>

<span data-ttu-id="cd598-109">La interfaz **IeAxiSystemInstaller** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cd598-109">The **IeAxiSystemInstaller** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cd598-110">**IeAxiSystemInstaller** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cd598-110">**IeAxiSystemInstaller** also has these types of members:</span></span>

-   [<span data-ttu-id="cd598-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="cd598-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cd598-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="cd598-112">Methods</span></span>

<span data-ttu-id="cd598-113">La interfaz **IeAxiSystemInstaller** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="cd598-113">The **IeAxiSystemInstaller** interface has these methods.</span></span>



| <span data-ttu-id="cd598-114">Método</span><span class="sxs-lookup"><span data-stu-id="cd598-114">Method</span></span>                                                                              | <span data-ttu-id="cd598-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd598-115">Description</span></span>                                       |
|:------------------------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="cd598-116">**InitializeSystemInstaller**</span><span class="sxs-lookup"><span data-stu-id="cd598-116">**InitializeSystemInstaller**</span></span>](ieaxisysteminstaller-initializesysteminstaller.md) | <span data-ttu-id="cd598-117">Instala el objeto ActiveX especificado.</span><span class="sxs-lookup"><span data-stu-id="cd598-117">Installs the specified ActiveX object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cd598-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd598-118">Requirements</span></span>



| <span data-ttu-id="cd598-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd598-119">Requirement</span></span> | <span data-ttu-id="cd598-120">Value</span><span class="sxs-lookup"><span data-stu-id="cd598-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd598-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd598-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cd598-122">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="cd598-122">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="cd598-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd598-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cd598-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cd598-124">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="cd598-125">IID</span><span class="sxs-lookup"><span data-stu-id="cd598-125">IID</span></span><br/>                      | <span data-ttu-id="cd598-126">IID \_ IeAxiSystemInstaller se define como a50ea6f8-4764-4299-B309-022b2a8b4d8d</span><span class="sxs-lookup"><span data-stu-id="cd598-126">IID\_IeAxiSystemInstaller is defined as a50ea6f8-4764-4299-b309-022b2a8b4d8d</span></span><br/>                   |



 

