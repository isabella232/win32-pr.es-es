---
description: Comprueba si el elemento físico al que se hace referencia puede estar contenido o insertado en el paquete físico.
ms.assetid: 406aaa75-b48c-4377-adb5-e900676b6e36
ms.tgt_platform: multiple
title: Método IsCompatible de la clase CIM_PhysicalPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalPackage.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1957b8d0c1929ff6f7b4ef8c69fa55ea4ccc83b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659502"
---
# <a name="iscompatible-method-of-the-cim_physicalpackage-class"></a><span data-ttu-id="77bc4-103">Método IsCompatible de la \_ clase PhysicalPackage de CIM</span><span class="sxs-lookup"><span data-stu-id="77bc4-103">IsCompatible method of the CIM\_PhysicalPackage class</span></span>

<span data-ttu-id="77bc4-104">El método **IsCompatible** comprueba si el paquete físico al que se hace referencia puede estar contenido o insertado en el paquete físico.</span><span class="sxs-lookup"><span data-stu-id="77bc4-104">The **IsCompatible** method verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="77bc4-105">En una subclase, el conjunto de códigos de retorno posibles se puede especificar mediante un calificador **ValueMap** en el método.</span><span class="sxs-lookup"><span data-stu-id="77bc4-105">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="77bc4-106">Las cadenas a las que se traduce el contenido **ValueMap** también se pueden especificar en la subclase como calificador de matriz **Values** .</span><span class="sxs-lookup"><span data-stu-id="77bc4-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="77bc4-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="77bc4-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="77bc4-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="77bc4-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="77bc4-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="77bc4-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="77bc4-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="77bc4-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="77bc4-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77bc4-111">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="77bc4-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77bc4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77bc4-113">*ElementToCheck* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77bc4-113">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77bc4-114">Referencia al elemento físico en el que se ejecuta el método **IsCompatible** .</span><span class="sxs-lookup"><span data-stu-id="77bc4-114">Reference to the physical element that the **IsCompatible** method runs against.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77bc4-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77bc4-115">Return value</span></span>

<span data-ttu-id="77bc4-116">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="77bc4-116">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="77bc4-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77bc4-117">Remarks</span></span>

<span data-ttu-id="77bc4-118">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="77bc4-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="77bc4-119">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="77bc4-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="77bc4-120">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="77bc4-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="77bc4-121">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="77bc4-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="77bc4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77bc4-122">Requirements</span></span>



| <span data-ttu-id="77bc4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="77bc4-123">Requirement</span></span> | <span data-ttu-id="77bc4-124">Value</span><span class="sxs-lookup"><span data-stu-id="77bc4-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77bc4-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77bc4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="77bc4-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77bc4-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="77bc4-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77bc4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="77bc4-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77bc4-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="77bc4-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="77bc4-129">Namespace</span></span><br/>                | <span data-ttu-id="77bc4-130">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="77bc4-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="77bc4-131">MOF</span><span class="sxs-lookup"><span data-stu-id="77bc4-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77bc4-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77bc4-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="77bc4-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="77bc4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77bc4-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77bc4-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77bc4-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="77bc4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77bc4-136">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="77bc4-136">**CIM\_PhysicalPackage**</span></span>](iscompatible-method-in-class-cim-physicalpackage.md)
</dt> <dt>

[<span data-ttu-id="77bc4-137">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="77bc4-137">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 

