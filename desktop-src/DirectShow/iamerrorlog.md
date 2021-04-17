---
description: La interfaz IAMErrorLog proporciona un método de devolución de llamada para el registro de errores en los servicios de edición de DirectShow (DES). DES no implementa esta interfaz.
ms.assetid: d5366072-2de7-437c-b198-cbc4d8623c45
title: Interfaz IAMErrorLog (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48a1515ebf3e7c829a3e23772f1f84ee76c36ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679396"
---
# <a name="iamerrorlog-interface"></a><span data-ttu-id="d7859-103">Interfaz IAMErrorLog</span><span class="sxs-lookup"><span data-stu-id="d7859-103">IAMErrorLog interface</span></span>

> [!Note]  
> <span data-ttu-id="d7859-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="d7859-104">\[Deprecated.</span></span> <span data-ttu-id="d7859-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d7859-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d7859-106">La `IAMErrorLog` interfaz proporciona un método de devolución de llamada para el registro de errores en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="d7859-106">The `IAMErrorLog` interface provides a callback method for error logging in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="d7859-107">DES no implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="d7859-107">DES does not implement this interface.</span></span> <span data-ttu-id="d7859-108">Para realizar el registro de errores, implemente esta interfaz en la aplicación y llame a [**IAMSetErrorLog::p \_ ErrorLog UT**](iamseterrorlog-put-errorlog.md) en la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="d7859-108">To perform error logging, implement this interface in your application and call [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) on the timeline.</span></span> <span data-ttu-id="d7859-109">Si se produce un error al representar el proyecto, DES llamará al método [**IAMErrorLog:: LogError**](iamerrorlog-logerror.md) implementado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d7859-109">If an error occurs when you render the project, DES will call the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method implemented by your application.</span></span>

<span data-ttu-id="d7859-110">DES registra los errores solo cuando se representa un proyecto mediante la interfaz [**IRenderEngine**](irenderengine.md) .</span><span class="sxs-lookup"><span data-stu-id="d7859-110">DES logs errors only when you render a project using the [**IRenderEngine**](irenderengine.md) interface.</span></span> <span data-ttu-id="d7859-111">Por ejemplo, si guarda un proyecto como un gráfico de filtros de DirectShow (formato. GRF) y reproduce el archivo de gráfico, no hay ningún registro de errores.</span><span class="sxs-lookup"><span data-stu-id="d7859-111">For example, if you save a project as a DirectShow filter graph (.grf format) and play the graph file, there is no error logging.</span></span> <span data-ttu-id="d7859-112">Para obtener más información sobre el uso de esta interfaz, vea [registrar errores](logging-errors.md).</span><span class="sxs-lookup"><span data-stu-id="d7859-112">For more information on using this interface, see [Logging Errors](logging-errors.md).</span></span>

## <a name="members"></a><span data-ttu-id="d7859-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="d7859-113">Members</span></span>

<span data-ttu-id="d7859-114">La interfaz **IAMErrorLog** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d7859-114">The **IAMErrorLog** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d7859-115">**IAMErrorLog** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d7859-115">**IAMErrorLog** also has these types of members:</span></span>

-   [<span data-ttu-id="d7859-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="d7859-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d7859-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="d7859-117">Methods</span></span>

<span data-ttu-id="d7859-118">La interfaz **IAMErrorLog** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d7859-118">The **IAMErrorLog** interface has these methods.</span></span>



| <span data-ttu-id="d7859-119">Método</span><span class="sxs-lookup"><span data-stu-id="d7859-119">Method</span></span>                                   | <span data-ttu-id="d7859-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7859-120">Description</span></span>               |
|:-----------------------------------------|:--------------------------|
| [<span data-ttu-id="d7859-121">**LogError**</span><span class="sxs-lookup"><span data-stu-id="d7859-121">**LogError**</span></span>](iamerrorlog-logerror.md) | <span data-ttu-id="d7859-122">Registra un error.</span><span class="sxs-lookup"><span data-stu-id="d7859-122">Logs an error.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d7859-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7859-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d7859-124">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="d7859-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d7859-125">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d7859-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d7859-126">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d7859-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d7859-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7859-127">Requirements</span></span>



| <span data-ttu-id="d7859-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7859-128">Requirement</span></span> | <span data-ttu-id="d7859-129">Value</span><span class="sxs-lookup"><span data-stu-id="d7859-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7859-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7859-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d7859-131"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7859-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d7859-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7859-132">Library</span></span><br/> | <dl> <span data-ttu-id="d7859-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7859-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
