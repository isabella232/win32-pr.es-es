---
description: 'Más información acerca de: JetGetSessionParameter (función)'
title: JetGetSessionParameter función)
TOCTitle: JetGetSessionParameter Function
ms:assetid: 36fbcc06-a72d-4bfb-976b-1b705487732a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835039(v=EXCHG.10)
ms:contentKeyID: 49894661
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetGetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0ac02142d48009d668d903b39163b425d738b55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907632"
---
# <a name="jetgetsessionparameter-function"></a><span data-ttu-id="7cf76-103">JetGetSessionParameter función)</span><span class="sxs-lookup"><span data-stu-id="7cf76-103">JetGetSessionParameter Function</span></span>


<span data-ttu-id="7cf76-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7cf76-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="7cf76-105">La función **JetGetSessionParameter** lee el parámetro de sesión para la sesión especificada.</span><span class="sxs-lookup"><span data-stu-id="7cf76-105">The **JetGetSessionParameter** function reads the session parameter for the given session.</span></span>

<span data-ttu-id="7cf76-106">La función **JetGetSessionParameter** se presentó en el sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7cf76-106">The **JetGetSessionParameter** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetGetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __out_cap_post_count_(cbParamMax, *pcbParamActual)  void* pvParam,
  __in          unsigned long cbParamMax,
  __out_opt_    unsigned long pcbParamActual
);
```

### <a name="parameters"></a><span data-ttu-id="7cf76-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7cf76-107">Parameters</span></span>

<span data-ttu-id="7cf76-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="7cf76-108">*sesid*</span></span>

<span data-ttu-id="7cf76-109">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="7cf76-109">The session to use for this call.</span></span>

<span data-ttu-id="7cf76-110">Cuando se especifica, se omite la instancia especificada y se utilizará la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="7cf76-110">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="7cf76-111">*sesparamid*</span><span class="sxs-lookup"><span data-stu-id="7cf76-111">*sesparamid*</span></span>

<span data-ttu-id="7cf76-112">IDENTIFICADOR del parámetro de sesión que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="7cf76-112">The ID of the session parameter to set.</span></span>

<span data-ttu-id="7cf76-113">*pvParam*</span><span class="sxs-lookup"><span data-stu-id="7cf76-113">*pvParam*</span></span>

<span data-ttu-id="7cf76-114">Datos de este parámetro de sesión.</span><span class="sxs-lookup"><span data-stu-id="7cf76-114">Data in this session parameter.</span></span>

<span data-ttu-id="7cf76-115">*cbParamMax*</span><span class="sxs-lookup"><span data-stu-id="7cf76-115">*cbParamMax*</span></span>

<span data-ttu-id="7cf76-116">Tamaño máximo del conjunto de datos en este parámetro de sesión.</span><span class="sxs-lookup"><span data-stu-id="7cf76-116">The maximum size of the data set in this session parameter.</span></span>

<span data-ttu-id="7cf76-117">*pcbParamActual*</span><span class="sxs-lookup"><span data-stu-id="7cf76-117">*pcbParamActual*</span></span>

<span data-ttu-id="7cf76-118">Tamaño real del conjunto de datos en este parámetro de sesión.</span><span class="sxs-lookup"><span data-stu-id="7cf76-118">The actual size of the data set in this session parameter.</span></span>

### <a name="return-value"></a><span data-ttu-id="7cf76-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7cf76-119">Return value</span></span>

<span data-ttu-id="7cf76-120">Si se ejecuta correctamente, el búfer de salida adecuado para el parámetro de sesión solicitado se establecerá en el valor de ese parámetro de sesión.</span><span class="sxs-lookup"><span data-stu-id="7cf76-120">On success, the output buffer appropriate for the requested session parameter will be set to the value of that session parameter.</span></span>

<span data-ttu-id="7cf76-121">En caso de error, el estado de los búferes de salida será undefined.</span><span class="sxs-lookup"><span data-stu-id="7cf76-121">On failure, the state of the output buffers will be undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7cf76-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7cf76-122">Remarks</span></span>

<span data-ttu-id="7cf76-123">El parámetro Session se usa para la duración de la sesión o hasta que se restablezca el valor.</span><span class="sxs-lookup"><span data-stu-id="7cf76-123">The session parameter is used for the lifetime of the session or until the value is reset.</span></span>

#### <a name="requirements"></a><span data-ttu-id="7cf76-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cf76-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7cf76-125"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="7cf76-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7cf76-126">Requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7cf76-126">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cf76-127"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7cf76-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7cf76-128">Requiere Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="7cf76-128">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cf76-129"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7cf76-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7cf76-130">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="7cf76-130">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cf76-131"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="7cf76-131"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7cf76-132">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7cf76-132">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cf76-133"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7cf76-133"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7cf76-134">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7cf76-134">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7cf76-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="7cf76-135">See also</span></span>

[<span data-ttu-id="7cf76-136">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="7cf76-136">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="7cf76-137">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7cf76-137">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7cf76-138">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="7cf76-138">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="7cf76-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7cf76-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7cf76-140">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="7cf76-140">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="7cf76-141">JetInit</span><span class="sxs-lookup"><span data-stu-id="7cf76-141">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="7cf76-142">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="7cf76-142">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="7cf76-143">JetStopService</span><span class="sxs-lookup"><span data-stu-id="7cf76-143">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="7cf76-144">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="7cf76-144">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
