---
description: Se produce cuando se activa una aplicación de la tienda Windows.
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: 'Evento ICoreApplicationView:: Activated (Windows. ApplicationModel. Core. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612f7110aa149396b18815afe664ee404c70fc52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275412"
---
# <a name="icoreapplicationviewactivated-event"></a><span data-ttu-id="61f42-103">Evento ICoreApplicationView:: Activated</span><span class="sxs-lookup"><span data-stu-id="61f42-103">ICoreApplicationView::Activated event</span></span>

<span data-ttu-id="61f42-104">Se produce cuando se activa una aplicación de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="61f42-104">Occurs when a Windows Store app is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="61f42-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61f42-105">Syntax</span></span>


```C++
void Activated(
  [in] ITypedEventHandler<ICoreApplicationView*, IActivatedEventArgs*> handler
);
```



## <a name="parameters"></a><span data-ttu-id="61f42-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61f42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61f42-107">*controlador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="61f42-107">*handler* \[in\]</span></span>
<span data-ttu-id="61f42-108"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="61f42-108"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="61f42-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61f42-109">Return value</span></span>

<span data-ttu-id="61f42-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="61f42-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="61f42-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61f42-111">Remarks</span></span>

<span data-ttu-id="61f42-112">No llame al método [**Exit**](/previous-versions//hh438368(v=vs.85)) desde dentro del *controlador*.</span><span class="sxs-lookup"><span data-stu-id="61f42-112">Do not call the [**Exit**](/previous-versions//hh438368(v=vs.85)) method from within *handler*.</span></span>

## <a name="requirements"></a><span data-ttu-id="61f42-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61f42-113">Requirements</span></span>



| <span data-ttu-id="61f42-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="61f42-114">Requirement</span></span> | <span data-ttu-id="61f42-115">Value</span><span class="sxs-lookup"><span data-stu-id="61f42-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61f42-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61f42-116">Minimum supported client</span></span><br/> | <span data-ttu-id="61f42-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="61f42-117">Windows 8</span></span><br/>                                                                                         |
| <span data-ttu-id="61f42-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61f42-118">Minimum supported server</span></span><br/> | <span data-ttu-id="61f42-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61f42-119">Windows Server 2012</span></span><br/>                                                                               |
| <span data-ttu-id="61f42-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61f42-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="61f42-121"><dt>Windows. ApplicationModel. Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="61f42-121"><dt>Windows.ApplicationModel.Core.h</dt></span></span> </dl>   |
| <span data-ttu-id="61f42-122">IDL</span><span class="sxs-lookup"><span data-stu-id="61f42-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="61f42-123"><dt>Windows. ApplicationModel. Core. idl</dt></span><span class="sxs-lookup"><span data-stu-id="61f42-123"><dt>Windows.ApplicationModel.Core.idl</dt></span></span> </dl> |



 

 
