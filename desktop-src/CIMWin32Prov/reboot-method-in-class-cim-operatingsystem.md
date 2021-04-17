---
description: El método de reinicio solicita un reinicio del sistema operativo.
ms.assetid: 2ce766dd-51a4-4ffb-a45a-40399f1110f6
ms.tgt_platform: multiple
title: Método de reinicio de la clase CIM_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e498dd16372503b23aa56471224faf4d5d0ff012
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659328"
---
# <a name="reboot-method-of-the-cim_operatingsystem-class"></a><span data-ttu-id="c8da0-103">Método de reinicio de la \_ clase CIM OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="c8da0-103">Reboot method of the CIM\_OperatingSystem class</span></span>

<span data-ttu-id="c8da0-104">El método de **reinicio** solicita un reinicio del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c8da0-104">The **Reboot** method requests a reboot of the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8da0-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="c8da0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c8da0-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c8da0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c8da0-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c8da0-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c8da0-108">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c8da0-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c8da0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8da0-109">Syntax</span></span>


```mof
uint32 Reboot();
```



## <a name="parameters"></a><span data-ttu-id="c8da0-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8da0-110">Parameters</span></span>

<span data-ttu-id="c8da0-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c8da0-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8da0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8da0-112">Return value</span></span>

<span data-ttu-id="c8da0-113">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="c8da0-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8da0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8da0-114">Remarks</span></span>

<span data-ttu-id="c8da0-115">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="c8da0-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c8da0-116">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="c8da0-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c8da0-117">Para las clases WMI que se derivan de [**CIM \_ OperatingSystem**](cim-operatingsystem.md), consulte [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c8da0-117">For WMI classes that are derived from [**CIM\_OperatingSystem**](cim-operatingsystem.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c8da0-118">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="c8da0-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c8da0-119">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="c8da0-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="c8da0-120">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="c8da0-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c8da0-121">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="c8da0-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8da0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8da0-122">Requirements</span></span>



| <span data-ttu-id="c8da0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8da0-123">Requirement</span></span> | <span data-ttu-id="c8da0-124">Value</span><span class="sxs-lookup"><span data-stu-id="c8da0-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8da0-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8da0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c8da0-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8da0-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c8da0-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8da0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c8da0-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8da0-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c8da0-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c8da0-129">Namespace</span></span><br/>                | <span data-ttu-id="c8da0-130">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c8da0-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c8da0-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c8da0-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8da0-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8da0-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8da0-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8da0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8da0-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8da0-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8da0-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8da0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8da0-136">OperatingSystem de CIM \_</span><span class="sxs-lookup"><span data-stu-id="c8da0-136">CIM\_OperatingSystem</span></span>](reboot-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="c8da0-137">**OperatingSystem de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="c8da0-137">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> </dl>

 

