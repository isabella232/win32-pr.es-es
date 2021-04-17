---
description: El \_ método get Item devuelve el atributo especificado por el índice.
ms.assetid: 67e36587-0bf5-4586-ace9-ef107f0b6548
title: 'Método ITAttributeList:: get_Item (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33745c10bf95fe8a1e9c6d9edc73cad54855a8c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690926"
---
# <a name="itattributelistget_item-method"></a><span data-ttu-id="c15bc-103">ITAttributeList:: get \_ Item (método)</span><span class="sxs-lookup"><span data-stu-id="c15bc-103">ITAttributeList::get\_Item method</span></span>

<span data-ttu-id="c15bc-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c15bc-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c15bc-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="c15bc-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c15bc-106">El método **Get \_ Item** devuelve el atributo especificado por el índice.</span><span class="sxs-lookup"><span data-stu-id="c15bc-106">The **get\_Item** method returns the attribute specified by the index.</span></span>

## <a name="syntax"></a><span data-ttu-id="c15bc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c15bc-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG Index,
  [out] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="c15bc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c15bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c15bc-109">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c15bc-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c15bc-110">Índice del elemento que se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="c15bc-110">Index of the item to get.</span></span>

</dd> <dt>

<span data-ttu-id="c15bc-111">*pval* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c15bc-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c15bc-112">Puntero a un **BSTR** que contiene los valores del elemento.</span><span class="sxs-lookup"><span data-stu-id="c15bc-112">Pointer to a **BSTR** containing the values of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c15bc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c15bc-113">Return value</span></span>

<span data-ttu-id="c15bc-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="c15bc-114">This method can return one of these values.</span></span>



| <span data-ttu-id="c15bc-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c15bc-115">Return code</span></span>                                                                                   | <span data-ttu-id="c15bc-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c15bc-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="c15bc-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c15bc-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c15bc-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c15bc-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c15bc-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="c15bc-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c15bc-120">El parámetro *pval* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="c15bc-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="c15bc-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c15bc-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c15bc-122">El parámetro de *Índice* no es válido.</span><span class="sxs-lookup"><span data-stu-id="c15bc-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="c15bc-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c15bc-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c15bc-124">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="c15bc-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="c15bc-125"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="c15bc-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="c15bc-126">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="c15bc-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c15bc-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="c15bc-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="c15bc-128">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="c15bc-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="c15bc-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c15bc-129">Remarks</span></span>

<span data-ttu-id="c15bc-130">La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *pval* .</span><span class="sxs-lookup"><span data-stu-id="c15bc-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *pVal* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c15bc-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c15bc-131">Requirements</span></span>



| <span data-ttu-id="c15bc-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c15bc-132">Requirement</span></span> | <span data-ttu-id="c15bc-133">Value</span><span class="sxs-lookup"><span data-stu-id="c15bc-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c15bc-134">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="c15bc-134">TAPI version</span></span><br/> | <span data-ttu-id="c15bc-135">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="c15bc-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c15bc-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c15bc-136">Header</span></span><br/>       | <dl> <span data-ttu-id="c15bc-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="c15bc-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="c15bc-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c15bc-138">Library</span></span><br/>      | <dl> <span data-ttu-id="c15bc-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c15bc-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c15bc-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c15bc-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="c15bc-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c15bc-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c15bc-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="c15bc-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c15bc-143">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="c15bc-143">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

