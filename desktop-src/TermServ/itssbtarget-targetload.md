---
title: Propiedad TargetLoad de ITsSbTarget
description: Recupera la carga relativa de un destino.
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad TargetLoad
- Propiedad TargetLoad Servicios de Escritorio remoto, interfaz ITsSbTarget
- Servicios de Escritorio remoto de la interfaz ITsSbTarget, propiedad TargetLoad
- Propiedad TargetLoad Servicios de Escritorio remoto, interfaz ITsSbTargetEx
- Servicios de Escritorio remoto de la interfaz ITsSbTargetEx, propiedad TargetLoad
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetLoad
- ITsSbTarget.get_TargetLoad
- ITsSbTargetEx.TargetLoad
- ITsSbTargetEx.get_TargetLoad
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddfc9be9805406ab76b166e2a34bc47a7f5e9ab5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784120"
---
# <a name="itssbtargettargetload-property"></a><span data-ttu-id="fc32d-108">ITsSbTarget:: TargetLoad (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fc32d-108">ITsSbTarget::TargetLoad property</span></span>

<span data-ttu-id="fc32d-109">Recupera la carga relativa de un destino.</span><span class="sxs-lookup"><span data-stu-id="fc32d-109">Retrieves the relative load on a target.</span></span> <span data-ttu-id="fc32d-110">Este valor se basa en el número de sesiones existentes y pendientes.</span><span class="sxs-lookup"><span data-stu-id="fc32d-110">This value is based on the number of existing and pending sessions.</span></span> <span data-ttu-id="fc32d-111">De forma predeterminada, una sesión pendiente tiene el mismo valor que una sesión existente.</span><span class="sxs-lookup"><span data-stu-id="fc32d-111">By default a pending session has the same value as an existing session.</span></span>

<span data-ttu-id="fc32d-112">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fc32d-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc32d-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc32d-113">Syntax</span></span>


```C++
HRESULT get_TargetLoad(
  [out, retval] DWORD *pTargetLoad
);
```



## <a name="property-value"></a><span data-ttu-id="fc32d-114">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fc32d-114">Property value</span></span>

<span data-ttu-id="fc32d-115">Número que representa la carga relativa de un destino.</span><span class="sxs-lookup"><span data-stu-id="fc32d-115">A number representing the relative load on a target.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc32d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc32d-116">Remarks</span></span>

<span data-ttu-id="fc32d-117">El peso de una sesión pendiente con respecto a una sesión activa se puede cambiar estableciendo el valor del parámetro *lb \_ ConnectionEstablishmentPenalty* para el agente de conexión.</span><span class="sxs-lookup"><span data-stu-id="fc32d-117">The weight of a pending session relative to an active session can be changed by setting the value of the *LB\_ConnectionEstablishmentPenalty* parameter for the Connection Broker.</span></span> <span data-ttu-id="fc32d-118">Este parámetro se encuentra en la clave del registro **HKLM \\ System \\ CurrentControlSet \\ Services \\ Tssdis \\ Parameters** .</span><span class="sxs-lookup"><span data-stu-id="fc32d-118">This parameter is located under the **HKLM\\System\\CurrentControlSet\\Services\\Tssdis\\Parameters** registry key.</span></span> <span data-ttu-id="fc32d-119">El valor predeterminado de 1 especifica que las sesiones pendientes tienen el mismo peso que las sesiones activas.</span><span class="sxs-lookup"><span data-stu-id="fc32d-119">The default value of 1 specifies that pending sessions have the same weight as active sessions.</span></span>

<span data-ttu-id="fc32d-120">Esta propiedad está disponible en Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) instalado en la interfaz [**ITsSbTargetEx**](itssbtargetex.md) .</span><span class="sxs-lookup"><span data-stu-id="fc32d-120">This property is available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbTargetEx**](itssbtargetex.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc32d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc32d-121">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc32d-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc32d-122">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="fc32d-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fc32d-123">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc32d-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc32d-124">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="fc32d-125">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fc32d-125">Windows Server 2016</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc32d-126">IDL</span><span class="sxs-lookup"><span data-stu-id="fc32d-126">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="fc32d-127"><dt>Sbtsv. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="fc32d-127"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc32d-128">IID</span><span class="sxs-lookup"><span data-stu-id="fc32d-128">IID</span></span><br/></td>
<td><span data-ttu-id="fc32d-129">IID_ITsSbTarget se define como:</span><span class="sxs-lookup"><span data-stu-id="fc32d-129">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="fc32d-130">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="fc32d-130">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="fc32d-131">e85e10ea-db0b-4752-B456-5fd5840901c0 en Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fc32d-131">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="fc32d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc32d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc32d-133">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="fc32d-133">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="fc32d-134">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="fc32d-134">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





