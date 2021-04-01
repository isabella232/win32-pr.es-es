---
description: El método Invoke de la \_ clase CIM FileSpecification evalúa una comprobación determinada. Los detalles de cómo evalúa el método una comprobación determinada en un contexto CIM se describen en las subclases de comprobación CIM no abstractas \_ . Este método se hereda de la \_ comprobación CIM.
ms.assetid: cefb64b5-c06f-4775-a903-4e8a8b99a6ae
ms.tgt_platform: multiple
title: Método Invoke de la clase CIM_FileSpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileSpecification.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 725fa6f9e667f70a270754d2bc453acc4b695ca2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907132"
---
# <a name="invoke-method-of-the-cim_filespecification-class"></a><span data-ttu-id="f96bb-105">Método Invoke de la \_ clase CIM FileSpecification</span><span class="sxs-lookup"><span data-stu-id="f96bb-105">Invoke method of the CIM\_FileSpecification class</span></span>

<span data-ttu-id="f96bb-106">El método **Invoke** de la clase [**CIM \_ FileSpecification**](cim-filespecification.md) evalúa una comprobación determinada.</span><span class="sxs-lookup"><span data-stu-id="f96bb-106">The **Invoke** method of the [**CIM\_FileSpecification**](cim-filespecification.md) class evaluates a particular check.</span></span> <span data-ttu-id="f96bb-107">Los detalles de cómo evalúa el método una comprobación determinada en un contexto CIM se describen en las subclases [**de \_ comprobación CIM**](cim-check.md) no abstractas.</span><span class="sxs-lookup"><span data-stu-id="f96bb-107">Details of how the method evaluates a particular check in a CIM context are described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="f96bb-108">Este método se hereda de **la \_ comprobación CIM**.</span><span class="sxs-lookup"><span data-stu-id="f96bb-108">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f96bb-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="f96bb-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f96bb-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f96bb-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f96bb-111">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f96bb-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f96bb-112">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f96bb-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f96bb-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f96bb-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="f96bb-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f96bb-114">Parameters</span></span>

<span data-ttu-id="f96bb-115">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f96bb-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f96bb-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f96bb-116">Return value</span></span>

<span data-ttu-id="f96bb-117">Devuelve un valor de 0 (cero) si se realiza correctamente, 1 (uno) si no se admite el método, y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="f96bb-117">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f96bb-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f96bb-118">Remarks</span></span>

<span data-ttu-id="f96bb-119">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="f96bb-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f96bb-120">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="f96bb-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f96bb-121">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="f96bb-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f96bb-122">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="f96bb-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f96bb-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f96bb-123">Requirements</span></span>



| <span data-ttu-id="f96bb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f96bb-124">Requirement</span></span> | <span data-ttu-id="f96bb-125">Value</span><span class="sxs-lookup"><span data-stu-id="f96bb-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f96bb-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f96bb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f96bb-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f96bb-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f96bb-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f96bb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f96bb-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f96bb-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f96bb-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f96bb-130">Namespace</span></span><br/>                | <span data-ttu-id="f96bb-131">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f96bb-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f96bb-132">MOF</span><span class="sxs-lookup"><span data-stu-id="f96bb-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f96bb-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f96bb-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f96bb-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f96bb-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f96bb-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f96bb-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f96bb-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f96bb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f96bb-137">\_FILESPECIFICATION CIM</span><span class="sxs-lookup"><span data-stu-id="f96bb-137">CIM\_FileSpecification</span></span>](invoke-method-in-class-cim-filespecification.md)
</dt> <dt>

[<span data-ttu-id="f96bb-138">**\_FILESPECIFICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="f96bb-138">**CIM\_FileSpecification**</span></span>](cim-filespecification.md)
</dt> </dl>

 

