---
description: 'ITMediaCollection::get__NewEnum método : el método get \_ \_ NewEnum devuelve un enumerador para la colección.'
ms.assetid: 22b1eb48-e1ef-4694-a1dc-b2de326989c8
title: Método ITMediaCollection::get__NewEnum (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6683ce0a00f0128cb959dd5a2c39e8b06382f65d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098363"
---
# <a name="itmediacollectionget__newenum-method"></a><span data-ttu-id="3d84f-103">ItMediaCollection::get \_ \_ NewEnum (método)</span><span class="sxs-lookup"><span data-stu-id="3d84f-103">ITMediaCollection::get\_\_NewEnum method</span></span>

<span data-ttu-id="3d84f-104">\[ Los controles e interfaces de conferencia de telefonía IP de Encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3d84f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3d84f-105">La API de cliente RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="3d84f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3d84f-106">El **método get \_ \_ NewEnum** devuelve un enumerador para la colección.</span><span class="sxs-lookup"><span data-stu-id="3d84f-106">The **get\_\_NewEnum** method returns an enumerator for the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d84f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d84f-107">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="3d84f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d84f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d84f-109">*pVal* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3d84f-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d84f-110">Puntero a una [interfaz IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) en un objeto enumerador de la colección.</span><span class="sxs-lookup"><span data-stu-id="3d84f-110">Pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface on an enumerator object for the collection.</span></span>

<span data-ttu-id="3d84f-111">Llame al [método QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en la interfaz **IUnknown** devuelta para obtener un puntero a una interfaz de enumeración [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en la colección.</span><span class="sxs-lookup"><span data-stu-id="3d84f-111">Call the [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the returned **IUnknown** interface to obtain a pointer to an [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumeration interface on the collection.</span></span> <span data-ttu-id="3d84f-112">**IEnumVARIANT proporciona** una serie de métodos que puede usar para recorrer en iteración la colección.</span><span class="sxs-lookup"><span data-stu-id="3d84f-112">**IEnumVARIANT** provides a number of methods that you can use to iterate through the collection.</span></span>

<span data-ttu-id="3d84f-113">Para obtener más información, vea la sección Comentarios que se muestra más adelante.</span><span class="sxs-lookup"><span data-stu-id="3d84f-113">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d84f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d84f-114">Return value</span></span>

<span data-ttu-id="3d84f-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="3d84f-115">This method can return one of these values.</span></span>



| <span data-ttu-id="3d84f-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3d84f-116">Return code</span></span>                                                                                   | <span data-ttu-id="3d84f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d84f-117">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3d84f-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3d84f-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3d84f-119">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3d84f-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3d84f-120"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="3d84f-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3d84f-121">El *parámetro pVal* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="3d84f-121">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="3d84f-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3d84f-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3d84f-123">No existe memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="3d84f-123">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="3d84f-124"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="3d84f-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="3d84f-125">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="3d84f-125">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3d84f-126"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="3d84f-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="3d84f-127">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="3d84f-127">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="3d84f-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3d84f-128">Remarks</span></span>

<span data-ttu-id="3d84f-129">Este método es intercambiable con [**get \_ EnumerationIf, salvo**](itmediacollection-get-enumerationif.md) que devuelve **IUnknown en** lugar de [**IEnumMedia.**](ienummedia.md)</span><span class="sxs-lookup"><span data-stu-id="3d84f-129">This method is interchangeable with [**get\_EnumerationIf**](itmediacollection-get-enumerationif.md) except that it returns **IUnknown** instead of [**IEnumMedia**](ienummedia.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d84f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d84f-130">Requirements</span></span>



| <span data-ttu-id="3d84f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d84f-131">Requirement</span></span> | <span data-ttu-id="3d84f-132">Valor</span><span class="sxs-lookup"><span data-stu-id="3d84f-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d84f-133">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="3d84f-133">TAPI version</span></span><br/> | <span data-ttu-id="3d84f-134">Requiere TAPI 3.0 o posterior</span><span class="sxs-lookup"><span data-stu-id="3d84f-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3d84f-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d84f-135">Header</span></span><br/>       | <dl> <span data-ttu-id="3d84f-136"><dt>Sdpblb.h</dt></span><span class="sxs-lookup"><span data-stu-id="3d84f-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="3d84f-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3d84f-137">Library</span></span><br/>      | <dl> <span data-ttu-id="3d84f-138"><dt>Uuid.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d84f-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3d84f-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3d84f-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="3d84f-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d84f-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d84f-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3d84f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d84f-142">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="3d84f-142">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

