---
description: El método Insertat (inserta un elemento (o varias copias de un elemento) o todos los elementos de otra matriz en un índice especificado.
audience: developer
ms.assetid: 1d6355bc-7df2-4aa3-8e47-0239d726ed7d
ms.tgt_platform: multiple
title: 'Métodos CHStringArray:: Insertat ((ChStrArr. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 4047b740778c8d0adf1f2b5981b2f3aac5ba9529
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707353"
---
# <a name="chstringarrayinsertat-methods"></a><span data-ttu-id="9fc81-103">CHStringArray:: Insertat ((métodos)</span><span class="sxs-lookup"><span data-stu-id="9fc81-103">CHStringArray::InsertAt methods</span></span>

<span data-ttu-id="9fc81-104">\[La clase [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="9fc81-104">\[The [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="9fc81-105">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="9fc81-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="9fc81-106">El método **insertat (** inserta un elemento (o varias copias de un elemento) o todos los elementos de otra matriz en un índice especificado.</span><span class="sxs-lookup"><span data-stu-id="9fc81-106">The **InsertAt** method inserts an element (or multiple copies of an element) or all the elements of another array at a specified index.</span></span>

### <a name="overload-list"></a><span data-ttu-id="9fc81-107">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="9fc81-107">Overload list</span></span>



| <span data-ttu-id="9fc81-108">Método</span><span class="sxs-lookup"><span data-stu-id="9fc81-108">Method</span></span>                                                                               | <span data-ttu-id="9fc81-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fc81-109">Description</span></span>                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc81-110">[**Insertat ((int, LPCWSTR, int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9fc81-110">[**InsertAt(int,LPCWSTR,int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))</span></span>       | <span data-ttu-id="9fc81-111">Inserta uno o más elementos en un índice especificado de una matriz.</span><span class="sxs-lookup"><span data-stu-id="9fc81-111">Inserts one or more elements at a specified index in an array.</span></span><br/>                                               |
| <span data-ttu-id="9fc81-112">[**Insertat ((int, CHStringArray \* )**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span><span class="sxs-lookup"><span data-stu-id="9fc81-112">[**InsertAt(int,CHStringArray\*)**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span></span> | <span data-ttu-id="9fc81-113">Inserta todos los elementos de otro [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) en el índice especificado de una matriz.</span><span class="sxs-lookup"><span data-stu-id="9fc81-113">Inserts all the elements of another [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) at a specified index in an array.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9fc81-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fc81-114">Requirements</span></span>



| <span data-ttu-id="9fc81-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fc81-115">Requirement</span></span> | <span data-ttu-id="9fc81-116">Value</span><span class="sxs-lookup"><span data-stu-id="9fc81-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc81-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fc81-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9fc81-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9fc81-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="9fc81-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fc81-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9fc81-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fc81-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="9fc81-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fc81-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fc81-122"><dt>ChStrArr. h (incluye FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9fc81-122"><dt>ChStrArr.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9fc81-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9fc81-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="9fc81-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fc81-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="9fc81-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9fc81-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fc81-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fc81-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fc81-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fc81-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fc81-128">**CHStringArray**</span><span class="sxs-lookup"><span data-stu-id="9fc81-128">**CHStringArray**</span></span>](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray)
</dt> </dl>

<span data-ttu-id="9fc81-129">�</span><span class="sxs-lookup"><span data-stu-id="9fc81-129">�</span></span>

<span data-ttu-id="9fc81-130">�</span><span class="sxs-lookup"><span data-stu-id="9fc81-130">�</span></span>
