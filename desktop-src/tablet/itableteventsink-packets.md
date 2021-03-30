---
description: Se produce cuando el lápiz óptico se mueve en el digitalizador.
ms.assetid: 67d55dbc-6119-45d9-8016-a2a59f5f04ea
title: ITabletEventSink::P método ackets
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.Packets
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fb671b0556cf121e28ae81c5dcfa804208e00006
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002391"
---
# <a name="itableteventsinkpackets-method"></a><span data-ttu-id="bdd34-103">ITabletEventSink::P método ackets</span><span class="sxs-lookup"><span data-stu-id="bdd34-103">ITabletEventSink::Packets method</span></span>

<span data-ttu-id="bdd34-104">Se produce cuando el lápiz óptico se mueve en el digitalizador.</span><span class="sxs-lookup"><span data-stu-id="bdd34-104">Occurs when the stylus is moving on the digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdd34-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bdd34-105">Syntax</span></span>


```C++
HRESULT Packets(
  [in] TABLET_CONTEXT_ID tcid,
  [in] ULONG             cPkts,
  [in] ULONG             cbPkts,
  [in] BYTE              *pbPkts,
  [in] ULONG             *pnSerialNumbers,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="bdd34-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bdd34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdd34-107">*TCID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bdd34-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdd34-108">El identificador de la tableta.</span><span class="sxs-lookup"><span data-stu-id="bdd34-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="bdd34-109">*cPkts* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bdd34-109">*cPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdd34-110">El número de paquetes.</span><span class="sxs-lookup"><span data-stu-id="bdd34-110">The number of packets.</span></span>

</dd> <dt>

<span data-ttu-id="bdd34-111">*cbPkts* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bdd34-111">*cbPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdd34-112">Tamaño del búfer de paquetes</span><span class="sxs-lookup"><span data-stu-id="bdd34-112">The size of packet buffer</span></span>

</dd> <dt>

<span data-ttu-id="bdd34-113">*pbPkts* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bdd34-113">*pbPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdd34-114">Búfer de paquetes.</span><span class="sxs-lookup"><span data-stu-id="bdd34-114">The packet buffer.</span></span>

</dd> <dt>

<span data-ttu-id="bdd34-115">*pnSerialNumbers* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bdd34-115">*pnSerialNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdd34-116">Matriz de números de serie.</span><span class="sxs-lookup"><span data-stu-id="bdd34-116">The serial number array.</span></span>

</dd> <dt>

<span data-ttu-id="bdd34-117">*Cid*</span><span class="sxs-lookup"><span data-stu-id="bdd34-117">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="bdd34-118">Identificador del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="bdd34-118">The identifier of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdd34-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bdd34-119">Return value</span></span>

<span data-ttu-id="bdd34-120">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="bdd34-120">This method can return one of these values.</span></span>



| <span data-ttu-id="bdd34-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bdd34-121">Return code</span></span>                                                                            | <span data-ttu-id="bdd34-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="bdd34-122">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="bdd34-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="bdd34-123"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="bdd34-124">Correcto.</span><span class="sxs-lookup"><span data-stu-id="bdd34-124">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="bdd34-125"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="bdd34-125"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="bdd34-126">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="bdd34-126">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bdd34-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdd34-127">Requirements</span></span>



| <span data-ttu-id="bdd34-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdd34-128">Requirement</span></span> | <span data-ttu-id="bdd34-129">Value</span><span class="sxs-lookup"><span data-stu-id="bdd34-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdd34-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bdd34-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bdd34-131">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bdd34-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bdd34-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bdd34-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bdd34-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bdd34-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="bdd34-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bdd34-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="bdd34-135"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bdd34-135"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdd34-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="bdd34-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdd34-137">**Interfaz ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="bdd34-137">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




