---
description: Cada uno de los constructores siguientes Inicializa un nuevo objeto CHString con los datos especificados.
audience: developer
ms.assetid: d49e1600-d5d4-4c44-81c5-1b8c53b768de
ms.tgt_platform: multiple
title: 'Constructores CHString:: CHString (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 711d2f28680a9f273ff808876e30e92f66336b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277126"
---
# <a name="chstringchstring-constructors"></a><span data-ttu-id="e837c-103">Constructores CHString:: CHString</span><span class="sxs-lookup"><span data-stu-id="e837c-103">CHString::CHString constructors</span></span>

<span data-ttu-id="e837c-104">\[La clase [**CHString**](chstring.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="e837c-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="e837c-105">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="e837c-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="e837c-106">Cada uno de los constructores siguientes Inicializa un nuevo objeto [**CHString**](chstring.md) con los datos especificados.</span><span class="sxs-lookup"><span data-stu-id="e837c-106">Each of the following constructors initializes a new [**CHString**](chstring.md) object with the specified data.</span></span>

### <a name="overload-list"></a><span data-ttu-id="e837c-107">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="e837c-107">Overload list</span></span>



| <span data-ttu-id="e837c-108">Constructor</span><span class="sxs-lookup"><span data-stu-id="e837c-108">Constructor</span></span>                                                                        | <span data-ttu-id="e837c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e837c-109">Description</span></span>                                                  |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="e837c-110">**CHString()**</span><span class="sxs-lookup"><span data-stu-id="e837c-110">**CHString()**</span></span>](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                          | <span data-ttu-id="e837c-111">Crea un objeto CHString vacío.</span><span class="sxs-lookup"><span data-stu-id="e837c-111">Creates an empty CHString object.</span></span><br/>                 |
| <span data-ttu-id="e837c-112">[**CHString (LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))</span><span class="sxs-lookup"><span data-stu-id="e837c-112">[**CHString(LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))</span></span>                              | <span data-ttu-id="e837c-113">Se inicializa con el valor de LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="e837c-113">Initializes with the LPCSTR value.</span></span><br/>                |
| <span data-ttu-id="e837c-114">[**CHString (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="e837c-114">[**CHString(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))</span></span>                            | <span data-ttu-id="e837c-115">Se inicializa con el valor de LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="e837c-115">Initializes with the LPCWSTR value.</span></span><br/>               |
| <span data-ttu-id="e837c-116">[**CHString (WCHAR, int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))</span><span class="sxs-lookup"><span data-stu-id="e837c-116">[**CHString(WCHAR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))</span></span>                        | <span data-ttu-id="e837c-117">Inicializa con las copias int del valor WCHAR.</span><span class="sxs-lookup"><span data-stu-id="e837c-117">Initializes with int copies of the WCHAR value.</span></span><br/>   |
| <span data-ttu-id="e837c-118">[**CHString (LPCWSTR, int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))</span><span class="sxs-lookup"><span data-stu-id="e837c-118">[**CHString(LPCWSTR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))</span></span>                    | <span data-ttu-id="e837c-119">Inicializa con las copias int del valor de LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="e837c-119">Initializes with int copies of the LPCWSTR value.</span></span><br/> |
| <span data-ttu-id="e837c-120">[**CHString (const CHString&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))</span><span class="sxs-lookup"><span data-stu-id="e837c-120">[**CHString(const CHString&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))</span></span>            | <span data-ttu-id="e837c-121">Replica el parámetro CHString.</span><span class="sxs-lookup"><span data-stu-id="e837c-121">Replicates the CHString parameter.</span></span><br/>                |
| <span data-ttu-id="e837c-122">[**CHString (const sin signo \* )**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar))</span><span class="sxs-lookup"><span data-stu-id="e837c-122">[**CHString(const unsigned char\*)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar))</span></span> | <span data-ttu-id="e837c-123">Se inicializa con el valor al que apunta char \* .</span><span class="sxs-lookup"><span data-stu-id="e837c-123">Initializes with the value pointed to by char\*.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="e837c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e837c-124">Requirements</span></span>



| <span data-ttu-id="e837c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e837c-125">Requirement</span></span> | <span data-ttu-id="e837c-126">Value</span><span class="sxs-lookup"><span data-stu-id="e837c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e837c-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e837c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e837c-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e837c-128">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="e837c-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e837c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e837c-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e837c-130">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="e837c-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e837c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e837c-132"><dt>ChString. h (incluye FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e837c-132"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e837c-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e837c-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="e837c-134"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e837c-134"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="e837c-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e837c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e837c-136"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e837c-136"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="e837c-137">�</span><span class="sxs-lookup"><span data-stu-id="e837c-137">�</span></span>

<span data-ttu-id="e837c-138">�</span><span class="sxs-lookup"><span data-stu-id="e837c-138">�</span></span>
