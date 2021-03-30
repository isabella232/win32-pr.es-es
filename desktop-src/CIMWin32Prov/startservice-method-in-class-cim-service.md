---
description: El método StartService pone el servicio en estado Iniciado.
ms.assetid: 0f2880ed-1643-4211-8684-12493711b1f8
ms.tgt_platform: multiple
title: Método StartService de la clase CIM_Service (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1592552595c06ec7111041cbb1c1b1d2628f8b6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807465"
---
# <a name="startservice-method-of-the-cim_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="32e6a-103">Método StartService de la clase CIM_Service (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="32e6a-103">StartService method of the CIM_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="32e6a-104">El método **StartService** pone el servicio en estado Iniciado.</span><span class="sxs-lookup"><span data-stu-id="32e6a-104">The **StartService** method puts the service in a started state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32e6a-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="32e6a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="32e6a-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="32e6a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="32e6a-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="32e6a-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="32e6a-108">Para obtener más información sobre el uso de este método, vea [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="32e6a-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="32e6a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32e6a-109">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="32e6a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32e6a-110">Parameters</span></span>

<span data-ttu-id="32e6a-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="32e6a-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="32e6a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32e6a-112">Return value</span></span>

<span data-ttu-id="32e6a-113">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="32e6a-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="32e6a-114">En una subclase, el conjunto de códigos de retorno posibles se puede especificar mediante un calificador **ValueMap** en el método.</span><span class="sxs-lookup"><span data-stu-id="32e6a-114">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="32e6a-115">Las cadenas a las que se traduce el contenido **ValueMap** también se pueden especificar en la subclase como calificador de matriz **Values** .</span><span class="sxs-lookup"><span data-stu-id="32e6a-115">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="32e6a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32e6a-116">Remarks</span></span>

<span data-ttu-id="32e6a-117">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="32e6a-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="32e6a-118">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="32e6a-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="32e6a-119">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="32e6a-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="32e6a-120">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="32e6a-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="32e6a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32e6a-121">Requirements</span></span>



| <span data-ttu-id="32e6a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="32e6a-122">Requirement</span></span> | <span data-ttu-id="32e6a-123">Value</span><span class="sxs-lookup"><span data-stu-id="32e6a-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32e6a-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32e6a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="32e6a-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32e6a-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="32e6a-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32e6a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="32e6a-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32e6a-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="32e6a-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="32e6a-128">Namespace</span></span><br/>                | <span data-ttu-id="32e6a-129">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="32e6a-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="32e6a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="32e6a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32e6a-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32e6a-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="32e6a-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="32e6a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32e6a-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32e6a-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32e6a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="32e6a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32e6a-135">\_Servicio CIM</span><span class="sxs-lookup"><span data-stu-id="32e6a-135">CIM\_Service</span></span>](startservice-method-in-class-cim-service.md)
</dt> <dt>

[<span data-ttu-id="32e6a-136">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="32e6a-136">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

