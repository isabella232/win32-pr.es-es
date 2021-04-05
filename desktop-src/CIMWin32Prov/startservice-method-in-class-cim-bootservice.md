---
description: El método StartService coloca el servicio en un &\# 0034; inicie&\# 0034; State.
ms.assetid: b2b38d64-b497-46f5-8638-a9a8ce50e888
ms.tgt_platform: multiple
title: Método StartService de la clase CIM_BootService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootService.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e7f7f56633319f9e009f58f7c06dde7a3baee8e5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000827"
---
# <a name="startservice-method-of-the-cim_bootservice-class"></a><span data-ttu-id="cee8d-103">Método StartService de la \_ clase BootService de CIM</span><span class="sxs-lookup"><span data-stu-id="cee8d-103">StartService method of the CIM\_BootService class</span></span>

<span data-ttu-id="cee8d-104">El método **StartService** pone el servicio en un estado de "Inicio".</span><span class="sxs-lookup"><span data-stu-id="cee8d-104">The **StartService** method puts the service in a "start" state.</span></span> <span data-ttu-id="cee8d-105">En una subclase, el conjunto de códigos de retorno posibles se puede especificar mediante un calificador **ValueMap** en el método.</span><span class="sxs-lookup"><span data-stu-id="cee8d-105">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="cee8d-106">Las cadenas a las que se traduce el contenido **ValueMap** también se pueden especificar en la subclase como calificador de matriz **Values** .</span><span class="sxs-lookup"><span data-stu-id="cee8d-106">The strings to which the **ValueMap** contents are translated may also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="cee8d-107">Este método se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="cee8d-107">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cee8d-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="cee8d-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cee8d-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cee8d-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cee8d-110">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="cee8d-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cee8d-111">Para obtener más información sobre el uso de este método, vea [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cee8d-111">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cee8d-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cee8d-112">Syntax</span></span>


```mof
Integer StartService();
```



## <a name="parameters"></a><span data-ttu-id="cee8d-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cee8d-113">Parameters</span></span>

<span data-ttu-id="cee8d-114">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cee8d-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cee8d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cee8d-115">Return value</span></span>

<span data-ttu-id="cee8d-116">Devuelve un valor de 0 (cero) si se realiza correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="cee8d-116">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="cee8d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cee8d-117">Remarks</span></span>

<span data-ttu-id="cee8d-118">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="cee8d-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="cee8d-119">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="cee8d-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="cee8d-120">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="cee8d-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cee8d-121">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="cee8d-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cee8d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cee8d-122">Requirements</span></span>



| <span data-ttu-id="cee8d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cee8d-123">Requirement</span></span> | <span data-ttu-id="cee8d-124">Value</span><span class="sxs-lookup"><span data-stu-id="cee8d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cee8d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cee8d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cee8d-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cee8d-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cee8d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cee8d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cee8d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cee8d-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cee8d-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cee8d-129">Namespace</span></span><br/>                | <span data-ttu-id="cee8d-130">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cee8d-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cee8d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="cee8d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cee8d-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cee8d-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cee8d-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cee8d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cee8d-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cee8d-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cee8d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="cee8d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cee8d-136">\_BOOTSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="cee8d-136">CIM\_BootService</span></span>](startservice-method-in-class-cim-bootservice.md)
</dt> <dt>

[<span data-ttu-id="cee8d-137">**\_BOOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="cee8d-137">**CIM\_BootService**</span></span>](cim-bootservice.md)
</dt> </dl>

 

