---
title: CPRPOBJ. CPP
description: En el componente proveedor de ejemplo, los métodos de objeto de propiedad, en cprpobj. cpp, se muestran en la tabla siguiente.
ms.assetid: 88628b9b-12e6-4d64-9a21-b30f7392a5f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948409cc135daaffa249f8aa0b3729b34799957c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268264"
---
# <a name="cprpobjcpp"></a><span data-ttu-id="36007-103">CPRPOBJ. CPP</span><span class="sxs-lookup"><span data-stu-id="36007-103">CPRPOBJ.CPP</span></span>

<span data-ttu-id="36007-104">En el componente proveedor de ejemplo, los métodos de objeto de propiedad, en cprpobj. cpp, se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="36007-104">In the example provider component, property object methods, in cprpobj.cpp, are listed in the following table.</span></span>



| <span data-ttu-id="36007-105">Método</span><span class="sxs-lookup"><span data-stu-id="36007-105">Method</span></span>                                                 | <span data-ttu-id="36007-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="36007-106">Description</span></span>                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36007-107">**CSampleDSProperty::CSampleDSProperty**</span><span class="sxs-lookup"><span data-stu-id="36007-107">**CSampleDSProperty::CSampleDSProperty**</span></span>               | <span data-ttu-id="36007-108">Constructor estándar.</span><span class="sxs-lookup"><span data-stu-id="36007-108">Standard constructor.</span></span>                                                                                                                          |
| <span data-ttu-id="36007-109">**CSampleDSProperty:: ~ CSampleDSProperty**</span><span class="sxs-lookup"><span data-stu-id="36007-109">**CSampleDSProperty::~CSampleDSProperty**</span></span>              | <span data-ttu-id="36007-110">Destructor estándar.</span><span class="sxs-lookup"><span data-stu-id="36007-110">Standard destructor.</span></span>                                                                                                                           |
| <span data-ttu-id="36007-111">**CSampleDSProperty:: CreateProperty**</span><span class="sxs-lookup"><span data-stu-id="36007-111">**CSampleDSProperty::CreateProperty**</span></span>                  | <span data-ttu-id="36007-112">Cree un objeto de propiedad ADS, buscando las definiciones de atributo mediante una llamada a **SampleDSGetPropertyDefinition**.</span><span class="sxs-lookup"><span data-stu-id="36007-112">Create an ADS Property object, looking up the attribute definitions by calling **SampleDSGetPropertyDefinition**.</span></span>                              |
| <span data-ttu-id="36007-113">**CSampleDSProperty:: CreateProperty**</span><span class="sxs-lookup"><span data-stu-id="36007-113">**CSampleDSProperty::CreateProperty**</span></span>                  | <span data-ttu-id="36007-114">Dada la definición de atributo, cree un objeto de propiedad y establezca la correspondencia entre las sintaxis de ADS admitidas y las sintaxis del proveedor.</span><span class="sxs-lookup"><span data-stu-id="36007-114">Given the attribute definition, create a property object, setting the correspondence between supported ADS syntaxes and the provider syntaxes.</span></span> |
| <span data-ttu-id="36007-115">**CSampleDSProperty::AllocatePropertyObject**</span><span class="sxs-lookup"><span data-stu-id="36007-115">**CSampleDSProperty::AllocatePropertyObject**</span></span>          | <span data-ttu-id="36007-116">Cree un objeto de propiedad y cargue sus datos de tipo.</span><span class="sxs-lookup"><span data-stu-id="36007-116">Create a property object and load its type data.</span></span>                                                                                               |
| <span data-ttu-id="36007-117">**CSampleDSProperty:: QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="36007-117">**CSampleDSProperty::QueryInterface**</span></span>                  | <span data-ttu-id="36007-118">Devuelve el puntero de interfaz solicitado, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="36007-118">Return the requested interface pointer, if available.</span></span>                                                                                          |
| <span data-ttu-id="36007-119">Métodos [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) estándar.</span><span class="sxs-lookup"><span data-stu-id="36007-119">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) methods.</span></span>                 |                                                                                                                                                |
| <span data-ttu-id="36007-120">Métodos estándar de [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) .</span><span class="sxs-lookup"><span data-stu-id="36007-120">Standard [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) methods.</span></span> |                                                                                                                                                |
| <span data-ttu-id="36007-121">**MapSyntaxIdtoADsSyntax**</span><span class="sxs-lookup"><span data-stu-id="36007-121">**MapSyntaxIdtoADsSyntax**</span></span>                             | <span data-ttu-id="36007-122">Establezca la correspondencia entre el identificador de sintaxis y la sintaxis de ADS.</span><span class="sxs-lookup"><span data-stu-id="36007-122">Set the correspondence between the syntax ID and the ADS syntax.</span></span>                                                                               |
| <span data-ttu-id="36007-123">**MapSyntaxIdtoSampleDSSyntax**</span><span class="sxs-lookup"><span data-stu-id="36007-123">**MapSyntaxIdtoSampleDSSyntax**</span></span>                        | <span data-ttu-id="36007-124">Establezca la correspondencia entre el identificador de sintaxis y la sintaxis del proveedor.</span><span class="sxs-lookup"><span data-stu-id="36007-124">Set the correspondence between the syntax ID and the provider syntax.</span></span>                                                                          |



 

 

 




