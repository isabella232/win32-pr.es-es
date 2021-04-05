---
title: Método ISoftKbd ShowSoftKeyboard (Softkbdc. h)
description: El método ISoftKbd ShowSoftKeyboard muestra un teclado en pantalla.
ms.assetid: 7e24bef1-accb-40f6-a549-fb676abf9971
keywords:
- Método ShowSoftKeyboard marco de trabajo de servicios de texto
- Método ShowSoftKeyboard marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método ShowSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.ShowSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b319e7782a19571cf827175566e1af056c34cd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078826"
---
# <a name="isoftkbdshowsoftkeyboard-method"></a><span data-ttu-id="1319e-106">ISoftKbd:: ShowSoftKeyboard (método)</span><span class="sxs-lookup"><span data-stu-id="1319e-106">ISoftKbd::ShowSoftKeyboard method</span></span>

<span data-ttu-id="1319e-107">El método **ISoftKbd:: ShowSoftKeyboard** muestra un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="1319e-107">The **ISoftKbd::ShowSoftKeyboard** method displays a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="1319e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1319e-108">Syntax</span></span>


```C++
HRESULT ShowSoftKeyboard(
  [in] INT iShow
);
```



## <a name="parameters"></a><span data-ttu-id="1319e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1319e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1319e-110">*iShow* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1319e-110">*iShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1319e-111">Entero que indica el tipo de teclado en pantalla que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="1319e-111">Integer indicating the type of soft keyboard to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1319e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1319e-112">Return value</span></span>

<span data-ttu-id="1319e-113">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="1319e-113">This method can return one of these values.</span></span>



| <span data-ttu-id="1319e-114">Value</span><span class="sxs-lookup"><span data-stu-id="1319e-114">Value</span></span>                                                                                | <span data-ttu-id="1319e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="1319e-115">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="1319e-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1319e-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1319e-117">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1319e-117">The method was successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1319e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1319e-118">Requirements</span></span>



| <span data-ttu-id="1319e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1319e-119">Requirement</span></span> | <span data-ttu-id="1319e-120">Value</span><span class="sxs-lookup"><span data-stu-id="1319e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1319e-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1319e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1319e-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1319e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1319e-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1319e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1319e-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1319e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1319e-125">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="1319e-125">Redistributable</span></span><br/>          | <span data-ttu-id="1319e-126">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1319e-126">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="1319e-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1319e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1319e-128"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="1319e-128"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="1319e-129">IDL</span><span class="sxs-lookup"><span data-stu-id="1319e-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1319e-130"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1319e-130"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="1319e-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1319e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1319e-132"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1319e-132"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1319e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="1319e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1319e-134">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="1319e-134">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





