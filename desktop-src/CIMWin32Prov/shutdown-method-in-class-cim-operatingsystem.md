---
description: El método Shutdown solicita el apagado del sistema operativo.
ms.assetid: f2a2a98b-2f4f-4aa1-9f54-515660273c8d
ms.tgt_platform: multiple
title: Método Shutdown de la clase CIM_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78a11f325b8682b0024ff281a48989b837d3073a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906984"
---
# <a name="shutdown-method-of-the-cim_operatingsystem-class"></a><span data-ttu-id="30f2d-103">Método Shutdown de la \_ clase CIM OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="30f2d-103">Shutdown method of the CIM\_OperatingSystem class</span></span>

<span data-ttu-id="30f2d-104">El método **Shutdown** solicita el apagado del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="30f2d-104">The **Shutdown** method requests a shutdown of the operating system.</span></span> <span data-ttu-id="30f2d-105">La implementación o subclase del sistema operativo puede establecer dependencias entre los métodos de **apagado** y [**reinicio**](reboot-method-in-class-cim-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="30f2d-105">The implementation or subclass of the operating system can establish dependencies between the **Shutdown** and [**Reboot**](reboot-method-in-class-cim-operatingsystem.md) methods.</span></span> <span data-ttu-id="30f2d-106">Por ejemplo, se pueden proporcionar capacidades más sofisticadas, como un apagado programado y un reinicio.</span><span class="sxs-lookup"><span data-stu-id="30f2d-106">For example, more sophisticated capabilities can be provided, such as a scheduled shutdown and reboot.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="30f2d-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="30f2d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="30f2d-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="30f2d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="30f2d-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="30f2d-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="30f2d-110">Para obtener más información sobre el uso de este método, vea [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="30f2d-110">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="30f2d-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30f2d-111">Syntax</span></span>


```mof
uint32 Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="30f2d-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30f2d-112">Parameters</span></span>

<span data-ttu-id="30f2d-113">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="30f2d-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="30f2d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30f2d-114">Return value</span></span>

<span data-ttu-id="30f2d-115">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="30f2d-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="30f2d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30f2d-116">Remarks</span></span>

<span data-ttu-id="30f2d-117">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="30f2d-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="30f2d-118">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="30f2d-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="30f2d-119">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="30f2d-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="30f2d-120">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="30f2d-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="30f2d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30f2d-121">Requirements</span></span>



| <span data-ttu-id="30f2d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="30f2d-122">Requirement</span></span> | <span data-ttu-id="30f2d-123">Value</span><span class="sxs-lookup"><span data-stu-id="30f2d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30f2d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30f2d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="30f2d-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30f2d-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="30f2d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30f2d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="30f2d-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30f2d-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="30f2d-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="30f2d-128">Namespace</span></span><br/>                | <span data-ttu-id="30f2d-129">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="30f2d-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="30f2d-130">MOF</span><span class="sxs-lookup"><span data-stu-id="30f2d-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30f2d-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30f2d-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="30f2d-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="30f2d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30f2d-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30f2d-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30f2d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="30f2d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f2d-135">OperatingSystem de CIM \_</span><span class="sxs-lookup"><span data-stu-id="30f2d-135">CIM\_OperatingSystem</span></span>](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="30f2d-136">**OperatingSystem de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="30f2d-136">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> </dl>

 

