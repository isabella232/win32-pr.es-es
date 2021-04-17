---
title: Método ISoftKbd ShowKeysForKeyScanMode (Softkbdc. h)
description: El método ISoftKbd ShowKeysForKeyScanMode muestra las teclas utilizadas para el modo de exploración de teclas para un teclado en pantalla.
ms.assetid: bfa76e5b-6f6e-470a-ba3a-7ecff9f67f7b
keywords:
- Método ShowKeysForKeyScanMode marco de trabajo de servicios de texto
- Método ShowKeysForKeyScanMode marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método ShowKeysForKeyScanMode
topic_type:
- apiref
api_name:
- ISoftKbd.ShowKeysForKeyScanMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c46fbfc103c0ba40294e4c149d5fd427296765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492095"
---
# <a name="isoftkbdshowkeysforkeyscanmode-method"></a><span data-ttu-id="ecc30-106">ISoftKbd:: ShowKeysForKeyScanMode (método)</span><span class="sxs-lookup"><span data-stu-id="ecc30-106">ISoftKbd::ShowKeysForKeyScanMode method</span></span>

<span data-ttu-id="ecc30-107">El método **ISoftKbd:: ShowKeysForKeyScanMode** muestra las teclas utilizadas para el modo de exploración de teclas para un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="ecc30-107">The **ISoftKbd::ShowKeysForKeyScanMode** method displays the keys used for the key scan mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecc30-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ecc30-108">Syntax</span></span>


```C++
HRESULT ShowKeysForKeyScanMode(
  [in] KEYID *lpKeyID,
  [in] INT   iKeyNum,
  [in] BOOL  fHighL
);
```



## <a name="parameters"></a><span data-ttu-id="ecc30-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ecc30-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecc30-110">*lpKeyID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ecc30-110">*lpKeyID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecc30-111">Puntero a una matriz de elementos de clave de tipo que indica los identificadores de las claves que se van a mostrar.</span><span class="sxs-lookup"><span data-stu-id="ecc30-111">Pointer to an array of KEYID elements indicating the identifiers of keys to display.</span></span>

</dd> <dt>

<span data-ttu-id="ecc30-112">*iKeyNum* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ecc30-112">*iKeyNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecc30-113">Número de claves que se van a mostrar.</span><span class="sxs-lookup"><span data-stu-id="ecc30-113">The number of keys to display.</span></span>

</dd> <dt>

<span data-ttu-id="ecc30-114">*fHighL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ecc30-114">*fHighL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecc30-115">TRUE si el método va a resaltar las claves y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ecc30-115">TRUE if the method is to highlight the keys, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecc30-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ecc30-116">Return value</span></span>

<span data-ttu-id="ecc30-117">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="ecc30-117">This method can return one of these values.</span></span>



| <span data-ttu-id="ecc30-118">Value</span><span class="sxs-lookup"><span data-stu-id="ecc30-118">Value</span></span>                                                                                        | <span data-ttu-id="ecc30-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ecc30-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ecc30-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ecc30-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ecc30-121">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ecc30-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="ecc30-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ecc30-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ecc30-123">Uno de los parámetros no es válido.</span><span class="sxs-lookup"><span data-stu-id="ecc30-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ecc30-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecc30-124">Requirements</span></span>



| <span data-ttu-id="ecc30-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecc30-125">Requirement</span></span> | <span data-ttu-id="ecc30-126">Value</span><span class="sxs-lookup"><span data-stu-id="ecc30-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc30-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecc30-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ecc30-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ecc30-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ecc30-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecc30-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ecc30-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ecc30-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ecc30-131">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="ecc30-131">Redistributable</span></span><br/>          | <span data-ttu-id="ecc30-132">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ecc30-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="ecc30-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ecc30-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecc30-134"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecc30-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="ecc30-135">IDL</span><span class="sxs-lookup"><span data-stu-id="ecc30-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ecc30-136"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ecc30-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="ecc30-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ecc30-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecc30-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecc30-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecc30-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecc30-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecc30-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="ecc30-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





