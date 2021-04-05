---
description: Devuelve el número de elementos almacenados por este enumerador.
ms.assetid: d374ec81-0bd5-4b5d-8002-e3b53476421a
title: 'IEnumWiaItem2:: GetCount (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.GetCount
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 23c067b8e4da93d678f641890a85e2535b3ca50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082229"
---
# <a name="ienumwiaitem2getcount-method"></a><span data-ttu-id="9fbec-103">IEnumWiaItem2:: GetCount (método)</span><span class="sxs-lookup"><span data-stu-id="9fbec-103">IEnumWiaItem2::GetCount method</span></span>

<span data-ttu-id="9fbec-104">Devuelve el número de elementos almacenados por este enumerador.</span><span class="sxs-lookup"><span data-stu-id="9fbec-104">Returns the number of elements stored by this enumerator.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fbec-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fbec-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *cElt
);
```



## <a name="parameters"></a><span data-ttu-id="9fbec-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9fbec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fbec-107">*cElt* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9fbec-107">*cElt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fbec-108">Tipo: \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="9fbec-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="9fbec-109">Recibe un puntero a un _ *ULong*\* que recibe el número de elementos de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="9fbec-109">Receives a pointer to a _ *ULONG*\* that receives the number of elements in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fbec-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9fbec-110">Return value</span></span>

<span data-ttu-id="9fbec-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9fbec-111">Type: **HRESULT**</span></span>

<span data-ttu-id="9fbec-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9fbec-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9fbec-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9fbec-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fbec-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fbec-114">Requirements</span></span>



| <span data-ttu-id="9fbec-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fbec-115">Requirement</span></span> | <span data-ttu-id="9fbec-116">Value</span><span class="sxs-lookup"><span data-stu-id="9fbec-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9fbec-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fbec-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9fbec-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9fbec-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9fbec-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fbec-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9fbec-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9fbec-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9fbec-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fbec-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fbec-122"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fbec-122"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="9fbec-123">IDL</span><span class="sxs-lookup"><span data-stu-id="9fbec-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9fbec-124"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9fbec-124"><dt>Wia.idl</dt></span></span> </dl> |



 

 




