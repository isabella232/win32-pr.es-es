---
description: El método SWbemRefresher. Refresh actualiza todos los elementos contenidos en el objeto SWbemRefresher. Objeto SWbemRefresher.
ms.assetid: 85a4777a-4be7-44f2-b7a6-e18b5e57f7af
ms.tgt_platform: multiple
title: Método SWbemRefresher. Refresh (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Refresh
- ISWbemRefresher.Refresh
- ISWbemRefresher.Refresh
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d8b2522227041858770c7256d7d2520cc661948e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707553"
---
# <a name="swbemrefresherrefresh-method"></a><span data-ttu-id="e96e6-103">SWbemRefresher. Refresh (método)</span><span class="sxs-lookup"><span data-stu-id="e96e6-103">SWbemRefresher.Refresh method</span></span>

<span data-ttu-id="e96e6-104">El método **SWbemRefresher. Refresh** actualiza todos los elementos contenidos en el objeto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="e96e6-104">The **SWbemRefresher.Refresh** method updates all the items that are contained in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="e96e6-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e96e6-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e96e6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e96e6-106">Syntax</span></span>


```VB
SWbemRefresher.Refresh( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e96e6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e96e6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e96e6-108">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="e96e6-108">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e96e6-109">Las marcas se deben establecer en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="e96e6-109">Flags must be set to 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e96e6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e96e6-110">Return value</span></span>

<span data-ttu-id="e96e6-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e96e6-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e96e6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e96e6-112">Requirements</span></span>



| <span data-ttu-id="e96e6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e96e6-113">Requirement</span></span> | <span data-ttu-id="e96e6-114">Value</span><span class="sxs-lookup"><span data-stu-id="e96e6-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e96e6-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e96e6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e96e6-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e96e6-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e96e6-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e96e6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e96e6-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e96e6-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e96e6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e96e6-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e96e6-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e96e6-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e96e6-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e96e6-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="e96e6-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e96e6-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e96e6-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e96e6-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e96e6-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e96e6-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e96e6-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="e96e6-125">CLSID</span></span><br/>                    | <span data-ttu-id="e96e6-126">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="e96e6-126">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="e96e6-127">IID</span><span class="sxs-lookup"><span data-stu-id="e96e6-127">IID</span></span><br/>                      | <span data-ttu-id="e96e6-128">\_ISWBEMREFRESHER IID</span><span class="sxs-lookup"><span data-stu-id="e96e6-128">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="e96e6-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e96e6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e96e6-130">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="e96e6-130">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




