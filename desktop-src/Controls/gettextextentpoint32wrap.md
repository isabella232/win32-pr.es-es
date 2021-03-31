---
title: GetTextExtentPoint32Wrap función)
description: Calcula el ancho y el alto de la cadena de texto especificada. Esta función contiene una llamada a GetTextExtentPoint.
ms.assetid: 156f9344-6071-451c-94c7-63f369a5573a
keywords:
- GetTextExtentPoint32Wrap (función) controles de Windows
topic_type:
- apiref
api_name:
- GetTextExtentPoint32Wrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a0db92ad019950cf8be0a72260da75acc06779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801232"
---
# <a name="gettextextentpoint32wrap-function"></a><span data-ttu-id="efa2f-105">GetTextExtentPoint32Wrap función)</span><span class="sxs-lookup"><span data-stu-id="efa2f-105">GetTextExtentPoint32Wrap function</span></span>

<span data-ttu-id="efa2f-106">\[**GetTextExtentPoint32Wrap** está disponible a través de Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="efa2f-106">\[**GetTextExtentPoint32Wrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="efa2f-107">Podría modificarse o no estar disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="efa2f-107">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="efa2f-108">Se recomienda usar [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) directamente en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="efa2f-108">It is recommended to use [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) directly instead.\]</span></span>

<span data-ttu-id="efa2f-109">Calcula el ancho y el alto de la cadena de texto especificada.</span><span class="sxs-lookup"><span data-stu-id="efa2f-109">Computes the width and height of the specified string of text.</span></span> <span data-ttu-id="efa2f-110">Esta función contiene una llamada a [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span><span class="sxs-lookup"><span data-stu-id="efa2f-110">This function wraps a call to [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span></span>

## <a name="syntax"></a><span data-ttu-id="efa2f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="efa2f-111">Syntax</span></span>


```C++
BOOL GetTextExtentPoint32Wrap(
  _In_  HDC     hdc,
  _In_  LPCTSTR lpString,
  _In_  UINT    cbCount,
  _Out_ LPSIZE  lpSize
);
```



## <a name="parameters"></a><span data-ttu-id="efa2f-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="efa2f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efa2f-113">*HDC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="efa2f-113">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efa2f-114">Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="efa2f-114">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="efa2f-115">Identificador del contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efa2f-115">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="efa2f-116">*lpString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="efa2f-116">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efa2f-117">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="efa2f-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="efa2f-118">Puntero a un búfer que contiene el texto que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="efa2f-118">A pointer to a buffer that contains the text to be drawn.</span></span> <span data-ttu-id="efa2f-119">No es necesario que la cadena termine en cero, ya que *cbCount* especifica la longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="efa2f-119">The string does not need to be zero-terminated, since *cbCount* specifies the length of the string.</span></span>

</dd> <dt>

<span data-ttu-id="efa2f-120">*cbCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="efa2f-120">*cbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efa2f-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="efa2f-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="efa2f-122">La longitud, en bytes, de la cadena a la que apunta *lpString*.</span><span class="sxs-lookup"><span data-stu-id="efa2f-122">The length, in bytes, of the string pointed to by *lpString*.</span></span>

</dd> <dt>

<span data-ttu-id="efa2f-123">*lpSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="efa2f-123">*lpSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efa2f-124">Tipo: **LPSIZE**</span><span class="sxs-lookup"><span data-stu-id="efa2f-124">Type: **LPSIZE**</span></span>

<span data-ttu-id="efa2f-125">Cuando este método devuelve un valor, contiene un puntero a una estructura de [**tamaño**](/previous-versions//dd145106(v=vs.85)) que contiene las dimensiones de la cadena, en unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="efa2f-125">When this method returns, contains a pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure containing the dimensions of the string, in logical units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efa2f-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="efa2f-126">Return value</span></span>

<span data-ttu-id="efa2f-127">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="efa2f-127">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="efa2f-128">Devuelve un valor distinto de cero si es correcto; de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="efa2f-128">Returns a nonzero value if successful; otherwise, 0.</span></span>

<span data-ttu-id="efa2f-129">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="efa2f-129">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="efa2f-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="efa2f-130">Remarks</span></span>

<span data-ttu-id="efa2f-131">**GetTextExtentPoint32Wrap** no se exporta por nombre o se declara en un archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="efa2f-131">**GetTextExtentPoint32Wrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="efa2f-132">Para usarlo, debe utilizar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y el ordinal de solicitud 420 de ComCtl32.dll para obtener un puntero de función.</span><span class="sxs-lookup"><span data-stu-id="efa2f-132">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 420 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="efa2f-133">Para obtener más comentarios, vea [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span><span class="sxs-lookup"><span data-stu-id="efa2f-133">For additional remarks, please see [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span></span>

## <a name="requirements"></a><span data-ttu-id="efa2f-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efa2f-134">Requirements</span></span>



| <span data-ttu-id="efa2f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="efa2f-135">Requirement</span></span> | <span data-ttu-id="efa2f-136">Value</span><span class="sxs-lookup"><span data-stu-id="efa2f-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efa2f-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="efa2f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="efa2f-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="efa2f-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="efa2f-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="efa2f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="efa2f-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="efa2f-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="efa2f-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="efa2f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efa2f-142"><dt>Comctl32.dll (versión 5,81 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="efa2f-142"><dt>Comctl32.dll (version 5.81 or later)</dt></span></span> </dl> |



 

