---
description: El método SetAlias configura un alias H. 323 predeterminado para la dirección. Este alias se usará en la llamada H. 323 configuración de Exchange para que la otra parte conozca el nombre de esta entidad.
ms.assetid: 09608214-7346-4ee8-bbfd-0877d3ad0766
title: 'IH323LineEx:: SetAlias (método) (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7341d177297cf95f46d07e503244f06b2c4dea71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690169"
---
# <a name="ih323lineexsetalias-method"></a><span data-ttu-id="c9201-104">IH323LineEx:: SetAlias (método)</span><span class="sxs-lookup"><span data-stu-id="c9201-104">IH323LineEx::SetAlias method</span></span>

<span data-ttu-id="c9201-105">\[**SetAlias** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c9201-105">\[**SetAlias** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c9201-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="c9201-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c9201-107">El método **SetAlias** configura un alias H. 323 predeterminado para la dirección.</span><span class="sxs-lookup"><span data-stu-id="c9201-107">The **SetAlias** method configures a default H.323 alias for the address.</span></span> <span data-ttu-id="c9201-108">Este alias se usará en la llamada H. 323 configuración de Exchange para que la otra parte conozca el nombre de esta entidad.</span><span class="sxs-lookup"><span data-stu-id="c9201-108">This alias will be used in the H.323 call setup exchange so that the other party knows the name of this party.</span></span>

<span data-ttu-id="c9201-109">Si se llama a este método por segunda vez, se sobrescribirá el alias anterior.</span><span class="sxs-lookup"><span data-stu-id="c9201-109">Calling this method a second time will overwrite the previous alias.</span></span>

<span data-ttu-id="c9201-110">El alias establecido en esta interfaz solo se usará cuando no haya ninguna otra manera de que el TSP busque un alias adecuado.</span><span class="sxs-lookup"><span data-stu-id="c9201-110">The alias set on this interface will be used only when there is no other way for the TSP to find a proper alias.</span></span> <span data-ttu-id="c9201-111">En el futuro, cuando se agrega la compatibilidad con Gatekeeper al TSP, el alias registrado en el equipo selector o asignado por el equipo selector invalidará lo que se establezca a través de este método.</span><span class="sxs-lookup"><span data-stu-id="c9201-111">In the future, when gatekeeper support is added into the TSP, the alias registered to the gatekeeper or assigned by the gatekeeper will override whatever is set through this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9201-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9201-112">Syntax</span></span>


```C++
HRESULT SetAlias(
  [in] WCHAR *strAlias,
  [in] DWORD dwLength
);
```



## <a name="parameters"></a><span data-ttu-id="c9201-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9201-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9201-114">*strAlias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c9201-114">*strAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9201-115">El alias que se va a usar, en Unicode.</span><span class="sxs-lookup"><span data-stu-id="c9201-115">The alias to be used, in Unicode.</span></span> <span data-ttu-id="c9201-116">No es necesaria la terminación **nula** .</span><span class="sxs-lookup"><span data-stu-id="c9201-116">**Null** termination is not required.</span></span>

</dd> <dt>

<span data-ttu-id="c9201-117">*dwLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c9201-117">*dwLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9201-118">La longitud del nombre de alias en número de caracteres, incluido el terminador **null** .</span><span class="sxs-lookup"><span data-stu-id="c9201-118">The length of the alias name in number of characters, including the **null** terminator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9201-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9201-119">Return value</span></span>

<span data-ttu-id="c9201-120">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="c9201-120">This method can return one of these values.</span></span>



| <span data-ttu-id="c9201-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c9201-121">Return code</span></span>                                                                               | <span data-ttu-id="c9201-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9201-122">Description</span></span>                                                                                                                      |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9201-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c9201-123"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="c9201-124">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c9201-124">Method succeeded.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="c9201-125"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="c9201-125"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="c9201-126">El número de caracteres indicado en *dwLength* supera el número real de caracteres en el parámetro *strAlias* .</span><span class="sxs-lookup"><span data-stu-id="c9201-126">The number of characters indicated in *dwLength* exceeds the actual number of characters in the *strAlias* parameter.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c9201-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9201-127">Requirements</span></span>



| <span data-ttu-id="c9201-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9201-128">Requirement</span></span> | <span data-ttu-id="c9201-129">Value</span><span class="sxs-lookup"><span data-stu-id="c9201-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9201-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="c9201-130">TAPI version</span></span><br/> | <span data-ttu-id="c9201-131">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="c9201-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c9201-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9201-132">Header</span></span><br/>       | <dl> <span data-ttu-id="c9201-133"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9201-133"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="c9201-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c9201-134">Library</span></span><br/>      | <dl> <span data-ttu-id="c9201-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9201-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c9201-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c9201-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="c9201-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9201-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




