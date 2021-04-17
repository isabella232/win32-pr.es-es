---
description: La interfaz ITQOSApplicationID expone un método que permite a una aplicación obtener el identificador de QOS de la llamada actual.
ms.assetid: 1df50b3a-bd16-4e9b-afca-b025bfe537a4
title: Interfaz ITQOSApplicationID (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23df8da80798cc52ecd73b4f29288812f3774d9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681237"
---
# <a name="itqosapplicationid-interface"></a><span data-ttu-id="4f148-103">Interfaz ITQOSApplicationID</span><span class="sxs-lookup"><span data-stu-id="4f148-103">ITQOSApplicationID interface</span></span>

<span data-ttu-id="4f148-104">\[ Esta interfaz no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4f148-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4f148-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="4f148-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4f148-106">La interfaz **ITQOSApplicationID** expone un método que permite a una aplicación obtener el identificador de QoS de la llamada actual.</span><span class="sxs-lookup"><span data-stu-id="4f148-106">The **ITQOSApplicationID** interface exposes a method that allows an application to get the QOS identifier for the current call.</span></span>

<span data-ttu-id="4f148-107">Esta interfaz se implementa mediante el [MSP de IPConf](ipconf-msp.md) y solo se expone cuando una llamada usa conferencias IP.</span><span class="sxs-lookup"><span data-stu-id="4f148-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and is exposed only when a call uses IP Conferencing.</span></span>

## <a name="members"></a><span data-ttu-id="4f148-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4f148-108">Members</span></span>

<span data-ttu-id="4f148-109">La interfaz **ITQOSApplicationID** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="4f148-109">The **ITQOSApplicationID** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="4f148-110">**ITQOSApplicationID** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4f148-110">**ITQOSApplicationID** also has these types of members:</span></span>

-   [<span data-ttu-id="4f148-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4f148-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4f148-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4f148-112">Methods</span></span>

<span data-ttu-id="4f148-113">La interfaz **ITQOSApplicationID** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4f148-113">The **ITQOSApplicationID** interface has these methods.</span></span>



| <span data-ttu-id="4f148-114">Método</span><span class="sxs-lookup"><span data-stu-id="4f148-114">Method</span></span>                                                                | <span data-ttu-id="4f148-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f148-115">Description</span></span>                         |
|:----------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="4f148-116">**SetQOSApplicationID**</span><span class="sxs-lookup"><span data-stu-id="4f148-116">**SetQOSApplicationID**</span></span>](itqosapplicationid-setqosapplicationid.md) | <span data-ttu-id="4f148-117">Establece el identificador de QOS.</span><span class="sxs-lookup"><span data-stu-id="4f148-117">Sets the QOS identifier.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4f148-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f148-118">Requirements</span></span>



| <span data-ttu-id="4f148-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f148-119">Requirement</span></span> | <span data-ttu-id="4f148-120">Value</span><span class="sxs-lookup"><span data-stu-id="4f148-120">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4f148-121">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="4f148-121">TAPI version</span></span><br/> | <span data-ttu-id="4f148-122">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="4f148-122">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="4f148-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f148-123">Header</span></span><br/>       | <dl> <span data-ttu-id="4f148-124"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f148-124"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f148-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f148-125">Library</span></span><br/>      | <dl> <span data-ttu-id="4f148-126"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f148-126"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="4f148-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4f148-127">DLL</span></span><br/>          | <dl> <span data-ttu-id="4f148-128"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f148-128"><dt>Tapi3.dll</dt></span></span> </dl> |



 

