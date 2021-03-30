---
description: Se produce cuando la punta del lápiz se pone en contacto con la superficie de la tableta de la digitalización.
ms.assetid: 7f4a441d-00d2-4120-8a8d-d3496cdc7e58
title: 'ITabletEventSink:: CursorDown (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorDown
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 1f0ffbe8c300e3c227cd59d8ff391b8990873c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814430"
---
# <a name="itableteventsinkcursordown-method"></a><span data-ttu-id="0128b-103">ITabletEventSink:: CursorDown (método)</span><span class="sxs-lookup"><span data-stu-id="0128b-103">ITabletEventSink::CursorDown method</span></span>

<span data-ttu-id="0128b-104">Se produce cuando la punta del lápiz se pone en contacto con la superficie de la tableta de la digitalización.</span><span class="sxs-lookup"><span data-stu-id="0128b-104">Occurs when the stylus tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0128b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0128b-105">Syntax</span></span>


```C++
HRESULT CursorDown(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a><span data-ttu-id="0128b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0128b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0128b-107">*TCID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0128b-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0128b-108">El identificador de la tableta.</span><span class="sxs-lookup"><span data-stu-id="0128b-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="0128b-109">*CID* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="0128b-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0128b-110">Identificador del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="0128b-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="0128b-111">*nSerialNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0128b-111">*nSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0128b-112">Número de serie del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="0128b-112">The serial number of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="0128b-113">*cbPkt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0128b-113">*cbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0128b-114">El número de bytes de un paquete de datos del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="0128b-114">The number of bytes in a stylus data packet.</span></span>

</dd> <dt>

<span data-ttu-id="0128b-115">*pbPkt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0128b-115">*pbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0128b-116">Datos del lápiz óptico que indican la ubicación donde el lápiz toca la tableta.</span><span class="sxs-lookup"><span data-stu-id="0128b-116">The stylus data indicating the location where the stylus touched the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0128b-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0128b-117">Return value</span></span>

<span data-ttu-id="0128b-118">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0128b-118">This method can return one of these values.</span></span>



| <span data-ttu-id="0128b-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0128b-119">Return code</span></span>                                                                            | <span data-ttu-id="0128b-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="0128b-120">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="0128b-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0128b-121"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="0128b-122">Correcto.</span><span class="sxs-lookup"><span data-stu-id="0128b-122">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="0128b-123"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="0128b-123"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="0128b-124">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="0128b-124">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0128b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0128b-125">Requirements</span></span>



| <span data-ttu-id="0128b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0128b-126">Requirement</span></span> | <span data-ttu-id="0128b-127">Value</span><span class="sxs-lookup"><span data-stu-id="0128b-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0128b-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0128b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0128b-129">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0128b-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0128b-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0128b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0128b-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0128b-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0128b-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0128b-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="0128b-133"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0128b-133"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0128b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="0128b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0128b-135">**Interfaz ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="0128b-135">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




