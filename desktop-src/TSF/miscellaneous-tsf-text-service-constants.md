---
title: Constantes de servicio de texto TSF variadas (Ctffunc. h)
description: Los siguientes valores se usan con servicios de texto.
ms.assetid: 38110314-1638-4963-92b6-4ba2f81fb7c2
topic_type:
- apiref
api_name:
- TF_MENUREADY
- TF_PROPUI_STATUS_SAVETOFILE
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ebd7d22f9cfbd59f95ee3dcfe68229536503b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686143"
---
# <a name="miscellaneous-tsf-text-service-constants"></a><span data-ttu-id="2e60e-103">Constantes de servicio de texto TSF variadas</span><span class="sxs-lookup"><span data-stu-id="2e60e-103">Miscellaneous TSF Text Service Constants</span></span>

<span data-ttu-id="2e60e-104">Los siguientes valores se usan con servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="2e60e-104">The following values are used with text services.</span></span>



| <span data-ttu-id="2e60e-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="2e60e-105">Constant/value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="2e60e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e60e-106">Description</span></span>                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MENUREADY"></span><span id="tf_menuready"></span><dl> <span data-ttu-id="2e60e-107"><dt>**TF \_ MENUREADY**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="2e60e-107"><dt>**TF\_MENUREADY**</dt> <dt>0x00000001</dt></span></span> </dl>                                                | <span data-ttu-id="2e60e-108">No se usa actualmente.</span><span class="sxs-lookup"><span data-stu-id="2e60e-108">Not currently used.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="TF_PROPUI_STATUS_SAVETOFILE"></span><span id="tf_propui_status_savetofile"></span><dl> <span data-ttu-id="2e60e-109"><dt>**TF \_ PROPUI \_ status \_ SAVETOFILE**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="2e60e-109"><dt>**TF\_PROPUI\_STATUS\_SAVETOFILE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="2e60e-110">La propiedad se puede serializar.</span><span class="sxs-lookup"><span data-stu-id="2e60e-110">The property can be serialized.</span></span> <span data-ttu-id="2e60e-111">Si este valor no está presente, la propiedad no se puede serializar.</span><span class="sxs-lookup"><span data-stu-id="2e60e-111">If this value is not present, the property cannot be serialized.</span></span> <span data-ttu-id="2e60e-112">Este valor se usa con [ITfFnPropertyUIStatus:: getStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus) y [ITfFnPropertyUIStatus:: SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus).</span><span class="sxs-lookup"><span data-stu-id="2e60e-112">This value is used with [ITfFnPropertyUIStatus::GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus) and [ITfFnPropertyUIStatus::SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2e60e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e60e-113">Requirements</span></span>



| <span data-ttu-id="2e60e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e60e-114">Requirement</span></span> | <span data-ttu-id="2e60e-115">Value</span><span class="sxs-lookup"><span data-stu-id="2e60e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e60e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e60e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2e60e-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2e60e-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2e60e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e60e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2e60e-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e60e-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2e60e-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="2e60e-120">Redistributable</span></span><br/>          | <span data-ttu-id="2e60e-121">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2e60e-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="2e60e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e60e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e60e-123"><dt>Ctffunc. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e60e-123"><dt>Ctffunc.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e60e-124">IDL</span><span class="sxs-lookup"><span data-stu-id="2e60e-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e60e-125"><dt>Ctffunc. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e60e-125"><dt>Ctffunc.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e60e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e60e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e60e-127">ITfFnPropertyUIStatus:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="2e60e-127">ITfFnPropertyUIStatus::GetStatus</span></span>](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus)
</dt> <dt>

[<span data-ttu-id="2e60e-128">ITfFnPropertyUIStatus:: SetStatus</span><span class="sxs-lookup"><span data-stu-id="2e60e-128">ITfFnPropertyUIStatus::SetStatus</span></span>](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus)
</dt> </dl>

 

 





