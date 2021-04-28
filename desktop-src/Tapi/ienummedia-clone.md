---
description: 'Método IEnumMedia::Clone: el método Clone crea otro enumerador que contiene el mismo estado de enumeración que el actual.'
ms.assetid: b48399f5-daaa-40e4-bd80-a918539d25c6
title: Método IEnumMedia::Clone (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f81542e1b0e3fc5bfb44e59827608396d7d906c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114553"
---
# <a name="ienummediaclone-method"></a><span data-ttu-id="e40fa-103">IEnumMedia::Clone (método)</span><span class="sxs-lookup"><span data-stu-id="e40fa-103">IEnumMedia::Clone method</span></span>

<span data-ttu-id="e40fa-104">\[ Los controles e interfaces de Conferencia de telefonía IP de Encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e40fa-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e40fa-105">La API de cliente RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="e40fa-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e40fa-106">El **método Clone** crea otro enumerador que contiene el mismo estado de enumeración que el actual.</span><span class="sxs-lookup"><span data-stu-id="e40fa-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="e40fa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e40fa-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumMedia **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="e40fa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e40fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e40fa-109">*ppEnum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e40fa-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e40fa-110">Puntero al nuevo [**objeto IEnumMedia.**](ienummedia.md)</span><span class="sxs-lookup"><span data-stu-id="e40fa-110">Pointer to the new [**IEnumMedia**](ienummedia.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e40fa-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e40fa-111">Return value</span></span>

<span data-ttu-id="e40fa-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="e40fa-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e40fa-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e40fa-113">Value</span></span>                                                                                         | <span data-ttu-id="e40fa-114">Significado</span><span class="sxs-lookup"><span data-stu-id="e40fa-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e40fa-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e40fa-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e40fa-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e40fa-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e40fa-117"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="e40fa-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e40fa-118">El *parámetro ppEnum* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="e40fa-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="e40fa-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e40fa-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e40fa-120">No existe memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="e40fa-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e40fa-121"><dt>**E \_ UNEXPECTED**</dt></span><span class="sxs-lookup"><span data-stu-id="e40fa-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="e40fa-122">Error por motivos desconocidos.</span><span class="sxs-lookup"><span data-stu-id="e40fa-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="e40fa-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e40fa-123">Remarks</span></span>

<span data-ttu-id="e40fa-124">TAPI llama al **método AddRef** en la [**interfaz IEnumMedia**](ienummedia.md) devuelta por **IEnumMedia::Clone**.</span><span class="sxs-lookup"><span data-stu-id="e40fa-124">TAPI calls the **AddRef** method on the [**IEnumMedia**](ienummedia.md) interface returned by **IEnumMedia::Clone**.</span></span> <span data-ttu-id="e40fa-125">La aplicación debe llamar **a Release** en la **interfaz IEnumMedia** para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="e40fa-125">The application must call **Release** on the **IEnumMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="e40fa-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e40fa-126">Requirements</span></span>



| <span data-ttu-id="e40fa-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e40fa-127">Requirement</span></span> | <span data-ttu-id="e40fa-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e40fa-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e40fa-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="e40fa-129">TAPI version</span></span><br/> | <span data-ttu-id="e40fa-130">Requiere TAPI 3.0 o posterior</span><span class="sxs-lookup"><span data-stu-id="e40fa-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e40fa-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e40fa-131">Header</span></span><br/>       | <dl> <span data-ttu-id="e40fa-132"><dt>Sdpblb.h</dt></span><span class="sxs-lookup"><span data-stu-id="e40fa-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e40fa-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e40fa-133">Library</span></span><br/>      | <dl> <span data-ttu-id="e40fa-134"><dt>Uuid.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e40fa-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e40fa-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e40fa-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="e40fa-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e40fa-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e40fa-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e40fa-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e40fa-138">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="e40fa-138">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




