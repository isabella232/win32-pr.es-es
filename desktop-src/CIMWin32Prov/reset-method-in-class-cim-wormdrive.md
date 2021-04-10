---
description: El método Reset de la \_ clase WORMDrive de CIM solicita un restablecimiento del dispositivo lógico.
ms.assetid: ece4a618-6748-45a7-90fe-34eccf0f59d7
ms.tgt_platform: multiple
title: Método Reset de la clase CIM_WORMDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WORMDrive.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4fa05b36a1d5cb1d21c4fe53ecebc1fa87bc3991
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153496"
---
# <a name="reset-method-of-the-cim_wormdrive-class"></a><span data-ttu-id="7c42f-103">Método Reset de la \_ clase WORMDrive de CIM</span><span class="sxs-lookup"><span data-stu-id="7c42f-103">Reset method of the CIM\_WORMDrive class</span></span>

<span data-ttu-id="7c42f-104">El método **RESET** de la clase \_ [**WORMDrive**](cim-wormdrive.md) de CIM solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7c42f-104">The **Reset** method of the CIM\_[**WORMDrive**](cim-wormdrive.md) class requests a reset of the logical device.</span></span> <span data-ttu-id="7c42f-105">Este método se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7c42f-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7c42f-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="7c42f-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7c42f-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7c42f-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7c42f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c42f-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="7c42f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c42f-109">Parameters</span></span>

<span data-ttu-id="7c42f-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7c42f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c42f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c42f-111">Return value</span></span>

<span data-ttu-id="7c42f-112">Devuelve 0 (cero) si la solicitud se ejecutó correctamente, 1 (uno) si no se admite la solicitud y otro valor si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="7c42f-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c42f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c42f-113">Remarks</span></span>

<span data-ttu-id="7c42f-114">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="7c42f-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="7c42f-115">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="7c42f-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="7c42f-116">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="7c42f-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7c42f-117">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="7c42f-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c42f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c42f-118">Requirements</span></span>



| <span data-ttu-id="7c42f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c42f-119">Requirement</span></span> | <span data-ttu-id="7c42f-120">Value</span><span class="sxs-lookup"><span data-stu-id="7c42f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c42f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c42f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7c42f-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c42f-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7c42f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c42f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7c42f-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c42f-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7c42f-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7c42f-125">Namespace</span></span><br/>                | <span data-ttu-id="7c42f-126">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7c42f-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7c42f-127">MOF</span><span class="sxs-lookup"><span data-stu-id="7c42f-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c42f-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c42f-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c42f-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7c42f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c42f-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c42f-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c42f-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c42f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c42f-132">\_WORMDRIVE CIM</span><span class="sxs-lookup"><span data-stu-id="7c42f-132">CIM\_WORMDrive</span></span>](reset-method-in-class-cim-wormdrive.md)
</dt> <dt>

[<span data-ttu-id="7c42f-133">**\_WORMDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="7c42f-133">**CIM\_WORMDrive**</span></span>](cim-wormdrive.md)
</dt> </dl>

 

 




