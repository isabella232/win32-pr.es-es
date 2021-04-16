---
description: Recupera una matriz que contiene los datos de propiedad del paquete para el trazo especificado.
ms.assetid: 02db48b3-edc3-4ecb-8103-79312194937a
title: 'IContextNode:: GetStrokePacketDataById (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDataById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be2e9326e2ecb20afc652776c006c8ae989c7396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696538"
---
# <a name="icontextnodegetstrokepacketdatabyid-method"></a><span data-ttu-id="c7342-103">IContextNode:: GetStrokePacketDataById (método)</span><span class="sxs-lookup"><span data-stu-id="c7342-103">IContextNode::GetStrokePacketDataById method</span></span>

<span data-ttu-id="c7342-104">Recupera una matriz que contiene los datos de propiedad del paquete para el trazo especificado.</span><span class="sxs-lookup"><span data-stu-id="c7342-104">Retrieves an array containing the packet property data for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7342-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7342-105">Syntax</span></span>


```C++
HRESULT GetStrokePacketDataById(
  [in]      LONG  strokeId,
  [in, out] ULONG *pStrokePacketDataCount,
  [out]     LONG  **pplStrokePacketData
);
```



## <a name="parameters"></a><span data-ttu-id="c7342-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7342-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7342-107">*strokeId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c7342-107">*strokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7342-108">Identificador del trazo.</span><span class="sxs-lookup"><span data-stu-id="c7342-108">The identifier for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="c7342-109">*pStrokePacketDataCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c7342-109">*pStrokePacketDataCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7342-110">La longitud de la matriz de datos de paquetes.</span><span class="sxs-lookup"><span data-stu-id="c7342-110">The length of the packet data array.</span></span>

</dd> <dt>

<span data-ttu-id="c7342-111">*pplStrokePacketData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c7342-111">*pplStrokePacketData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7342-112">Puntero a los datos del paquete del trazo.</span><span class="sxs-lookup"><span data-stu-id="c7342-112">A pointer to the packet data for the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7342-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7342-113">Return value</span></span>

<span data-ttu-id="c7342-114">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c7342-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c7342-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7342-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c7342-116">Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *pplStrokePacketData* cuando ya no necesite la información.</span><span class="sxs-lookup"><span data-stu-id="c7342-116">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokePacketData* when you no longer need the information.</span></span>

 

<span data-ttu-id="c7342-117">*plStrokePacketData* contiene datos de paquetes para todos los puntos del trazo.</span><span class="sxs-lookup"><span data-stu-id="c7342-117">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="c7342-118">Para obtener los tipos de datos de paquete incluidos para cada punto del trazo, use [**IContextNode:: GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md).</span><span class="sxs-lookup"><span data-stu-id="c7342-118">To get the types of packet data included for each point in the stroke, use [**IContextNode::GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7342-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7342-119">Requirements</span></span>



| <span data-ttu-id="c7342-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7342-120">Requirement</span></span> | <span data-ttu-id="c7342-121">Value</span><span class="sxs-lookup"><span data-stu-id="c7342-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7342-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7342-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c7342-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c7342-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c7342-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7342-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c7342-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c7342-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c7342-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7342-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7342-127"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c7342-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c7342-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7342-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7342-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7342-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c7342-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7342-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7342-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="c7342-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c7342-132">**IContextNode::GetStrokePacketDescriptionById**</span><span class="sxs-lookup"><span data-stu-id="c7342-132">**IContextNode::GetStrokePacketDescriptionById**</span></span>](icontextnode-getstrokepacketdescriptionbyid.md)
</dt> <dt>

[<span data-ttu-id="c7342-133">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="c7342-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

