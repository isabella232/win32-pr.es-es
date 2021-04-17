---
description: La interfaz IAMSetErrorLog establece o recupera un registro de errores en los servicios de edición de DirectShow (DES).
ms.assetid: ce658533-eacf-4b5d-9910-dca918de09e7
title: Interfaz IAMSetErrorLog (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0a24d29625bf08bc2f4c728a61f5188e8bec211
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653521"
---
# <a name="iamseterrorlog-interface"></a><span data-ttu-id="2e378-103">Interfaz IAMSetErrorLog</span><span class="sxs-lookup"><span data-stu-id="2e378-103">IAMSetErrorLog interface</span></span>

> [!Note]  
> <span data-ttu-id="2e378-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="2e378-104">\[Deprecated.</span></span> <span data-ttu-id="2e378-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2e378-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2e378-106">La `IAMSetErrorLog` interfaz establece o recupera un registro de errores en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="2e378-106">The `IAMSetErrorLog` interface sets or retrieves an error log in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="2e378-107">El objeto Timeline implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="2e378-107">The timeline object implements this interface.</span></span> <span data-ttu-id="2e378-108">Las aplicaciones pueden utilizar esta interfaz para registrar los errores de representación en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2e378-108">Applications can use this interface to log rendering errors at run time.</span></span> <span data-ttu-id="2e378-109">Implemente la interfaz [**IAMErrorLog**](iamerrorlog.md) en la aplicación y, a continuación, llame al método de [**\_ ErrorLog IAMSetErrorLog::p UT**](iamseterrorlog-put-errorlog.md) en la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="2e378-109">Implement the [**IAMErrorLog**](iamerrorlog.md) interface in your application, and then call the [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) method on the timeline.</span></span>

<span data-ttu-id="2e378-110">Para obtener más información sobre el uso de esta interfaz, vea [registrar errores](logging-errors.md).</span><span class="sxs-lookup"><span data-stu-id="2e378-110">For more information on using this interface, see [Logging Errors](logging-errors.md).</span></span>

## <a name="members"></a><span data-ttu-id="2e378-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="2e378-111">Members</span></span>

<span data-ttu-id="2e378-112">La interfaz **IAMSetErrorLog** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2e378-112">The **IAMSetErrorLog** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2e378-113">**IAMSetErrorLog** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2e378-113">**IAMSetErrorLog** also has these types of members:</span></span>

-   [<span data-ttu-id="2e378-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="2e378-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2e378-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="2e378-115">Methods</span></span>

<span data-ttu-id="2e378-116">La interfaz **IAMSetErrorLog** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2e378-116">The **IAMSetErrorLog** interface has these methods.</span></span>



| <span data-ttu-id="2e378-117">Método</span><span class="sxs-lookup"><span data-stu-id="2e378-117">Method</span></span>                                               | <span data-ttu-id="2e378-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e378-118">Description</span></span>                                                 |
|:-----------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="2e378-119">**obtener \_ ErrorLog**</span><span class="sxs-lookup"><span data-stu-id="2e378-119">**get\_ErrorLog**</span></span>](iamseterrorlog-get-errorlog.md) | <span data-ttu-id="2e378-120">Recupera el registro de errores actual de este objeto.</span><span class="sxs-lookup"><span data-stu-id="2e378-120">Retrieves the current error log for this object.</span></span><br/> |
| [<span data-ttu-id="2e378-121">**poner \_ ErrorLog**</span><span class="sxs-lookup"><span data-stu-id="2e378-121">**put\_ErrorLog**</span></span>](iamseterrorlog-put-errorlog.md) | <span data-ttu-id="2e378-122">Especifica un registro de errores para el objeto.</span><span class="sxs-lookup"><span data-stu-id="2e378-122">Specifies an error log for the object.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="2e378-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e378-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2e378-124">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="2e378-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2e378-125">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2e378-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2e378-126">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2e378-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2e378-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e378-127">Requirements</span></span>



| <span data-ttu-id="2e378-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e378-128">Requirement</span></span> | <span data-ttu-id="2e378-129">Value</span><span class="sxs-lookup"><span data-stu-id="2e378-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e378-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e378-130">Header</span></span><br/>  | <dl> <span data-ttu-id="2e378-131"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e378-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2e378-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e378-132">Library</span></span><br/> | <dl> <span data-ttu-id="2e378-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e378-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
