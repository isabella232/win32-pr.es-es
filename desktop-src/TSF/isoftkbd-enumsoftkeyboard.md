---
title: Método ISoftKbd EnumSoftKeyboard (Softkbdc. h)
description: El método ISoftKbd EnumSoftKeyboard enumera los posibles teclados de software que admiten el idioma especificado.
ms.assetid: c71f99e5-c4c2-4b09-a58f-d3f4348d0c5d
keywords:
- Método EnumSoftKeyboard marco de trabajo de servicios de texto
- Método EnumSoftKeyboard marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método EnumSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.EnumSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecdb083684163798a68674628a8b1abc2460268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491891"
---
# <a name="isoftkbdenumsoftkeyboard-method"></a><span data-ttu-id="8427e-106">ISoftKbd:: EnumSoftKeyboard (método)</span><span class="sxs-lookup"><span data-stu-id="8427e-106">ISoftKbd::EnumSoftKeyboard method</span></span>

<span data-ttu-id="8427e-107">El método **ISoftKbd:: EnumSoftKeyboard** enumera los posibles teclados de software que admiten el idioma especificado.</span><span class="sxs-lookup"><span data-stu-id="8427e-107">The **ISoftKbd::EnumSoftKeyboard** method enumerates the possible soft keyboards that support the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="8427e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8427e-108">Syntax</span></span>


```C++
HRESULT EnumSoftKeyboard(
  [in]  LANGID langid,
  [out] DWORD  *lpdwKeyboard
);
```



## <a name="parameters"></a><span data-ttu-id="8427e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8427e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8427e-110">*langid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8427e-110">*langid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8427e-111">Identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="8427e-111">Language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="8427e-112">*lpdwKeyboard* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8427e-112">*lpdwKeyboard* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8427e-113">Puntero a un búfer en el que este método recupera los identificadores de los teclados de software disponibles.</span><span class="sxs-lookup"><span data-stu-id="8427e-113">Pointer to a buffer in which this method retrieves identifiers of the available soft keyboards.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8427e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8427e-114">Return value</span></span>

<span data-ttu-id="8427e-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="8427e-115">This method can return one of these values.</span></span>



| <span data-ttu-id="8427e-116">Value</span><span class="sxs-lookup"><span data-stu-id="8427e-116">Value</span></span>                                                                                        | <span data-ttu-id="8427e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="8427e-117">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="8427e-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8427e-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="8427e-119">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="8427e-119">The method was successful.</span></span><br/>         |
| <dl> <span data-ttu-id="8427e-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8427e-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="8427e-121">El parámetro *langid* no es válido.</span><span class="sxs-lookup"><span data-stu-id="8427e-121">The *langid* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8427e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8427e-122">Requirements</span></span>



| <span data-ttu-id="8427e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8427e-123">Requirement</span></span> | <span data-ttu-id="8427e-124">Value</span><span class="sxs-lookup"><span data-stu-id="8427e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8427e-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8427e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8427e-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8427e-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8427e-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8427e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8427e-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8427e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8427e-129">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="8427e-129">Redistributable</span></span><br/>          | <span data-ttu-id="8427e-130">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8427e-130">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="8427e-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8427e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8427e-132"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="8427e-132"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="8427e-133">IDL</span><span class="sxs-lookup"><span data-stu-id="8427e-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8427e-134"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8427e-134"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="8427e-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8427e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8427e-136"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8427e-136"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8427e-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="8427e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8427e-138">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="8427e-138">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





