---
description: El método Reset de la \_ clase PCVideoController de CIM solicita un restablecimiento del dispositivo lógico.
ms.assetid: 0dbed7af-6c7a-4bbb-b1ae-d768d2f88697
ms.tgt_platform: multiple
title: Método Reset de la clase CIM_PCVideoController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCVideoController.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b156f4c440e98ebc51618ca8350696f23b55074b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659571"
---
# <a name="reset-method-of-the-cim_pcvideocontroller-class"></a><span data-ttu-id="8aa97-103">Método Reset de la \_ clase PCVideoController de CIM</span><span class="sxs-lookup"><span data-stu-id="8aa97-103">Reset method of the CIM\_PCVideoController class</span></span>

<span data-ttu-id="8aa97-104">El método **RESET** de la \_ clase PCVideoController de CIM solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8aa97-104">The **Reset** method of the CIM\_PCVideoController class requests a reset of the logical device.</span></span> <span data-ttu-id="8aa97-105">Este método se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8aa97-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8aa97-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="8aa97-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8aa97-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8aa97-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8aa97-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8aa97-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="8aa97-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8aa97-109">Parameters</span></span>

<span data-ttu-id="8aa97-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8aa97-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8aa97-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8aa97-111">Return value</span></span>

<span data-ttu-id="8aa97-112">Devuelve 0 (cero) si la solicitud se ejecutó correctamente, 1 (uno) si no se admite la solicitud y otro valor si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="8aa97-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="8aa97-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8aa97-113">Remarks</span></span>

<span data-ttu-id="8aa97-114">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="8aa97-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8aa97-115">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="8aa97-115">To use this method, you must implement it in your own provider.</span></span> <span data-ttu-id="8aa97-116">Para las clases WMI derivadas de [**CIM \_ PCVideoController**](cim-pcvideocontroller.md), vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8aa97-116">For WMI classes derived from [**CIM\_PCVideoController**](cim-pcvideocontroller.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8aa97-117">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="8aa97-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8aa97-118">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="8aa97-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aa97-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8aa97-119">Requirements</span></span>



| <span data-ttu-id="8aa97-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aa97-120">Requirement</span></span> | <span data-ttu-id="8aa97-121">Value</span><span class="sxs-lookup"><span data-stu-id="8aa97-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8aa97-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8aa97-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8aa97-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8aa97-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8aa97-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8aa97-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8aa97-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8aa97-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8aa97-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8aa97-126">Namespace</span></span><br/>                | <span data-ttu-id="8aa97-127">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8aa97-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8aa97-128">MOF</span><span class="sxs-lookup"><span data-stu-id="8aa97-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8aa97-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8aa97-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8aa97-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8aa97-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8aa97-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8aa97-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aa97-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="8aa97-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aa97-133">\_PCVIDEOCONTROLLER CIM</span><span class="sxs-lookup"><span data-stu-id="8aa97-133">CIM\_PCVideoController</span></span>](reset-method-in-class-cim-pcvideocontroller.md)
</dt> <dt>

[<span data-ttu-id="8aa97-134">**\_PCVIDEOCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="8aa97-134">**CIM\_PCVideoController**</span></span>](cim-pcvideocontroller.md)
</dt> </dl>

 

 




