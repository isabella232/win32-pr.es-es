---
title: Método ISoftKbd GetSoftKeyboardTypeMode (Softkbdc. h)
description: El método ISoftKbd GetSoftKeyboardTypeMode recupera el modo de tipo para un teclado en pantalla.
ms.assetid: 77294652-b82e-4b69-bb55-5ebebc3c97c7
keywords:
- Método GetSoftKeyboardTypeMode marco de trabajo de servicios de texto
- Método GetSoftKeyboardTypeMode marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método GetSoftKeyboardTypeMode
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6aad6d60c50ee0050cf418018dd6db1c7a33efc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421896"
---
# <a name="isoftkbdgetsoftkeyboardtypemode-method"></a><span data-ttu-id="0803b-106">ISoftKbd:: GetSoftKeyboardTypeMode (método)</span><span class="sxs-lookup"><span data-stu-id="0803b-106">ISoftKbd::GetSoftKeyboardTypeMode method</span></span>

<span data-ttu-id="0803b-107">El método **ISoftKbd:: GetSoftKeyboardTypeMode** recupera el modo de tipo para un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="0803b-107">The **ISoftKbd::GetSoftKeyboardTypeMode** method retrieves the type mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="0803b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0803b-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardTypeMode(
  [out] TYPEMODE *lpTypeMode
);
```



## <a name="parameters"></a><span data-ttu-id="0803b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0803b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0803b-110">*lpTypeMode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0803b-110">*lpTypeMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0803b-111">Puntero a un búfer en el que este método recupera el modo de tipo.</span><span class="sxs-lookup"><span data-stu-id="0803b-111">Pointer to a buffer in which this method retrieves the type mode.</span></span> <span data-ttu-id="0803b-112">Se definen los valores posibles para la enumeración [**TYPEMODE**](typemode.md) .</span><span class="sxs-lookup"><span data-stu-id="0803b-112">Possible values are defined for the [**TYPEMODE**](typemode.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0803b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0803b-113">Return value</span></span>

<span data-ttu-id="0803b-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0803b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="0803b-115">Value</span><span class="sxs-lookup"><span data-stu-id="0803b-115">Value</span></span>                                                                                        | <span data-ttu-id="0803b-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="0803b-116">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="0803b-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0803b-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0803b-118">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="0803b-118">The method was successful.</span></span><br/>             |
| <dl> <span data-ttu-id="0803b-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0803b-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0803b-120">El parámetro *lpTypeMode* no es válido.</span><span class="sxs-lookup"><span data-stu-id="0803b-120">The *lpTypeMode* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0803b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0803b-121">Requirements</span></span>



| <span data-ttu-id="0803b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0803b-122">Requirement</span></span> | <span data-ttu-id="0803b-123">Value</span><span class="sxs-lookup"><span data-stu-id="0803b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0803b-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0803b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0803b-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0803b-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0803b-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0803b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0803b-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0803b-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0803b-128">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0803b-128">Redistributable</span></span><br/>          | <span data-ttu-id="0803b-129">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0803b-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="0803b-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0803b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0803b-131"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="0803b-131"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="0803b-132">IDL</span><span class="sxs-lookup"><span data-stu-id="0803b-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0803b-133"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0803b-133"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="0803b-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0803b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0803b-135"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0803b-135"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0803b-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="0803b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0803b-137">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="0803b-137">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="0803b-138">**ISoftKbd::SetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="0803b-138">**ISoftKbd::SetSoftKeyboardTypeMode**</span></span>](isoftkbd-setsoftkeyboardtypemode.md)
</dt> <dt>

[<span data-ttu-id="0803b-139">**TYPEMODE**</span><span class="sxs-lookup"><span data-stu-id="0803b-139">**TYPEMODE**</span></span>](typemode.md)
</dt> </dl>

 

 





