---
description: El \_ método get AttributeList obtiene la lista de atributos.
ms.assetid: 75518257-3339-441f-9965-b93e27f0e2bf
title: 'Método ITAttributeList:: get_AttributeList (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499352cd5087f478e58653fd304e27101db9b433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690927"
---
# <a name="itattributelistget_attributelist-method"></a><span data-ttu-id="a80fe-103">ITAttributeList:: get \_ AttributeList (método)</span><span class="sxs-lookup"><span data-stu-id="a80fe-103">ITAttributeList::get\_AttributeList method</span></span>

<span data-ttu-id="a80fe-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a80fe-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a80fe-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="a80fe-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a80fe-106">El método **Get \_ AttributeList** obtiene la lista de atributos.</span><span class="sxs-lookup"><span data-stu-id="a80fe-106">The **get\_AttributeList** method gets the list of attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a80fe-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a80fe-107">Syntax</span></span>


```C++
HRESULT get_AttributeList(
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="a80fe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a80fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a80fe-109">*pval* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a80fe-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a80fe-110">Matriz de atributos.</span><span class="sxs-lookup"><span data-stu-id="a80fe-110">Array of attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a80fe-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a80fe-111">Return value</span></span>

<span data-ttu-id="a80fe-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="a80fe-112">This method can return one of these values.</span></span>



| <span data-ttu-id="a80fe-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a80fe-113">Return code</span></span>                                                                                   | <span data-ttu-id="a80fe-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a80fe-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a80fe-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a80fe-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a80fe-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a80fe-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a80fe-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="a80fe-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a80fe-118">El parámetro *pval* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="a80fe-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="a80fe-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a80fe-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a80fe-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="a80fe-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a80fe-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="a80fe-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a80fe-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="a80fe-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a80fe-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="a80fe-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a80fe-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="a80fe-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="a80fe-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a80fe-125">Requirements</span></span>



| <span data-ttu-id="a80fe-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a80fe-126">Requirement</span></span> | <span data-ttu-id="a80fe-127">Value</span><span class="sxs-lookup"><span data-stu-id="a80fe-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a80fe-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="a80fe-128">TAPI version</span></span><br/> | <span data-ttu-id="a80fe-129">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a80fe-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a80fe-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a80fe-130">Header</span></span><br/>       | <dl> <span data-ttu-id="a80fe-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a80fe-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a80fe-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a80fe-132">Library</span></span><br/>      | <dl> <span data-ttu-id="a80fe-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a80fe-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a80fe-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a80fe-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="a80fe-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a80fe-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a80fe-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a80fe-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a80fe-137">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="a80fe-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> <dt>

[<span data-ttu-id="a80fe-138">**ITAttributeList::p de \_ AttributeList**</span><span class="sxs-lookup"><span data-stu-id="a80fe-138">**ITAttributeList::put\_AttributeList**</span></span>](itattributelist-put-attributelist.md)
</dt> </dl>

 

 




