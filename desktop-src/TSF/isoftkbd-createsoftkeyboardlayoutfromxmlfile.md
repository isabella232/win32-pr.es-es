---
title: Método ISoftKbd CreateSoftKeyboardLayoutFromXMLFile (Softkbdc. h)
description: El método ISoftKbd CreateSoftKeyboardLayoutFromXMLFile crea una distribución de teclado en pantalla a partir del archivo XML especificado.
ms.assetid: e665adab-1d75-4e41-87bf-c8ce0f7a0399
keywords:
- Método CreateSoftKeyboardLayoutFromXMLFile marco de trabajo de servicios de texto
- Método CreateSoftKeyboardLayoutFromXMLFile marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método CreateSoftKeyboardLayoutFromXMLFile
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromXMLFile
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252db845c5e1cc732adc295e1989fee83d4ac6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686096"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromxmlfile-method"></a><span data-ttu-id="b4d1c-106">ISoftKbd:: CreateSoftKeyboardLayoutFromXMLFile (método)</span><span class="sxs-lookup"><span data-stu-id="b4d1c-106">ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile method</span></span>

<span data-ttu-id="b4d1c-107">El método **ISoftKbd:: CreateSoftKeyboardLayoutFromXMLFile** crea una distribución de teclado en pantalla a partir del archivo XML especificado.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-107">The **ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile** method creates a soft keyboard layout from the specified XML file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4d1c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4d1c-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardLayoutFromXMLFile(
  [in]  WCHAR *lpszKeyboardDesFile,
  [in]  INT   szFileStrLen,
  [out] DWORD *pdwLayoutCookie
);
```



## <a name="parameters"></a><span data-ttu-id="b4d1c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4d1c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4d1c-110">*lpszKeyboardDesFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b4d1c-110">*lpszKeyboardDesFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4d1c-111">Puntero a una cadena terminada en cero que indica el nombre del archivo XML.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-111">Pointer to a zero-terminated string indicating the name of the XML file.</span></span>

</dd> <dt>

<span data-ttu-id="b4d1c-112">*szFileStrLen* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b4d1c-112">*szFileStrLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4d1c-113">Cadena terminada en cero que indica la longitud del archivo XML.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-113">Zero-terminated string indicating the length of the XML file.</span></span>

</dd> <dt>

<span data-ttu-id="b4d1c-114">*pdwLayoutCookie* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b4d1c-114">*pdwLayoutCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4d1c-115">Puntero al búfer en el que este método recupera una cookie de distribución de teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-115">Pointer to the buffer in which this method retrieves a soft keyboard layout cookie.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4d1c-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4d1c-116">Return value</span></span>

<span data-ttu-id="b4d1c-117">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-117">This method can return one of these values.</span></span>



| <span data-ttu-id="b4d1c-118">Value</span><span class="sxs-lookup"><span data-stu-id="b4d1c-118">Value</span></span>                                                                                        | <span data-ttu-id="b4d1c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4d1c-119">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="b4d1c-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b4d1c-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="b4d1c-121">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-121">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="b4d1c-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b4d1c-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="b4d1c-123">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="b4d1c-123">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b4d1c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4d1c-124">Requirements</span></span>



| <span data-ttu-id="b4d1c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4d1c-125">Requirement</span></span> | <span data-ttu-id="b4d1c-126">Value</span><span class="sxs-lookup"><span data-stu-id="b4d1c-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4d1c-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4d1c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b4d1c-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b4d1c-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b4d1c-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4d1c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b4d1c-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4d1c-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b4d1c-131">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b4d1c-131">Redistributable</span></span><br/>          | <span data-ttu-id="b4d1c-132">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b4d1c-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="b4d1c-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4d1c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4d1c-134"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4d1c-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="b4d1c-135">IDL</span><span class="sxs-lookup"><span data-stu-id="b4d1c-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b4d1c-136"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b4d1c-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="b4d1c-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b4d1c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4d1c-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4d1c-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4d1c-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4d1c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4d1c-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="b4d1c-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="b4d1c-141">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span><span class="sxs-lookup"><span data-stu-id="b4d1c-141">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> </dl>

 

 





