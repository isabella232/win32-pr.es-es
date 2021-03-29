---
title: CENUMVAR. CPP
description: En el componente de proveedor de ejemplo, la implementación base para las clases derivadas de xxxEnumVariant se puede encontrar en cenumvar. cpp. En la tabla siguiente se enumeran los métodos asociados.
ms.assetid: 6b38bc99-25d4-40af-863a-9cc37f786d9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d361cb7d3e2657a31645fba05aa2e1a23762a3fc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359408"
---
# <a name="cenumvarcpp"></a><span data-ttu-id="a0ad0-104">CENUMVAR. CPP</span><span class="sxs-lookup"><span data-stu-id="a0ad0-104">CENUMVAR.CPP</span></span>

<span data-ttu-id="a0ad0-105">En el componente de proveedor de ejemplo, la implementación base para las clases derivadas de xxxEnumVariant se puede encontrar en cenumvar. cpp.</span><span class="sxs-lookup"><span data-stu-id="a0ad0-105">In the example provider component, the base implementation for xxxEnumVariant derived classes can be found in cenumvar.cpp.</span></span> <span data-ttu-id="a0ad0-106">En la tabla siguiente se enumeran los métodos asociados.</span><span class="sxs-lookup"><span data-stu-id="a0ad0-106">Associated methods are listed in the following table.</span></span>



| <span data-ttu-id="a0ad0-107">Método</span><span class="sxs-lookup"><span data-stu-id="a0ad0-107">Method</span></span>                                          | <span data-ttu-id="a0ad0-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0ad0-108">Description</span></span>                                                                           |
|-------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ad0-109">**CSampleDSEnumVariant::CSampleDSEnumVariant**</span><span class="sxs-lookup"><span data-stu-id="a0ad0-109">**CSampleDSEnumVariant::CSampleDSEnumVariant**</span></span>  | <span data-ttu-id="a0ad0-110">Constructor estándar.</span><span class="sxs-lookup"><span data-stu-id="a0ad0-110">Standard constructor.</span></span>                                                                 |
| <span data-ttu-id="a0ad0-111">**CSampleDSEnumVariant:: ~ CSampleDSEnumVariant**</span><span class="sxs-lookup"><span data-stu-id="a0ad0-111">**CSampleDSEnumVariant::~CSampleDSEnumVariant**</span></span> | <span data-ttu-id="a0ad0-112">Destructor estándar.</span><span class="sxs-lookup"><span data-stu-id="a0ad0-112">Standard destructor.</span></span>                                                                  |
| <span data-ttu-id="a0ad0-113">**CSampleDSEnumVariant:: QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="a0ad0-113">**CSampleDSEnumVariant::QueryInterface**</span></span>        | <span data-ttu-id="a0ad0-114">Implementación de [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) estándar.</span><span class="sxs-lookup"><span data-stu-id="a0ad0-114">Standard [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) implementation.</span></span> |
| <span data-ttu-id="a0ad0-115">**CSampleDSEnumVariant:: AddRef**</span><span class="sxs-lookup"><span data-stu-id="a0ad0-115">**CSampleDSEnumVariant::AddRef**</span></span>                | <span data-ttu-id="a0ad0-116">Implementación [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) estándar.</span><span class="sxs-lookup"><span data-stu-id="a0ad0-116">Standard [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) implementation.</span></span>                 |
| <span data-ttu-id="a0ad0-117">**CSampleDSEnumVariant:: Release**</span><span class="sxs-lookup"><span data-stu-id="a0ad0-117">**CSampleDSEnumVariant::Release**</span></span>               | <span data-ttu-id="a0ad0-118">Implementación estándar de [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="a0ad0-118">Standard [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) implementation.</span></span>               |
| <span data-ttu-id="a0ad0-119">**CSampleDSEnumVariant:: Skip**</span><span class="sxs-lookup"><span data-stu-id="a0ad0-119">**CSampleDSEnumVariant::Skip**</span></span>                  | <span data-ttu-id="a0ad0-120">Implementación estándar de **IEnumXXXX:: Skip** .</span><span class="sxs-lookup"><span data-stu-id="a0ad0-120">Standard **IEnumXXXX::Skip** implementation.</span></span>                                          |
| <span data-ttu-id="a0ad0-121">**CSampleDSEnumVariant:: RESET**</span><span class="sxs-lookup"><span data-stu-id="a0ad0-121">**CSampleDSEnumVariant::Reset**</span></span>                 | <span data-ttu-id="a0ad0-122">Implementación estándar de **IEnumXXXX:: RESET** .</span><span class="sxs-lookup"><span data-stu-id="a0ad0-122">Standard **IEnumXXXX::Reset** implementation.</span></span>                                         |
| <span data-ttu-id="a0ad0-123">**CSampleDSEnumVariant:: Clone**</span><span class="sxs-lookup"><span data-stu-id="a0ad0-123">**CSampleDSEnumVariant::Clone**</span></span>                 | <span data-ttu-id="a0ad0-124">Implementación estándar de **IEnumXXXX:: Clone** .</span><span class="sxs-lookup"><span data-stu-id="a0ad0-124">Standard **IEnumXXXX::Clone** implementation.</span></span>                                         |



 

 

 