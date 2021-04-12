---
description: Método sobrecargado que libera la memoria que contiene la ruta de acceso.
audience: developer
ms.assetid: 9164d7b2-15b8-4b73-ab8c-68ed45692ea0
ms.tgt_platform: multiple
title: 'CObjectPathParser:: Free (método) (ObjPath. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 86494e569f68d8eff8b691c648ec5e221b28b39d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277938"
---
# <a name="cobjectpathparserfree-methods"></a><span data-ttu-id="dc93a-103">CObjectPathParser:: Free (métodos)</span><span class="sxs-lookup"><span data-stu-id="dc93a-103">CObjectPathParser::Free methods</span></span>

<span data-ttu-id="dc93a-104">\[La clase [**CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="dc93a-104">\[The [**CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="dc93a-105">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="dc93a-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="dc93a-106">Método sobrecargado que libera la memoria que contiene la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="dc93a-106">An overloaded method that releases the memory that contains the path.</span></span>

### <a name="overload-list"></a><span data-ttu-id="dc93a-107">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="dc93a-107">Overload list</span></span>



| <span data-ttu-id="dc93a-108">Método</span><span class="sxs-lookup"><span data-stu-id="dc93a-108">Method</span></span>                                                                     | <span data-ttu-id="dc93a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc93a-109">Description</span></span>                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| <span data-ttu-id="dc93a-110">[**Free (LPWSTR)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(lpwstr))</span><span class="sxs-lookup"><span data-stu-id="dc93a-110">[**Free(LPWSTR)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(lpwstr))</span></span>                     | <span data-ttu-id="dc93a-111">Libera la memoria que contiene la ruta de acceso sin analizar.</span><span class="sxs-lookup"><span data-stu-id="dc93a-111">Releases the memory that contains the unparsed path.</span></span><br/>                      |
| <span data-ttu-id="dc93a-112">[**Gratis (ParsedObjectPath)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(parsedobjectpath))</span><span class="sxs-lookup"><span data-stu-id="dc93a-112">[**Free(ParsedObjectPath)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(parsedobjectpath))</span></span> | <span data-ttu-id="dc93a-113">Libera la memoria que contiene la estructura que tiene la ruta de acceso analizada.</span><span class="sxs-lookup"><span data-stu-id="dc93a-113">Releases the memory that contains the structure that has the parsed path.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="dc93a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc93a-114">Requirements</span></span>



| <span data-ttu-id="dc93a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc93a-115">Requirement</span></span> | <span data-ttu-id="dc93a-116">Value</span><span class="sxs-lookup"><span data-stu-id="dc93a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc93a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc93a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dc93a-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc93a-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="dc93a-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc93a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dc93a-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc93a-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="dc93a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc93a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc93a-122"><dt>ObjPath. h (incluye ObjPath. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc93a-122"><dt>ObjPath.h (include ObjPath.h)</dt></span></span> </dl>                                                      |
| <span data-ttu-id="dc93a-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc93a-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="dc93a-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc93a-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="dc93a-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc93a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc93a-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc93a-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc93a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc93a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc93a-128">**CObjectPathParser**</span><span class="sxs-lookup"><span data-stu-id="dc93a-128">**CObjectPathParser**</span></span>](/windows/win32/api/objpath/nl-objpath-cobjectpathparser)
</dt> </dl>

<span data-ttu-id="dc93a-129">�</span><span class="sxs-lookup"><span data-stu-id="dc93a-129">�</span></span>

<span data-ttu-id="dc93a-130">�</span><span class="sxs-lookup"><span data-stu-id="dc93a-130">�</span></span>
