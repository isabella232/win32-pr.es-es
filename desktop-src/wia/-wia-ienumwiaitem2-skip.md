---
description: Omite el número especificado de elementos durante una enumeración de objetos IWiaItem2 disponibles.
ms.assetid: 7a5e9e1c-1e6e-4de0-9499-bf89e35c19aa
title: 'IEnumWiaItem2:: Skip (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Skip
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7618aad923136a9a32d8b7fb935050fefe07bff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001306"
---
# <a name="ienumwiaitem2skip-method"></a><span data-ttu-id="63220-103">IEnumWiaItem2:: Skip (método)</span><span class="sxs-lookup"><span data-stu-id="63220-103">IEnumWiaItem2::Skip method</span></span>

<span data-ttu-id="63220-104">Omite el número especificado de elementos durante una enumeración de objetos [**IWiaItem2**](-wia-iwiaitem2.md) disponibles.</span><span class="sxs-lookup"><span data-stu-id="63220-104">Skips the specified number of items during an enumeration of available [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="63220-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63220-105">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG cElt
);
```



## <a name="parameters"></a><span data-ttu-id="63220-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63220-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63220-107">*cElt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63220-107">*cElt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63220-108">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="63220-108">Type: **ULONG**</span></span>

<span data-ttu-id="63220-109">Especifica el número de elementos que se van a omitir.</span><span class="sxs-lookup"><span data-stu-id="63220-109">Specifies the number of items to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63220-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63220-110">Return value</span></span>

<span data-ttu-id="63220-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="63220-111">Type: **HRESULT**</span></span>

<span data-ttu-id="63220-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="63220-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="63220-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="63220-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="63220-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63220-114">Requirements</span></span>



| <span data-ttu-id="63220-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="63220-115">Requirement</span></span> | <span data-ttu-id="63220-116">Value</span><span class="sxs-lookup"><span data-stu-id="63220-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="63220-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63220-117">Minimum supported client</span></span><br/> | <span data-ttu-id="63220-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="63220-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="63220-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63220-119">Minimum supported server</span></span><br/> | <span data-ttu-id="63220-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="63220-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="63220-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63220-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="63220-122"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="63220-122"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="63220-123">IDL</span><span class="sxs-lookup"><span data-stu-id="63220-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="63220-124"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="63220-124"><dt>Wia.idl</dt></span></span> </dl> |



 

 




