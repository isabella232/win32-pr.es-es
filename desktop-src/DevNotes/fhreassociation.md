---
description: Representa la característica de reasociación del historial de archivos, que permite a un usuario restablecer una relación con un destino de copia de seguridad utilizado por el mismo usuario en el pasado. La reasociación se realiza mediante una llamada a los métodos de la interfaz IFhReassociation.
ms.assetid: BB81F8ED-4DFB-4FA5-B3ED-ACBAB32BBE3D
title: Clase FhReassociation (Fhcfg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhReassociation
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 1e303799a792e788fcb948ad6d3c6e2fd732e26e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659535"
---
# <a name="fhreassociation-class"></a><span data-ttu-id="c00b4-104">Clase FhReassociation</span><span class="sxs-lookup"><span data-stu-id="c00b4-104">FhReassociation class</span></span>

<span data-ttu-id="c00b4-105">Representa la característica de reasociación del historial de archivos, que permite a un usuario restablecer una relación con un destino de copia de seguridad utilizado por el mismo usuario en el pasado.</span><span class="sxs-lookup"><span data-stu-id="c00b4-105">Represents the File History reassociation feature, which allows a user to reestablish a relationship with a backup target that was used by the same user in the past.</span></span> <span data-ttu-id="c00b4-106">La reasociación se realiza mediante una llamada a los métodos de la interfaz [**IFhReassociation**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) .</span><span class="sxs-lookup"><span data-stu-id="c00b4-106">Reassociation is performed by calling the methods of the [**IFhReassociation**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="c00b4-107">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="c00b4-107">When to implement</span></span>

<span data-ttu-id="c00b4-108">La API del historial de archivos implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="c00b4-108">The File History API implements this class.</span></span> <span data-ttu-id="c00b4-109">Para crear una instancia de esta clase, use la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="c00b4-109">To create an instance of this class, use the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c00b4-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c00b4-110">Requirements</span></span>



| <span data-ttu-id="c00b4-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c00b4-111">Requirement</span></span> | <span data-ttu-id="c00b4-112">Value</span><span class="sxs-lookup"><span data-stu-id="c00b4-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c00b4-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c00b4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c00b4-114">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c00b4-114">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c00b4-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c00b4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c00b4-116">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c00b4-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c00b4-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c00b4-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c00b4-118"><dt>Fhcfg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c00b4-118"><dt>Fhcfg.h</dt></span></span> </dl>   |
| <span data-ttu-id="c00b4-119">IDL</span><span class="sxs-lookup"><span data-stu-id="c00b4-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c00b4-120"><dt>Fhcfg. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c00b4-120"><dt>Fhcfg.idl</dt></span></span> </dl> |



 

 
