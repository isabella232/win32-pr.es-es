---
description: El método Reset de la \_ clase MediaAccessDevice de CIM solicita un restablecimiento del dispositivo lógico.
ms.assetid: 89796284-3569-4ff0-873d-0c5ed58eaedc
ms.tgt_platform: multiple
title: Método Reset de la clase CIM_MediaAccessDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90dd391a32d36ea17bfbb20edd4e6394a85f38dd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003433"
---
# <a name="reset-method-of-the-cim_mediaaccessdevice-class"></a><span data-ttu-id="9f561-103">Método Reset de la \_ clase MediaAccessDevice de CIM</span><span class="sxs-lookup"><span data-stu-id="9f561-103">Reset method of the CIM\_MediaAccessDevice class</span></span>

<span data-ttu-id="9f561-104">El método **RESET** de la \_ clase MediaAccessDevice de CIM solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9f561-104">The **Reset** method of the CIM\_MediaAccessDevice class requests a reset of the logical device.</span></span> <span data-ttu-id="9f561-105">Este método se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f561-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f561-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="9f561-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9f561-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9f561-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9f561-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f561-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="9f561-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f561-109">Parameters</span></span>

<span data-ttu-id="9f561-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9f561-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f561-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f561-111">Return value</span></span>

<span data-ttu-id="9f561-112">Devuelve 0 (cero) si la solicitud se ejecutó correctamente, 1 (uno) si no se admite la solicitud y otro valor si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="9f561-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f561-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f561-113">Remarks</span></span>

<span data-ttu-id="9f561-114">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="9f561-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="9f561-115">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="9f561-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="9f561-116">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="9f561-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9f561-117">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="9f561-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f561-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f561-118">Requirements</span></span>



| <span data-ttu-id="9f561-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f561-119">Requirement</span></span> | <span data-ttu-id="9f561-120">Value</span><span class="sxs-lookup"><span data-stu-id="9f561-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f561-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f561-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9f561-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f561-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9f561-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f561-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9f561-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f561-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9f561-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9f561-125">Namespace</span></span><br/>                | <span data-ttu-id="9f561-126">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9f561-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9f561-127">MOF</span><span class="sxs-lookup"><span data-stu-id="9f561-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f561-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f561-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f561-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9f561-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f561-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f561-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f561-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f561-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f561-132">\_MEDIAACCESSDEVICE CIM</span><span class="sxs-lookup"><span data-stu-id="9f561-132">CIM\_MediaAccessDevice</span></span>](reset-method-in-class-cim-mediaaccessdevice.md)
</dt> <dt>

[<span data-ttu-id="9f561-133">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="9f561-133">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

 




