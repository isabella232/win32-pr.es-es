---
title: Mensaje de CQPM_PERSIST (Cmnquery. h)
description: Se envía a la función de devolución de llamada CQPageProc de una página de extensión de formulario de consulta para permitir que la página lea o escriba datos de consulta de la memoria persistente.
ms.assetid: f01586dd-4ed3-45af-9e25-a596a693313d
ms.tgt_platform: multiple
keywords:
- CQPM_PERSIST Active Directory de mensaje
topic_type:
- apiref
api_name:
- CQPM_PERSIST
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70aaaae3b4fcc6788a16d59477d5f8158b43b892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079315"
---
# <a name="cqpm_persist-message"></a><span data-ttu-id="1f4e2-104">CQPM \_ mensaje persistente</span><span class="sxs-lookup"><span data-stu-id="1f4e2-104">CQPM\_PERSIST message</span></span>

<span data-ttu-id="1f4e2-105">El mensaje **CQPM \_ Persist** se envía a la función de devolución de llamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de una página de extensión de formulario de consulta para permitir que la página lea o escriba datos de consulta de la memoria persistente.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-105">The **CQPM\_PERSIST** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to allow the page to read or write query data from persistent memory.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f4e2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f4e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f4e2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f4e2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f4e2-108">Contiene un valor distinto de cero para leer los datos de la consulta o cero para escribir los datos de la consulta.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-108">Contains nonzero to read the query data or zero to write the query data.</span></span>

</dd> <dt>

<span data-ttu-id="1f4e2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f4e2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f4e2-110">Puntero a una interfaz [**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) en la que se deben leer o escribir los datos de la consulta.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-110">Pointer to an [**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) interface that the query data should be read from or written to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f4e2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f4e2-111">Return value</span></span>

<span data-ttu-id="1f4e2-112">Devuelve **S \_ correcto** si es correcto o un código de error **HRESULT** estándar en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-112">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f4e2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f4e2-113">Requirements</span></span>



| <span data-ttu-id="1f4e2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f4e2-114">Requirement</span></span> | <span data-ttu-id="1f4e2-115">Value</span><span class="sxs-lookup"><span data-stu-id="1f4e2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f4e2-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f4e2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1f4e2-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f4e2-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="1f4e2-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f4e2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1f4e2-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f4e2-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="1f4e2-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f4e2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f4e2-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f4e2-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f4e2-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f4e2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f4e2-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="1f4e2-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="1f4e2-124">**IPersistQuery**</span><span class="sxs-lookup"><span data-stu-id="1f4e2-124">**IPersistQuery**</span></span>](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery)
</dt> </dl>

 

