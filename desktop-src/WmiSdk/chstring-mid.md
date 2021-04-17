---
description: El método Mid extrae una subcadena de longitud nCount caracteres de una cadena CHString, comenzando en la posición Nprimer (basada en cero). El método devuelve una copia de la subcadena extraída.
audience: developer
ms.assetid: 2036813b-f991-4ca3-95d3-8bbe858aae09
ms.tgt_platform: multiple
title: 'Métodos CHString:: MID (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5d05259128f80bcb21d00144d19002ca58ce39c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716289"
---
# <a name="chstringmid-methods"></a><span data-ttu-id="8c937-104">CHString:: MID (métodos)</span><span class="sxs-lookup"><span data-stu-id="8c937-104">CHString::Mid methods</span></span>

<span data-ttu-id="8c937-105">\[La clase [**CHString**](chstring.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="8c937-105">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="8c937-106">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="8c937-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="8c937-107">El método **Mid** extrae una subcadena de longitud *nCount* caracteres de una cadena [**CHString**](chstring.md) , comenzando en la posición *nprimer* (basada en cero).</span><span class="sxs-lookup"><span data-stu-id="8c937-107">The **Mid** method extracts a substring of length *nCount* characters from a [**CHString**](chstring.md) string, starting at position *nFirst* (zero-based).</span></span> <span data-ttu-id="8c937-108">El método devuelve una copia de la subcadena extraída.</span><span class="sxs-lookup"><span data-stu-id="8c937-108">The method returns a copy of the extracted substring.</span></span>

### <a name="overload-list"></a><span data-ttu-id="8c937-109">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="8c937-109">Overload list</span></span>



| <span data-ttu-id="8c937-110">Método</span><span class="sxs-lookup"><span data-stu-id="8c937-110">Method</span></span>                                        | <span data-ttu-id="8c937-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c937-111">Description</span></span>                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| <span data-ttu-id="8c937-112">[**MID (int, int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int))</span><span class="sxs-lookup"><span data-stu-id="8c937-112">[**Mid(int,int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int))</span></span> | <span data-ttu-id="8c937-113">Extrae una subcadena de la longitud y el punto inicial especificados.</span><span class="sxs-lookup"><span data-stu-id="8c937-113">Extracts a substring of specified length and beginning point.</span></span><br/> |
| <span data-ttu-id="8c937-114">[**MID (int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span><span class="sxs-lookup"><span data-stu-id="8c937-114">[**Mid(int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span></span>         | <span data-ttu-id="8c937-115">Extrae una subcadena que comienza en int.</span><span class="sxs-lookup"><span data-stu-id="8c937-115">Extracts a substring beginning at int.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="8c937-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c937-116">Requirements</span></span>



| <span data-ttu-id="8c937-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c937-117">Requirement</span></span> | <span data-ttu-id="8c937-118">Value</span><span class="sxs-lookup"><span data-stu-id="8c937-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c937-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c937-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8c937-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c937-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="8c937-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c937-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8c937-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c937-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="8c937-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c937-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c937-124"><dt>ChString. h (incluye FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c937-124"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8c937-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c937-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="8c937-126"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c937-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="8c937-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c937-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c937-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c937-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="8c937-129">�</span><span class="sxs-lookup"><span data-stu-id="8c937-129">�</span></span>

<span data-ttu-id="8c937-130">�</span><span class="sxs-lookup"><span data-stu-id="8c937-130">�</span></span>
