---
description: El método Invoke de la \_ clase CIM DiskSpaceCheck evalúa una comprobación determinada. Los detalles de cómo evalúa el método una comprobación determinada en un contexto CIM se describen en la subclase de comprobación CIM no abstracta \_ .
ms.assetid: 1f06b0c4-3f39-4a6f-9205-2aa309fb06bb
ms.tgt_platform: multiple
title: Método Invoke de la clase CIM_DiskSpaceCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskSpaceCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bbcef752bf412ea255891dd0f5abdf7563f0e078
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659469"
---
# <a name="invoke-method-of-the-cim_diskspacecheck-class"></a><span data-ttu-id="5edd2-104">Método Invoke de la \_ clase CIM DiskSpaceCheck</span><span class="sxs-lookup"><span data-stu-id="5edd2-104">Invoke method of the CIM\_DiskSpaceCheck class</span></span>

<span data-ttu-id="5edd2-105">El método **Invoke** de la clase [**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md) evalúa una comprobación determinada.</span><span class="sxs-lookup"><span data-stu-id="5edd2-105">The **Invoke** method of the [**CIM\_DiskSpaceCheck**](cim-diskspacecheck.md) class evaluates a particular check.</span></span> <span data-ttu-id="5edd2-106">Los detalles de cómo evalúa el método una comprobación determinada en un contexto CIM se describen en la subclase de [**\_ comprobación CIM**](cim-check.md) no abstracta.</span><span class="sxs-lookup"><span data-stu-id="5edd2-106">The details of how the method evaluates a particular check in a CIM context is described by the non-abstract [**CIM\_Check**](cim-check.md) subclass.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5edd2-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="5edd2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5edd2-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5edd2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5edd2-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="5edd2-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5edd2-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5edd2-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5edd2-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5edd2-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="5edd2-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5edd2-112">Parameters</span></span>

<span data-ttu-id="5edd2-113">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5edd2-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5edd2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5edd2-114">Return value</span></span>

<span data-ttu-id="5edd2-115">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="5edd2-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="5edd2-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5edd2-116">Remarks</span></span>

<span data-ttu-id="5edd2-117">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="5edd2-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="5edd2-118">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="5edd2-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="5edd2-119">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="5edd2-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5edd2-120">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="5edd2-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5edd2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5edd2-121">Requirements</span></span>



| <span data-ttu-id="5edd2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5edd2-122">Requirement</span></span> | <span data-ttu-id="5edd2-123">Value</span><span class="sxs-lookup"><span data-stu-id="5edd2-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5edd2-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5edd2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5edd2-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5edd2-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5edd2-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5edd2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5edd2-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5edd2-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5edd2-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5edd2-128">Namespace</span></span><br/>                | <span data-ttu-id="5edd2-129">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5edd2-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5edd2-130">MOF</span><span class="sxs-lookup"><span data-stu-id="5edd2-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5edd2-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5edd2-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5edd2-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5edd2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5edd2-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5edd2-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5edd2-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="5edd2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5edd2-135">\_DISKSPACECHECK CIM</span><span class="sxs-lookup"><span data-stu-id="5edd2-135">CIM\_DiskSpaceCheck</span></span>](invoke-method-in-class-cim-diskspacecheck.md)
</dt> <dt>

[<span data-ttu-id="5edd2-136">**\_DISKSPACECHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="5edd2-136">**CIM\_DiskSpaceCheck**</span></span>](cim-diskspacecheck.md)
</dt> </dl>

 

