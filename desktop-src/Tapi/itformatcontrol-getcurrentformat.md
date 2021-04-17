---
description: El método GetCurrentFormat recupera el formato de medios de la secuencia actual.
ms.assetid: 02d1b3b5-3639-4864-9b72-623bf94acf69
title: 'ITFormatControl:: GetCurrentFormat (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1b711b539ea9a92af6bd345c5a1f48b212b640b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690537"
---
# <a name="itformatcontrolgetcurrentformat-method"></a><span data-ttu-id="06884-103">ITFormatControl:: GetCurrentFormat (método)</span><span class="sxs-lookup"><span data-stu-id="06884-103">ITFormatControl::GetCurrentFormat method</span></span>

<span data-ttu-id="06884-104">\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="06884-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="06884-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="06884-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="06884-106">El método **GetCurrentFormat** recupera el formato de medios de la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="06884-106">The **GetCurrentFormat** method retrieves the media format of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="06884-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06884-107">Syntax</span></span>


```C++
HRESULT GetCurrentFormat(
  [out] AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="06884-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06884-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06884-109">*ppMediaType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="06884-109">*ppMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06884-110">Puntero a un descriptor de **\_ \_ tipo de medio am** del formato de terminal.</span><span class="sxs-lookup"><span data-stu-id="06884-110">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="06884-111">Para obtener más información sobre el **\_ \_ tipo de medio am**, consulte la documentación de DirectX.</span><span class="sxs-lookup"><span data-stu-id="06884-111">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06884-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06884-112">Return value</span></span>

<span data-ttu-id="06884-113">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="06884-113">This method can return one of these values.</span></span>



| <span data-ttu-id="06884-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="06884-114">Return code</span></span>                                                                                   | <span data-ttu-id="06884-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="06884-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="06884-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="06884-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="06884-117">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="06884-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="06884-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="06884-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="06884-119">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="06884-119">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="06884-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06884-120">Requirements</span></span>



| <span data-ttu-id="06884-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="06884-121">Requirement</span></span> | <span data-ttu-id="06884-122">Value</span><span class="sxs-lookup"><span data-stu-id="06884-122">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="06884-123">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="06884-123">TAPI version</span></span><br/> | <span data-ttu-id="06884-124">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="06884-124">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="06884-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06884-125">Header</span></span><br/>       | <dl> <span data-ttu-id="06884-126"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="06884-126"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="06884-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="06884-127">Library</span></span><br/>      | <dl> <span data-ttu-id="06884-128"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06884-128"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="06884-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="06884-129">DLL</span></span><br/>          | <dl> <span data-ttu-id="06884-130"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06884-130"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06884-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="06884-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06884-132">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="06884-132">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 




