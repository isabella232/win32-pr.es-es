---
description: El método Create crea un nuevo componente ITTime.
ms.assetid: dee50454-8358-4898-b098-2de51505b658
title: 'ITTimeCollection:: Create (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df62bbc8f1ad2a24a9b80a7f5d0a25bc01f713d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679371"
---
# <a name="ittimecollectioncreate-method"></a><span data-ttu-id="cfe42-103">ITTimeCollection:: Create (método)</span><span class="sxs-lookup"><span data-stu-id="cfe42-103">ITTimeCollection::Create method</span></span>

<span data-ttu-id="cfe42-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cfe42-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cfe42-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="cfe42-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cfe42-106">El método **Create** crea un nuevo componente [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="cfe42-106">The **Create** method creates a new [**ITTime**](ittime.md) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfe42-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cfe42-107">Syntax</span></span>


```C++
HRESULT Create(
  [in]  LONG   Index,
  [out] ITTime **ppTime
);
```



## <a name="parameters"></a><span data-ttu-id="cfe42-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cfe42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfe42-109">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="cfe42-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe42-110">Índice del elemento que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="cfe42-110">Index of the item to create.</span></span> <span data-ttu-id="cfe42-111">(La matriz de índice está basada en uno).</span><span class="sxs-lookup"><span data-stu-id="cfe42-111">(The index array is one-based.)</span></span>

</dd> <dt>

<span data-ttu-id="cfe42-112">*ppTime* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cfe42-112">*ppTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe42-113">Puntero al componente b creado.</span><span class="sxs-lookup"><span data-stu-id="cfe42-113">Pointer to the b component created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfe42-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cfe42-114">Return value</span></span>

<span data-ttu-id="cfe42-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="cfe42-115">This method can return one of these values.</span></span>



| <span data-ttu-id="cfe42-116">Value</span><span class="sxs-lookup"><span data-stu-id="cfe42-116">Value</span></span>                                                                                         | <span data-ttu-id="cfe42-117">Significado</span><span class="sxs-lookup"><span data-stu-id="cfe42-117">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="cfe42-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="cfe42-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cfe42-119">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="cfe42-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cfe42-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="cfe42-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="cfe42-121">El parámetro *ppTime* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="cfe42-121">The *ppTime* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="cfe42-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cfe42-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="cfe42-123">El parámetro de *Índice* no es válido.</span><span class="sxs-lookup"><span data-stu-id="cfe42-123">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="cfe42-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cfe42-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cfe42-125">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="cfe42-125">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="cfe42-126"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="cfe42-126"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="cfe42-127">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="cfe42-127">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="cfe42-128"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="cfe42-128"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="cfe42-129">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="cfe42-129">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="cfe42-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cfe42-130">Remarks</span></span>

<span data-ttu-id="cfe42-131">TAPI llama al método **AddRef** en la interfaz [**ITTime**](ittime.md) devuelta por **ITTimeCollection:: Create**.</span><span class="sxs-lookup"><span data-stu-id="cfe42-131">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by **ITTimeCollection::Create**.</span></span> <span data-ttu-id="cfe42-132">La aplicación debe llamar a **Release** en la interfaz v para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="cfe42-132">The application must call **Release** on the v interface to free resources associated with it.</span></span>

<span data-ttu-id="cfe42-133">Esta función puede enviar datos a través de la conexión en formato no cifrado. por lo tanto, es posible que alguien que escucha en la red pueda leer los datos.</span><span class="sxs-lookup"><span data-stu-id="cfe42-133">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="cfe42-134">El riesgo de seguridad de enviar los datos en texto no cifrado debe tenerse en cuenta antes de usar este método.</span><span class="sxs-lookup"><span data-stu-id="cfe42-134">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfe42-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfe42-135">Requirements</span></span>



| <span data-ttu-id="cfe42-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfe42-136">Requirement</span></span> | <span data-ttu-id="cfe42-137">Value</span><span class="sxs-lookup"><span data-stu-id="cfe42-137">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe42-138">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="cfe42-138">TAPI version</span></span><br/> | <span data-ttu-id="cfe42-139">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="cfe42-139">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="cfe42-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cfe42-140">Header</span></span><br/>       | <dl> <span data-ttu-id="cfe42-141"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfe42-141"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="cfe42-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cfe42-142">Library</span></span><br/>      | <dl> <span data-ttu-id="cfe42-143"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cfe42-143"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cfe42-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cfe42-144">DLL</span></span><br/>          | <dl> <span data-ttu-id="cfe42-145"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfe42-145"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfe42-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfe42-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfe42-147">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="cfe42-147">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="cfe42-148">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="cfe42-148">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




