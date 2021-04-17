---
description: Recupera una matriz que contiene los identificadores de propiedad de paquete para el trazo especificado.
ms.assetid: 169e3ce3-fb81-4ed6-b380-ef0d12444ba7
title: 'IContextNode:: GetStrokePacketDescriptionById (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDescriptionById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e1633cd2097e256d389a2c86e450bf221f0546f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696537"
---
# <a name="icontextnodegetstrokepacketdescriptionbyid-method"></a><span data-ttu-id="ec0ab-103">IContextNode:: GetStrokePacketDescriptionById (método)</span><span class="sxs-lookup"><span data-stu-id="ec0ab-103">IContextNode::GetStrokePacketDescriptionById method</span></span>

<span data-ttu-id="ec0ab-104">Recupera una matriz que contiene los identificadores de propiedad de paquete para el trazo especificado.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-104">Retrieves an array containing the packet property identifiers for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec0ab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec0ab-105">Syntax</span></span>


```C++
HRESULT GetStrokePacketDescriptionById(
  [in]      LONG  lStrokeId,
  [in, out] ULONG *pulStrokePacketDescriptionCount,
  [out]     GUID  **ppStrokePacketDescriptionGuids
);
```



## <a name="parameters"></a><span data-ttu-id="ec0ab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec0ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec0ab-107">*lStrokeId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ec0ab-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec0ab-108">Identificador del trazo.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-108">The identifier for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="ec0ab-109">*pulStrokePacketDescriptionCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ec0ab-109">*pulStrokePacketDescriptionCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec0ab-110">El número de propiedades de paquete en cada paquete.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-110">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="ec0ab-111">*ppStrokePacketDescriptionGuids* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ec0ab-111">*ppStrokePacketDescriptionGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec0ab-112">Una matriz que contiene los identificadores de propiedad de paquete.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-112">An array containing the packet property identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec0ab-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec0ab-113">Return value</span></span>

<span data-ttu-id="ec0ab-114">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ec0ab-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ec0ab-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec0ab-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ec0ab-116">Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppStrokePacketDescriptionGuids* cuando ya no necesite la información.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-116">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppStrokePacketDescriptionGuids* when you no longer need the information.</span></span>

 

<span data-ttu-id="ec0ab-117">\**ppStrokePacketDescriptionGuids* contiene los identificadores únicos globales (GUID) que describen los tipos de datos de paquete incluidos para cada punto del trazo.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-117">\**ppStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="ec0ab-118">Para obtener una lista completa de las propiedades de paquete disponibles, consulte [constantes de PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ec0ab-118">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec0ab-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec0ab-119">Requirements</span></span>



| <span data-ttu-id="ec0ab-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec0ab-120">Requirement</span></span> | <span data-ttu-id="ec0ab-121">Value</span><span class="sxs-lookup"><span data-stu-id="ec0ab-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec0ab-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec0ab-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ec0ab-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ec0ab-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ec0ab-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec0ab-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ec0ab-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ec0ab-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ec0ab-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec0ab-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec0ab-127"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ec0ab-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ec0ab-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ec0ab-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec0ab-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec0ab-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ec0ab-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec0ab-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec0ab-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="ec0ab-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ec0ab-132">**IContextNode::GetStrokePacketDataById**</span><span class="sxs-lookup"><span data-stu-id="ec0ab-132">**IContextNode::GetStrokePacketDataById**</span></span>](icontextnode-getstrokepacketdatabyid.md)
</dt> <dt>

[<span data-ttu-id="ec0ab-133">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="ec0ab-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

