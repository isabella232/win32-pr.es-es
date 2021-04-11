---
description: Se produce cuando el usuario ha generado el lápiz óptico desde la superficie del digitalizador de Tablet PC.
ms.assetid: 34dc7e6b-101a-4edd-8c3c-9aafb85cf58b
title: 'ITabletEventSink:: CursorUp (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorUp
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5e163fd01933ad0fc1a11429e77b37163655f39b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279174"
---
# <a name="itableteventsinkcursorup-method"></a><span data-ttu-id="4019d-103">ITabletEventSink:: CursorUp (método)</span><span class="sxs-lookup"><span data-stu-id="4019d-103">ITabletEventSink::CursorUp method</span></span>

<span data-ttu-id="4019d-104">Se produce cuando el usuario ha generado el lápiz óptico desde la superficie del digitalizador de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="4019d-104">Occurs when the user has raised the stylus from the tablet digitizer surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="4019d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4019d-105">Syntax</span></span>


```C++
HRESULT CursorUp(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a><span data-ttu-id="4019d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4019d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4019d-107">*TCID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4019d-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4019d-108">El identificador de la tableta.</span><span class="sxs-lookup"><span data-stu-id="4019d-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="4019d-109">*CID* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="4019d-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4019d-110">Identificador del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="4019d-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="4019d-111">*nSerialNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4019d-111">*nSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4019d-112">Número de serie del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="4019d-112">The serial number of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="4019d-113">*cbPkt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4019d-113">*cbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4019d-114">El número de bytes de un paquete de datos del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="4019d-114">The number of bytes in a stylus data packet.</span></span>

</dd> <dt>

<span data-ttu-id="4019d-115">*pbPkt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4019d-115">*pbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4019d-116">Los datos del lápiz óptico que indican la ubicación en la que se ha levantado el lápiz óptico de la tableta.</span><span class="sxs-lookup"><span data-stu-id="4019d-116">The stylus data indicating the location where the stylus was lifted from the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4019d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4019d-117">Return value</span></span>

<span data-ttu-id="4019d-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4019d-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4019d-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4019d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4019d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4019d-120">Requirements</span></span>



| <span data-ttu-id="4019d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4019d-121">Requirement</span></span> | <span data-ttu-id="4019d-122">Value</span><span class="sxs-lookup"><span data-stu-id="4019d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4019d-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4019d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4019d-124">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4019d-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4019d-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4019d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4019d-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4019d-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4019d-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4019d-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="4019d-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4019d-128"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4019d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="4019d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4019d-130">**Interfaz ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="4019d-130">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




