---
title: Interfaz INapSoHProcessor (NapProtocol. h)
description: Los Sha usan para procesar el contenido de SoHResponses y de los SHV para procesar el contenido de SoHRequests.
ms.assetid: c2dd71ca-a4dd-44d2-81ab-b83e90599a2f
keywords:
- Interfaz INapSoHProcessor NAP
- Interfaz INapSoHProcessor NAP, descripción
topic_type:
- apiref
api_name:
- INapSoHProcessor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c43abf137bb267468deeb9d4bd47546275ba6c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078896"
---
# <a name="inapsohprocessor-interface"></a><span data-ttu-id="1891f-105">Interfaz INapSoHProcessor</span><span class="sxs-lookup"><span data-stu-id="1891f-105">INapSoHProcessor interface</span></span>

> [!Note]  
> <span data-ttu-id="1891f-106">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="1891f-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1891f-107">**INapSoHProcessor** proporciona métodos que los Sha usan para procesar el contenido de [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh) y SHV para procesar el contenido de **SoHRequests**.</span><span class="sxs-lookup"><span data-stu-id="1891f-107">The **INapSoHProcessor** provides methods that are used by SHAs to process the contents of [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh) and by SHVs to process the contents of **SoHRequests**.</span></span>

## <a name="members"></a><span data-ttu-id="1891f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1891f-108">Members</span></span>

<span data-ttu-id="1891f-109">La interfaz **INapSoHProcessor** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1891f-109">The **INapSoHProcessor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1891f-110">**INapSoHProcessor** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1891f-110">**INapSoHProcessor** also has these types of members:</span></span>

-   [<span data-ttu-id="1891f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="1891f-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1891f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="1891f-112">Methods</span></span>

<span data-ttu-id="1891f-113">La interfaz **INapSoHProcessor** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1891f-113">The **INapSoHProcessor** interface has these methods.</span></span>



| <span data-ttu-id="1891f-114">Método</span><span class="sxs-lookup"><span data-stu-id="1891f-114">Method</span></span>                                                                                           | <span data-ttu-id="1891f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="1891f-115">Description</span></span>                                                                           |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="1891f-116">**INapSoHProcessor::FindNextAttribute**</span><span class="sxs-lookup"><span data-stu-id="1891f-116">**INapSoHProcessor::FindNextAttribute**</span></span>](inapsohprocessor-findnextattribute-method.md)         | <span data-ttu-id="1891f-117">Busca el índice de ubicación del siguiente atributo de paquete SoH.</span><span class="sxs-lookup"><span data-stu-id="1891f-117">Finds the location index of the next SoH packet attribute.</span></span><br/>                 |
| [<span data-ttu-id="1891f-118">**INapSoHProcessor:: GetAttribute**</span><span class="sxs-lookup"><span data-stu-id="1891f-118">**INapSoHProcessor::GetAttribute**</span></span>](inapsohprocessor-getattribute-method.md)                   | <span data-ttu-id="1891f-119">Recupera el tipo y el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="1891f-119">Retrieves the attribute type and value.</span></span><br/>                                    |
| [<span data-ttu-id="1891f-120">**INapSoHProcessor::GetNumberOfAttributes**</span><span class="sxs-lookup"><span data-stu-id="1891f-120">**INapSoHProcessor::GetNumberOfAttributes**</span></span>](inapsohprocessor-getnumberofattributes-method.md) | <span data-ttu-id="1891f-121">Recupera el número de atributos contenidos en el SoH.</span><span class="sxs-lookup"><span data-stu-id="1891f-121">Retrieves the number of attributes contained in the SoH.</span></span><br/>                   |
| [<span data-ttu-id="1891f-122">**INapSoHProcessor:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="1891f-122">**INapSoHProcessor::Initialize**</span></span>](inapsohprocessor-initialize-method.md)                       | <span data-ttu-id="1891f-123">Inicializa el paquete de protocolo SoH y el sistema NAP para el procesamiento de contenido.</span><span class="sxs-lookup"><span data-stu-id="1891f-123">Initializes the SoH protocol packet and NAP System for content processing.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1891f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1891f-124">Requirements</span></span>



| <span data-ttu-id="1891f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1891f-125">Requirement</span></span> | <span data-ttu-id="1891f-126">Value</span><span class="sxs-lookup"><span data-stu-id="1891f-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1891f-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1891f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1891f-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1891f-128">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1891f-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1891f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1891f-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1891f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1891f-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1891f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1891f-132"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="1891f-132"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="1891f-133">IDL</span><span class="sxs-lookup"><span data-stu-id="1891f-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1891f-134"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1891f-134"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="1891f-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1891f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1891f-136"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1891f-136"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="1891f-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="1891f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1891f-138">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="1891f-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="1891f-139">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="1891f-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

