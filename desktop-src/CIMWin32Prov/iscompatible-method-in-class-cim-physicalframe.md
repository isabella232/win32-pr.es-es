---
description: Comprueba si el paquete físico al que se hace referencia puede estar contenido o insertado en el paquete físico.
ms.assetid: 8102569d-a956-445a-ae42-23eb206ba224
ms.tgt_platform: multiple
title: Método IsCompatible de la clase CIM_PhysicalFrame
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalFrame.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 121405e66a9361e832f6accb24ca6e303bb8e280
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998226"
---
# <a name="iscompatible-method-of-the-cim_physicalframe-class"></a><span data-ttu-id="a5d33-103">Método IsCompatible de la \_ clase PhysicalFrame de CIM</span><span class="sxs-lookup"><span data-stu-id="a5d33-103">IsCompatible method of the CIM\_PhysicalFrame class</span></span>

<span data-ttu-id="a5d33-104">El método **IsCompatible** comprueba si el paquete físico al que se hace referencia puede estar contenido o insertado en el paquete físico.</span><span class="sxs-lookup"><span data-stu-id="a5d33-104">The **IsCompatible** method verifies whether the referenced physical frame can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="a5d33-105">En una subclase, el conjunto de códigos de retorno posibles se puede especificar mediante un calificador **ValueMap** en el método.</span><span class="sxs-lookup"><span data-stu-id="a5d33-105">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="a5d33-106">Las cadenas a las que se traduce el contenido **ValueMap** también se pueden especificar en la subclase como calificador de matriz **Values** .</span><span class="sxs-lookup"><span data-stu-id="a5d33-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="a5d33-107">Este método se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="a5d33-107">This method is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5d33-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="a5d33-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a5d33-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a5d33-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a5d33-110">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="a5d33-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a5d33-111">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a5d33-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5d33-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5d33-112">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="a5d33-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5d33-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5d33-114">*ElementToCheck* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a5d33-114">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5d33-115">Referencia al elemento físico en el que se ejecuta el método **IsCompatible** .</span><span class="sxs-lookup"><span data-stu-id="a5d33-115">Reference to the physical element that the **IsCompatible** method runs against.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5d33-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5d33-116">Return value</span></span>

<span data-ttu-id="a5d33-117">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="a5d33-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5d33-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5d33-118">Remarks</span></span>

<span data-ttu-id="a5d33-119">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="a5d33-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a5d33-120">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="a5d33-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a5d33-121">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="a5d33-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a5d33-122">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="a5d33-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5d33-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5d33-123">Requirements</span></span>



| <span data-ttu-id="a5d33-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5d33-124">Requirement</span></span> | <span data-ttu-id="a5d33-125">Value</span><span class="sxs-lookup"><span data-stu-id="a5d33-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d33-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5d33-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a5d33-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5d33-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a5d33-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5d33-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a5d33-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5d33-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a5d33-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a5d33-130">Namespace</span></span><br/>                | <span data-ttu-id="a5d33-131">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a5d33-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a5d33-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a5d33-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5d33-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5d33-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5d33-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a5d33-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5d33-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5d33-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5d33-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5d33-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5d33-137">**\_PHYSICALFRAME CIM**</span><span class="sxs-lookup"><span data-stu-id="a5d33-137">**CIM\_PhysicalFrame**</span></span>](iscompatible-method-in-class-cim-physicalframe.md)
</dt> <dt>

[<span data-ttu-id="a5d33-138">**\_PHYSICALFRAME CIM**</span><span class="sxs-lookup"><span data-stu-id="a5d33-138">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> </dl>

 

