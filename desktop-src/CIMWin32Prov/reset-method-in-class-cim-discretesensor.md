---
description: 'Método reset de la CIM_DiscreteSensor : el método Reset solicita un restablecimiento del dispositivo lógico. Este método se hereda de CIM \_ LogicalDevice.'
ms.assetid: 4ddbad2a-e586-434a-a33e-7d60dcb67b3a
ms.tgt_platform: multiple
title: Método Reset de la CIM_DiscreteSensor clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiscreteSensor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: aecda4b40a70c72679c3edff7b30f6ba548938cf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096913"
---
# <a name="reset-method-of-the-cim_discretesensor-class"></a><span data-ttu-id="cf559-104">Método Reset de la clase \_ CIM DiscreteSensor</span><span class="sxs-lookup"><span data-stu-id="cf559-104">Reset method of the CIM\_DiscreteSensor class</span></span>

<span data-ttu-id="cf559-105">El **método Reset** solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cf559-105">The **Reset** method requests a reset of the logical device.</span></span> <span data-ttu-id="cf559-106">Este método se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cf559-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf559-107">Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI.</span><span class="sxs-lookup"><span data-stu-id="cf559-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cf559-108">WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cf559-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="cf559-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf559-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="cf559-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf559-110">Parameters</span></span>

<span data-ttu-id="cf559-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cf559-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf559-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf559-112">Return value</span></span>

<span data-ttu-id="cf559-113">Devuelve 0 (cero) si la solicitud se ejecutó correctamente, 1 (uno) si no se admite la solicitud y algún otro valor si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="cf559-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf559-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cf559-114">Remarks</span></span>

<span data-ttu-id="cf559-115">Wmi no implementa actualmente este método.</span><span class="sxs-lookup"><span data-stu-id="cf559-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="cf559-116">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="cf559-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="cf559-117">Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf.</span><span class="sxs-lookup"><span data-stu-id="cf559-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cf559-118">Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="cf559-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf559-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf559-119">Requirements</span></span>



| <span data-ttu-id="cf559-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf559-120">Requirement</span></span> | <span data-ttu-id="cf559-121">Valor</span><span class="sxs-lookup"><span data-stu-id="cf559-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf559-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf559-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cf559-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf559-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cf559-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf559-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cf559-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf559-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cf559-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cf559-126">Namespace</span></span><br/>                | <span data-ttu-id="cf559-127">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="cf559-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cf559-128">MOF</span><span class="sxs-lookup"><span data-stu-id="cf559-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf559-129"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf559-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf559-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cf559-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf559-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf559-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf559-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cf559-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf559-133">CIM \_ DiscreteSensor</span><span class="sxs-lookup"><span data-stu-id="cf559-133">CIM\_DiscreteSensor</span></span>](reset-method-in-class-cim-discretesensor.md)
</dt> <dt>

[<span data-ttu-id="cf559-134">**CIM \_ DiscreteSensor**</span><span class="sxs-lookup"><span data-stu-id="cf559-134">**CIM\_DiscreteSensor**</span></span>](cim-discretesensor.md)
</dt> </dl>

 

 




