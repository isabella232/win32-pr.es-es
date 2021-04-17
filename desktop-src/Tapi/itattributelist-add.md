---
description: El método Add agrega el atributo en el índice especificado.
ms.assetid: 5b74c177-bf5c-4547-bebb-034a9a10be13
title: 'ITAttributeList:: Add (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5504a216549231aca82eac3b3311ae7208eb8432
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681184"
---
# <a name="itattributelistadd-method"></a><span data-ttu-id="467b8-103">ITAttributeList:: Add (método)</span><span class="sxs-lookup"><span data-stu-id="467b8-103">ITAttributeList::Add method</span></span>

<span data-ttu-id="467b8-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="467b8-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="467b8-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="467b8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="467b8-106">El método **Add** agrega el atributo en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="467b8-106">The **Add** method adds the attribute at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="467b8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="467b8-107">Syntax</span></span>


```C++
HRESULT Add(
  [in] LONG Index,
  [in] BSTR pAttribute
);
```



## <a name="parameters"></a><span data-ttu-id="467b8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="467b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="467b8-109">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="467b8-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="467b8-110">Índice del atributo que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="467b8-110">Index of the attribute to add.</span></span>

</dd> <dt>

<span data-ttu-id="467b8-111">*pAttribute* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="467b8-111">*pAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="467b8-112">Puntero a un **BSTR** que contiene el valor del atributo que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="467b8-112">Pointer to a **BSTR** containing the value of the attribute to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="467b8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="467b8-113">Return value</span></span>

<span data-ttu-id="467b8-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="467b8-114">This method can return one of these values.</span></span>



| <span data-ttu-id="467b8-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="467b8-115">Return code</span></span>                                                                                   | <span data-ttu-id="467b8-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="467b8-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="467b8-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="467b8-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="467b8-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="467b8-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="467b8-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="467b8-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="467b8-120">El parámetro *index* o *pAttribute* no es válido.</span><span class="sxs-lookup"><span data-stu-id="467b8-120">The *Index* or *pAttribute* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="467b8-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="467b8-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="467b8-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="467b8-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="467b8-123"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="467b8-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="467b8-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="467b8-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="467b8-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="467b8-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="467b8-126">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="467b8-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="467b8-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="467b8-127">Remarks</span></span>

<span data-ttu-id="467b8-128">La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para el parámetro *PAttribute* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando la variable ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="467b8-128">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pAttribute* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="467b8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="467b8-129">Requirements</span></span>



| <span data-ttu-id="467b8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="467b8-130">Requirement</span></span> | <span data-ttu-id="467b8-131">Value</span><span class="sxs-lookup"><span data-stu-id="467b8-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="467b8-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="467b8-132">TAPI version</span></span><br/> | <span data-ttu-id="467b8-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="467b8-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="467b8-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="467b8-134">Header</span></span><br/>       | <dl> <span data-ttu-id="467b8-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="467b8-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="467b8-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="467b8-136">Library</span></span><br/>      | <dl> <span data-ttu-id="467b8-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="467b8-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="467b8-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="467b8-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="467b8-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="467b8-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="467b8-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="467b8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="467b8-141">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="467b8-141">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

