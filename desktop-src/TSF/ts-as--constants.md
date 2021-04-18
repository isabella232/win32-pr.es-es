---
title: Constantes de TS_AS_ (Textstor. h)
description: Las marcas siguientes especifican los eventos que llaman a los métodos AdviseSink.
ms.assetid: 8f406b67-f846-4712-b4be-811dbcc6ad55
topic_type:
- apiref
api_name:
- TS_AS_TEXT_CHANGE
- TS_AS_SEL_CHANGE
- TS_AS_LAYOUT_CHANGE
- TS_AS_ATTR_CHANGE
- TS_AS_STATUS_CHANGE
- TS_AS_ALL_SINKS
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7b36bdc2c3b559693503b2a8e408a0782855f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686131"
---
# <a name="ts_as_-constants"></a><span data-ttu-id="62f2c-103">TS \_ como \_ \* constantes</span><span class="sxs-lookup"><span data-stu-id="62f2c-103">TS\_AS\_\* Constants</span></span>

<span data-ttu-id="62f2c-104">Las marcas siguientes especifican los eventos que llaman a los métodos **AdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="62f2c-104">The following flags specify the events that call the **AdviseSink** methods.</span></span>



| <span data-ttu-id="62f2c-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="62f2c-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="62f2c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="62f2c-106">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="TS_AS_TEXT_CHANGE"></span><span id="ts_as_text_change"></span><dl> <span data-ttu-id="62f2c-107"><dt>**TS \_ Como \_ \_ cambio de texto**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="62f2c-107"><dt>**TS\_AS\_TEXT\_CHANGE**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                                                                                               | <span data-ttu-id="62f2c-108">El texto se cambia en el documento.</span><span class="sxs-lookup"><span data-stu-id="62f2c-108">Text is changed in the document.</span></span><br/>                          |
| <span id="TS_AS_SEL_CHANGE"></span><span id="ts_as_sel_change"></span><dl> <span data-ttu-id="62f2c-109"><dt>**TS \_ COMO \_ \_ cambio SEL**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="62f2c-109"><dt>**TS\_AS\_SEL\_CHANGE**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                                                                                                  | <span data-ttu-id="62f2c-110">Texto seleccionado en el documento.</span><span class="sxs-lookup"><span data-stu-id="62f2c-110">Text is selected in the document.</span></span><br/>                         |
| <span id="TS_AS_LAYOUT_CHANGE"></span><span id="ts_as_layout_change"></span><dl> <span data-ttu-id="62f2c-111"><dt>**TS \_ Como \_ \_ cambio de diseño**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="62f2c-111"><dt>**TS\_AS\_LAYOUT\_CHANGE**</dt> <dt>( 0x4 )</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="62f2c-112">Se cambia el diseño del documento.</span><span class="sxs-lookup"><span data-stu-id="62f2c-112">The layout of the document is changed.</span></span><br/>                    |
| <span id="TS_AS_ATTR_CHANGE"></span><span id="ts_as_attr_change"></span><dl> <span data-ttu-id="62f2c-113"><dt>**TS \_ Como \_ \_ cambio de atributo**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="62f2c-113"><dt>**TS\_AS\_ATTR\_CHANGE**</dt> <dt>( 0x8 )</dt></span></span> </dl>                                                                                                               | <span data-ttu-id="62f2c-114">Se cambian los atributos del documento.</span><span class="sxs-lookup"><span data-stu-id="62f2c-114">The attributes of the document is changed.</span></span><br/>                |
| <span id="TS_AS_STATUS_CHANGE"></span><span id="ts_as_status_change"></span><dl> <span data-ttu-id="62f2c-115"><dt>**TS \_ Como \_ \_ cambio de estado**</dt> <dt>(0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="62f2c-115"><dt>**TS\_AS\_STATUS\_CHANGE**</dt> <dt>( 0x10 )</dt></span></span> </dl>                                                                                                        | <span data-ttu-id="62f2c-116">Se cambia el estado del documento.</span><span class="sxs-lookup"><span data-stu-id="62f2c-116">The status of the document is changed.</span></span><br/>                    |
| <span id="TS_AS_ALL_SINKS"></span><span id="ts_as_all_sinks"></span><dl> <span data-ttu-id="62f2c-117"><dt>**TS \_ Dado que \_ todos los \_ receptores**</dt> <dt>(TS \_ as \_ Text cambian de \_ \| TS \_ como \_ SEL \_ Change TS as \| \_ \_ relayout Change TS as ATTR Change \_ \| \_ \_ \_ \| TS \_ as \_ status Change \_ )</dt></span><span class="sxs-lookup"><span data-stu-id="62f2c-117"><dt>**TS\_AS\_ALL\_SINKS**</dt> <dt>( TS\_AS\_TEXT\_CHANGE \| TS\_AS\_SEL\_CHANGE \| TS\_AS\_LAYOUT\_CHANGE \| TS\_AS\_ATTR\_CHANGE \| TS\_AS\_STATUS\_CHANGE )</dt></span></span> </dl> | <span data-ttu-id="62f2c-118">Uno de los cuatro eventos anteriores se produjo en el documento.</span><span class="sxs-lookup"><span data-stu-id="62f2c-118">One of the previous four events occurred in the document.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="62f2c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62f2c-119">Requirements</span></span>



| <span data-ttu-id="62f2c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="62f2c-120">Requirement</span></span> | <span data-ttu-id="62f2c-121">Value</span><span class="sxs-lookup"><span data-stu-id="62f2c-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62f2c-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62f2c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="62f2c-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="62f2c-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="62f2c-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62f2c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="62f2c-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="62f2c-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="62f2c-126">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="62f2c-126">Redistributable</span></span><br/>          | <span data-ttu-id="62f2c-127">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="62f2c-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="62f2c-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62f2c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="62f2c-129"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="62f2c-129"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="62f2c-130">IDL</span><span class="sxs-lookup"><span data-stu-id="62f2c-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="62f2c-131"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="62f2c-131"><dt>Textstor.idl</dt></span></span> </dl> |



 

 





