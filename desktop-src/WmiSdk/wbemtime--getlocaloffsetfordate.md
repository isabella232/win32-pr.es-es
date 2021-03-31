---
description: El método GetLocalOffsetForDate devuelve el desplazamiento en minutos (+ o &\# 8211;) entre GMT y hora local para el tiempo proporcionado en el argumento.
audience: developer
ms.assetid: 15cc5f45-604c-4335-bcd3-92d62dc15420
ms.tgt_platform: multiple
title: 'Métodos WBEMTime:: GetLocalOffsetForDate (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e2c10cd076e18a803f0cb22b2798c09091cc70b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911478"
---
# <a name="wbemtimegetlocaloffsetfordate-methods"></a><span data-ttu-id="267e4-103">WBEMTime:: GetLocalOffsetForDate (métodos)</span><span class="sxs-lookup"><span data-stu-id="267e4-103">WBEMTime::GetLocalOffsetForDate methods</span></span>

<span data-ttu-id="267e4-104">\[La clase [**WBEMTime**](wbemtime.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="267e4-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="267e4-105">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="267e4-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="267e4-106">El método **GetLocalOffsetForDate** devuelve el desplazamiento en minutos (+ o) entre GMT y la hora local para el tiempo proporcionado en el argumento.</span><span class="sxs-lookup"><span data-stu-id="267e4-106">The **GetLocalOffsetForDate** method returns the offset in minutes (+ or �) between GMT and local time for the time supplied in the argument.</span></span>

### <a name="overload-list"></a><span data-ttu-id="267e4-107">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="267e4-107">Overload list</span></span>



| <span data-ttu-id="267e4-108">Método</span><span class="sxs-lookup"><span data-stu-id="267e4-108">Method</span></span>                                                                                           | <span data-ttu-id="267e4-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="267e4-109">Description</span></span>                                           |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| <span data-ttu-id="267e4-110">[**GetLocalOffsetForDate (Time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="267e4-110">[**GetLocalOffsetForDate(time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))</span></span>         | <span data-ttu-id="267e4-111">El argumento es una referencia a un **tiempo \_ t**.</span><span class="sxs-lookup"><span data-stu-id="267e4-111">Argument is a reference to a **time\_t**.</span></span><br/>  |
| <span data-ttu-id="267e4-112">[**GetLocalOffsetForDate (FILETIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))</span><span class="sxs-lookup"><span data-stu-id="267e4-112">[**GetLocalOffsetForDate(FILETIME\*)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))</span></span>     | <span data-ttu-id="267e4-113">El argumento es un puntero a un **FILETIME**.</span><span class="sxs-lookup"><span data-stu-id="267e4-113">Argument is a pointer to a **FILETIME**.</span></span><br/>   |
| [<span data-ttu-id="267e4-114">**GetLocalOffsetForDate (struct TM \* )**</span><span class="sxs-lookup"><span data-stu-id="267e4-114">**GetLocalOffsetForDate(struct tm\*)**</span></span>](/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getstructtm)   | <span data-ttu-id="267e4-115">El argumento es un puntero a la estructura **TM** .</span><span class="sxs-lookup"><span data-stu-id="267e4-115">Argument is a pointer to **tm** structure.</span></span><br/> |
| <span data-ttu-id="267e4-116">[**GetLocalOffsetForDate (SYSTEMTIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime))</span><span class="sxs-lookup"><span data-stu-id="267e4-116">[**GetLocalOffsetForDate(SYSTEMTIME\*)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime))</span></span> | <span data-ttu-id="267e4-117">El argumento es un puntero a un **SYSTEMTIME**.</span><span class="sxs-lookup"><span data-stu-id="267e4-117">Argument is a pointer to a **SYSTEMTIME**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="267e4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="267e4-118">Requirements</span></span>



| <span data-ttu-id="267e4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="267e4-119">Requirement</span></span> | <span data-ttu-id="267e4-120">Value</span><span class="sxs-lookup"><span data-stu-id="267e4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="267e4-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="267e4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="267e4-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="267e4-122">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="267e4-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="267e4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="267e4-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="267e4-124">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="267e4-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="267e4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="267e4-126"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="267e4-126"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="267e4-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="267e4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="267e4-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="267e4-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="267e4-129">�</span><span class="sxs-lookup"><span data-stu-id="267e4-129">�</span></span>

<span data-ttu-id="267e4-130">�</span><span class="sxs-lookup"><span data-stu-id="267e4-130">�</span></span>
