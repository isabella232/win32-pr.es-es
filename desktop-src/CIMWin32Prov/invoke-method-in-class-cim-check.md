---
description: El método Invoke de la \_ clase de comprobación CIM evalúa una comprobación determinada.
ms.assetid: cf1adeb2-f8a2-4f84-978f-e801bce104ac
ms.tgt_platform: multiple
title: Método Invoke de la clase CIM_Check
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Check.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7774fcd1b3ef451fffb34ce9ad10d404e8ea95b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659471"
---
# <a name="invoke-method-of-the-cim_check-class"></a><span data-ttu-id="f416e-103">Método Invoke de la \_ clase de comprobación CIM</span><span class="sxs-lookup"><span data-stu-id="f416e-103">Invoke method of the CIM\_Check class</span></span>

<span data-ttu-id="f416e-104">El método **Invoke** de la clase de [**\_ comprobación CIM**](cim-check.md) evalúa una comprobación determinada.</span><span class="sxs-lookup"><span data-stu-id="f416e-104">The **Invoke** method of the [**CIM\_Check**](cim-check.md) class evaluates a particular check.</span></span>

<span data-ttu-id="f416e-105">Para obtener más información sobre cómo el método evalúa una comprobación determinada en un contexto CIM, vea las subclases [**de \_ comprobación de CIM**](cim-check.md) no abstractas.</span><span class="sxs-lookup"><span data-stu-id="f416e-105">For more information about how the method evaluates a particular check in a CIM context, see the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f416e-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="f416e-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f416e-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f416e-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f416e-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f416e-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f416e-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f416e-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f416e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f416e-110">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="f416e-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f416e-111">Parameters</span></span>

<span data-ttu-id="f416e-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f416e-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f416e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f416e-113">Return value</span></span>

<span data-ttu-id="f416e-114">Devuelve un valor de 0 (cero) si se realiza correctamente, 1 (uno) si no se admite el método, y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="f416e-114">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f416e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f416e-115">Remarks</span></span>

<span data-ttu-id="f416e-116">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="f416e-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f416e-117">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="f416e-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f416e-118">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="f416e-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f416e-119">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="f416e-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f416e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f416e-120">Requirements</span></span>



| <span data-ttu-id="f416e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f416e-121">Requirement</span></span> | <span data-ttu-id="f416e-122">Value</span><span class="sxs-lookup"><span data-stu-id="f416e-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f416e-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f416e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f416e-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f416e-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f416e-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f416e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f416e-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f416e-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f416e-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f416e-127">Namespace</span></span><br/>                | <span data-ttu-id="f416e-128">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f416e-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f416e-129">MOF</span><span class="sxs-lookup"><span data-stu-id="f416e-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f416e-130"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f416e-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f416e-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f416e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f416e-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f416e-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f416e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f416e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f416e-134">**Comprobación de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="f416e-134">**CIM\_Check**</span></span>](invoke-method-in-class-cim-check.md)
</dt> <dt>

[<span data-ttu-id="f416e-135">**Comprobación de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="f416e-135">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

