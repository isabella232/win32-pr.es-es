---
title: Propiedad IpAddresses de ITsSbTarget
description: Recupera o especifica las direcciones IP externas del destino.
ms.assetid: 938a753c-d541-4772-b41b-817324488685
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad TargetExternalIpAddresses
- Propiedad TargetExternalIpAddresses Servicios de Escritorio remoto, interfaz ITsSbTarget
- Propiedad TargetExternalIpAddresses Servicios de Escritorio remoto, interfaz ITsSbTarget
- Servicios de Escritorio remoto de la propiedad IpAddresses
- Propiedad IpAddresses Servicios de Escritorio remoto, interfaz ITsSbTarget
- Servicios de Escritorio remoto de la interfaz ITsSbTarget, propiedad IpAddresses
- Propiedad IpAddresses Servicios de Escritorio remoto, interfaz ITsSbTargetEx
- Servicios de Escritorio remoto de la interfaz ITsSbTargetEx, propiedad IpAddresses
topic_type:
- apiref
api_name:
- ITsSbTarget.IpAddresses
- ITsSbTarget.get_IpAddresses
- ITsSbTarget.put_IpAddresses
- ITsSbTargetEx.IpAddresses
- ITsSbTargetEx.get_IpAddresses
- ITsSbTargetEx.put_IpAddresses
- TargetExternalIpAddresses
- ITsSbTarget.TargetExternalIpAddresses
- ITsSbTarget get_TargetExternalIpAddresses
- ITsSbTarget put_TargetExternalIpAddresses
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b3902840b24bc49ae3bda0510c8355afb67810
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419518"
---
# <a name="itssbtargetipaddresses-property"></a><span data-ttu-id="e0a84-111">ITsSbTarget:: IpAddresses (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e0a84-111">ITsSbTarget::IpAddresses property</span></span>

<span data-ttu-id="e0a84-112">Recupera o especifica las direcciones IP externas del destino.</span><span class="sxs-lookup"><span data-stu-id="e0a84-112">Retrieves or specifies the external IP addresses of the target.</span></span>

<span data-ttu-id="e0a84-113">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e0a84-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0a84-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0a84-114">Syntax</span></span>


```C++
HRESULT put_IpAddresses(
  [in, size_is(numAddresses)]   TSSD_ConnectionPoint *sockaddr,
  [in]                          DWORD                numAddresses
);

HRESULT get_IpAddresses(
  [out, size_is(*numAddresses)] TSSD_ConnectionPoint *sockaddr,
  [in, out]                     DWORD                *numAddresses
);
```



## <a name="property-value"></a><span data-ttu-id="e0a84-115">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e0a84-115">Property value</span></span>

<span data-ttu-id="e0a84-116">Un puntero a una matriz de [**estructuras \_ TSSD**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) de un conjunto de discos que reciben las direcciones IP externas del destino.</span><span class="sxs-lookup"><span data-stu-id="e0a84-116">A pointer to an array of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures that receive the external IP addresses of the target.</span></span>

<span data-ttu-id="e0a84-117">Un puntero a una variable **DWORD** que contiene el número de direcciones IP externas en el parámetro *sockaddr* .</span><span class="sxs-lookup"><span data-stu-id="e0a84-117">A pointer to a **DWORD** variable that contains the number of external IP addresses in the *sockaddr* parameter.</span></span> <span data-ttu-id="e0a84-118">Si el número de direcciones es desconocido, pase *sockaddr* como **null**.</span><span class="sxs-lookup"><span data-stu-id="e0a84-118">If the number of addresses is unknown, pass *sockaddr* as **NULL**.</span></span> <span data-ttu-id="e0a84-119">El método devolverá el número de estructuras [**TSSD \_**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) de un valor necesario para asignar en la matriz señalada por el parámetro *sockaddr* .</span><span class="sxs-lookup"><span data-stu-id="e0a84-119">The method will return the number of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures necessary to allocate in the array pointed to by the *sockaddr* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0a84-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0a84-120">Remarks</span></span>

<span data-ttu-id="e0a84-121">Esta propiedad se conocía anteriormente como **TargetExternalIpAddresses** en Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="e0a84-121">This property was formerly known as **TargetExternalIpAddresses** in Windows Server 2008 R2.</span></span>

<span data-ttu-id="e0a84-122">Si el número de direcciones IP externas es desconocido, puede llamar a este método con *sockaddr* establecido en **null**.</span><span class="sxs-lookup"><span data-stu-id="e0a84-122">If the number of external IP addresses is unknown, you can call this method with *sockaddr* set to **NULL**.</span></span> <span data-ttu-id="e0a84-123">Después, el método devolverá, en el parámetro *numAddresses* , el número de estructuras de [**TSSD \_**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) de un valor necesario para recibir todas las direcciones IP externas.</span><span class="sxs-lookup"><span data-stu-id="e0a84-123">The method will then return, in the *numAddresses* parameter, the number of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures necessary to receive all the external IP addresses.</span></span> <span data-ttu-id="e0a84-124">Asigne la matriz para *sockaddr* basándose en este número y, a continuación, llame de nuevo al método, estableciendo *sockaddr* en la matriz recién asignada y *numAddresses* en el número devuelto por la primera llamada.</span><span class="sxs-lookup"><span data-stu-id="e0a84-124">Allocate the array for *sockaddr* based on this number, and then call the method again, setting *sockaddr* to the newly allocated array and *numAddresses* to the number returned by the first call.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0a84-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0a84-125">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0a84-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0a84-126">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="e0a84-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e0a84-127">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0a84-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0a84-128">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="e0a84-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e0a84-129">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0a84-130">IDL</span><span class="sxs-lookup"><span data-stu-id="e0a84-130">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="e0a84-131"><dt>Sbtsv. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="e0a84-131"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0a84-132">IID</span><span class="sxs-lookup"><span data-stu-id="e0a84-132">IID</span></span><br/></td>
<td><span data-ttu-id="e0a84-133">IID_ITsSbTarget se define como:</span><span class="sxs-lookup"><span data-stu-id="e0a84-133">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="e0a84-134">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="e0a84-134">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="e0a84-135">e85e10ea-db0b-4752-B456-5fd5840901c0 en Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e0a84-135">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="e0a84-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0a84-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0a84-137">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="e0a84-137">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="e0a84-138">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="e0a84-138">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[<span data-ttu-id="e0a84-139">**TSSD \_**</span><span class="sxs-lookup"><span data-stu-id="e0a84-139">**TSSD\_ConnectionPoint**</span></span>](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)
</dt> </dl>

 

 





