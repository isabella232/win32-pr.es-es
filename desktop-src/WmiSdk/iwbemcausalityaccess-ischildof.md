---
description: El método IsChildOf determina si una solicitud es un elemento secundario de una solicitud especificada (pId).
ms.assetid: 7be52496-7dcf-41c0-853a-859810a57d21
ms.tgt_platform: multiple
title: 'IWbemCausalityAccess:: IsChildOf (método) (Wbemint. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.IsChildOf
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 6deec7521ceb58a76db3dbf8064ccc444019cb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277925"
---
# <a name="iwbemcausalityaccessischildof-method"></a><span data-ttu-id="37c04-103">IWbemCausalityAccess:: IsChildOf (método)</span><span class="sxs-lookup"><span data-stu-id="37c04-103">IWbemCausalityAccess::IsChildOf method</span></span>

<span data-ttu-id="37c04-104">El método **IsChildOf** determina si una solicitud es un elemento secundario de una solicitud especificada (pId).</span><span class="sxs-lookup"><span data-stu-id="37c04-104">The **IsChildOf** method determines if a request is a child of a specified request (pId).</span></span> <span data-ttu-id="37c04-105">Una solicitud primaria puede tener varias solicitudes secundarias.</span><span class="sxs-lookup"><span data-stu-id="37c04-105">A parent request can have multiple child requests.</span></span> <span data-ttu-id="37c04-106">Cada solicitud se identifica mediante un identificador único global (GUID) y puede tener una solicitud primaria o puede ser una solicitud Top.</span><span class="sxs-lookup"><span data-stu-id="37c04-106">Each request is identified by a Globally Unique Identifier (GUID) and can have a parent request or can be a top request.</span></span> <span data-ttu-id="37c04-107">Un GUID es un número único de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="37c04-107">A GUID is a unique 128-bit number.</span></span>

## <a name="syntax"></a><span data-ttu-id="37c04-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37c04-108">Syntax</span></span>


```C++
HRESULT IsChildOf(
  [in] REQUESTID pId
);
```



## <a name="parameters"></a><span data-ttu-id="37c04-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37c04-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37c04-110">*pId* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="37c04-110">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37c04-111">Valor GUID que identifica de forma única una solicitud.</span><span class="sxs-lookup"><span data-stu-id="37c04-111">The GUID value that uniquely identifies a request.</span></span> <span data-ttu-id="37c04-112">Por ejemplo, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span><span class="sxs-lookup"><span data-stu-id="37c04-112">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37c04-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37c04-113">Return value</span></span>

<span data-ttu-id="37c04-114">Devuelve correcto si la solicitud especificada es un elemento secundario de la solicitud que llama al método **IsChildOf** .</span><span class="sxs-lookup"><span data-stu-id="37c04-114">Returns successful if the specified request is a child of the request calling the **IsChildOf** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="37c04-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37c04-115">Requirements</span></span>



| <span data-ttu-id="37c04-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="37c04-116">Requirement</span></span> | <span data-ttu-id="37c04-117">Value</span><span class="sxs-lookup"><span data-stu-id="37c04-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37c04-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37c04-118">Minimum supported client</span></span><br/> | <span data-ttu-id="37c04-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37c04-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="37c04-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37c04-120">Minimum supported server</span></span><br/> | <span data-ttu-id="37c04-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37c04-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="37c04-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37c04-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="37c04-123"><dt>Wbemint. h</dt></span><span class="sxs-lookup"><span data-stu-id="37c04-123"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="37c04-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="37c04-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37c04-125"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37c04-125"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37c04-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="37c04-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37c04-127">**IWbemCausalityAccess**</span><span class="sxs-lookup"><span data-stu-id="37c04-127">**IWbemCausalityAccess**</span></span>](iwbemcausalityaccess.md)
</dt> </dl>

 

 




