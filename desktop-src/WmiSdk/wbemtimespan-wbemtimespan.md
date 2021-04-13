---
description: El constructor de la clase WBEMTimeSpan crea un objeto de intervalo de tiempo. El constructor está sobrecargado.
audience: developer
ms.assetid: 337dc247-9904-457a-a1f3-e1cf29b61126
ms.tgt_platform: multiple
title: 'Constructores WBEMTimeSpan:: WbemTimeSpan (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: af5724a91ab50b5286e23b3c8095163e415d95e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279283"
---
# <a name="wbemtimespanwbemtimespan-constructors"></a><span data-ttu-id="d9248-104">Constructores WBEMTimeSpan:: WbemTimeSpan</span><span class="sxs-lookup"><span data-stu-id="d9248-104">WBEMTimeSpan::WbemTimeSpan constructors</span></span>

<span data-ttu-id="d9248-105">\[La clase [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="d9248-105">\[The [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="d9248-106">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="d9248-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="d9248-107">El constructor de la clase **WBEMTimeSpan** crea un objeto de intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="d9248-107">The **WBEMTimeSpan** class constructor creates a time span object.</span></span> <span data-ttu-id="d9248-108">El constructor está sobrecargado.</span><span class="sxs-lookup"><span data-stu-id="d9248-108">The constructor is overloaded.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d9248-109">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="d9248-109">Overload list</span></span>



| <span data-ttu-id="d9248-110">Constructor</span><span class="sxs-lookup"><span data-stu-id="d9248-110">Constructor</span></span>                                                                                                 | <span data-ttu-id="d9248-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9248-111">Description</span></span>                                                                  |
|:------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span data-ttu-id="d9248-112">[**WBEMTimeSpan()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span><span class="sxs-lookup"><span data-stu-id="d9248-112">[**WBEMTimeSpan()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span></span>                                                      | <span data-ttu-id="d9248-113">Crea un objeto de intervalo de tiempo no inicializado.</span><span class="sxs-lookup"><span data-stu-id="d9248-113">Creates an uninitialized time span object.</span></span><br/>                        |
| <span data-ttu-id="d9248-114">[**WBEMTimeSpan (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span><span class="sxs-lookup"><span data-stu-id="d9248-114">[**WBEMTimeSpan(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span></span>                                               | <span data-ttu-id="d9248-115">Inicializa el nuevo objeto de intervalo de tiempo en el valor del parámetro.</span><span class="sxs-lookup"><span data-stu-id="d9248-115">Initializes the new time span object to value in the parameter.</span></span><br/>   |
| <span data-ttu-id="d9248-116">[**WBEMTimeSpan (int, int, int, int, int, int, int)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(int_int_int_int_int_int_int))</span><span class="sxs-lookup"><span data-stu-id="d9248-116">[**WBEMTimeSpan(int,int,int,int,int,int,int)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(int_int_int_int_int_int_int))</span></span> | <span data-ttu-id="d9248-117">Inicializa el nuevo objeto de intervalo de tiempo en los valores de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="d9248-117">Initializes the new time span object to values in the parameters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d9248-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9248-118">Requirements</span></span>



| <span data-ttu-id="d9248-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9248-119">Requirement</span></span> | <span data-ttu-id="d9248-120">Value</span><span class="sxs-lookup"><span data-stu-id="d9248-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9248-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9248-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d9248-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9248-122">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="d9248-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9248-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d9248-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9248-124">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="d9248-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9248-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9248-126"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9248-126"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="d9248-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d9248-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9248-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9248-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="d9248-129">�</span><span class="sxs-lookup"><span data-stu-id="d9248-129">�</span></span>

<span data-ttu-id="d9248-130">�</span><span class="sxs-lookup"><span data-stu-id="d9248-130">�</span></span>
