---
title: Método ISoftKbd CreateSoftKeyboardLayoutFromResource (Softkbdc. h)
description: El método ISoftKbd CreateSoftKeybboardLayoutFromResource crea una distribución de teclado en pantalla a partir del recurso especificado.
ms.assetid: c1b2f8bd-8065-426d-9c23-67fa46a33dc8
keywords:
- Método CreateSoftKeyboardLayoutFromResource marco de trabajo de servicios de texto
- Método CreateSoftKeyboardLayoutFromResource marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método CreateSoftKeyboardLayoutFromResource
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromResource
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f454b5d8f3366517d91170d6a92d6a9dbed5764
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686097"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromresource-method"></a><span data-ttu-id="875ea-106">ISoftKbd:: CreateSoftKeyboardLayoutFromResource (método)</span><span class="sxs-lookup"><span data-stu-id="875ea-106">ISoftKbd::CreateSoftKeyboardLayoutFromResource method</span></span>

<span data-ttu-id="875ea-107">El método **ISoftKbd:: CreateSoftKeybboardLayoutFromResource** crea una distribución de teclado en pantalla a partir del recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="875ea-107">The **ISoftKbd::CreateSoftKeybboardLayoutFromResource** method creates a soft keyboard layout from the specified resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="875ea-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="875ea-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardLayoutFromResource(
  [in]  WCHAR *lpszResFile,
  [in]  WCHAR *lpszResType,
  [in]  WCHAR *lpszXMLResString,
  [out] DWORD *lpdwLayoutCookie
);
```



## <a name="parameters"></a><span data-ttu-id="875ea-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="875ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="875ea-110">*lpszResFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="875ea-110">*lpszResFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="875ea-111">Puntero a una cadena terminada en cero que indica el nombre del archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="875ea-111">Pointer to a zero-terminated string indicating the name of the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="875ea-112">*lpszResType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="875ea-112">*lpszResType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="875ea-113">Puntero a una cadena terminada en cero que indica el tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="875ea-113">Pointer to a zero-terminated string indicating the type of resource.</span></span>

</dd> <dt>

<span data-ttu-id="875ea-114">*lpszXMLResString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="875ea-114">*lpszXMLResString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="875ea-115">Puntero a una cadena terminada en cero que identifica el recurso.</span><span class="sxs-lookup"><span data-stu-id="875ea-115">Pointer to a zero-terminated string identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="875ea-116">*lpdwLayoutCookie* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="875ea-116">*lpdwLayoutCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="875ea-117">Puntero al búfer en el que este método recupera una cookie de distribución de teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="875ea-117">Pointer to the buffer in which this method retrieves a soft keyboard layout cookie.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="875ea-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="875ea-118">Return value</span></span>

<span data-ttu-id="875ea-119">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="875ea-119">This method can return one of these values.</span></span>



| <span data-ttu-id="875ea-120">Value</span><span class="sxs-lookup"><span data-stu-id="875ea-120">Value</span></span>                                                                                        | <span data-ttu-id="875ea-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="875ea-121">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="875ea-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="875ea-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="875ea-123">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="875ea-123">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="875ea-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="875ea-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="875ea-125">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="875ea-125">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="875ea-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="875ea-126">Requirements</span></span>



| <span data-ttu-id="875ea-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="875ea-127">Requirement</span></span> | <span data-ttu-id="875ea-128">Value</span><span class="sxs-lookup"><span data-stu-id="875ea-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="875ea-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="875ea-129">Minimum supported client</span></span><br/> | <span data-ttu-id="875ea-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="875ea-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="875ea-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="875ea-131">Minimum supported server</span></span><br/> | <span data-ttu-id="875ea-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="875ea-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="875ea-133">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="875ea-133">Redistributable</span></span><br/>          | <span data-ttu-id="875ea-134">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="875ea-134">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="875ea-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="875ea-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="875ea-136"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="875ea-136"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="875ea-137">IDL</span><span class="sxs-lookup"><span data-stu-id="875ea-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="875ea-138"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="875ea-138"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="875ea-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="875ea-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="875ea-140"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="875ea-140"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="875ea-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="875ea-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="875ea-142">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="875ea-142">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="875ea-143">**ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile**</span><span class="sxs-lookup"><span data-stu-id="875ea-143">**ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile**</span></span>](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)
</dt> <dt>

[<span data-ttu-id="875ea-144">**ISoftKbd::ShowSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="875ea-144">**ISoftKbd::ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)
</dt> </dl>

 

 





