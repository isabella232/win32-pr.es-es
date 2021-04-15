---
description: El método Reset de la \_ clase AlarmDevice de CIM solicita un restablecimiento del dispositivo lógico. Este método se hereda del LogicalDevice de CIM \_ .
ms.assetid: e70718c5-2c80-4084-b233-b3e4d083e7b4
ms.tgt_platform: multiple
title: Método Reset de la clase CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 442cac28c094e60c978099c2337076fd8f2df980
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496546"
---
# <a name="reset-method-of-the-cim_alarmdevice-class"></a><span data-ttu-id="99732-104">Método Reset de la \_ clase AlarmDevice de CIM</span><span class="sxs-lookup"><span data-stu-id="99732-104">Reset method of the CIM\_AlarmDevice class</span></span>

<span data-ttu-id="99732-105">El método **RESET** de la [**clase \_ AlarmDevice de CIM**](cim-alarmdevice.md) solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="99732-105">The **Reset** method of the [**CIM\_AlarmDevice**](cim-alarmdevice.md) class requests a logical device reset.</span></span> <span data-ttu-id="99732-106">Este método se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="99732-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="99732-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="99732-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="99732-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="99732-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="99732-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99732-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="99732-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99732-110">Parameters</span></span>

<span data-ttu-id="99732-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="99732-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="99732-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99732-112">Return value</span></span>

<span data-ttu-id="99732-113">Devuelve 0 (cero) si la solicitud se ejecutó correctamente, 1 (uno) si no se admite la solicitud y otro valor si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="99732-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="99732-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99732-114">Remarks</span></span>

<span data-ttu-id="99732-115">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="99732-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="99732-116">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="99732-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="99732-117">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="99732-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="99732-118">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="99732-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="99732-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99732-119">Requirements</span></span>



| <span data-ttu-id="99732-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="99732-120">Requirement</span></span> | <span data-ttu-id="99732-121">Value</span><span class="sxs-lookup"><span data-stu-id="99732-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99732-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99732-122">Minimum supported client</span></span><br/> | <span data-ttu-id="99732-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99732-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="99732-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99732-124">Minimum supported server</span></span><br/> | <span data-ttu-id="99732-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99732-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="99732-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="99732-126">Namespace</span></span><br/>                | <span data-ttu-id="99732-127">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="99732-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="99732-128">MOF</span><span class="sxs-lookup"><span data-stu-id="99732-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99732-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="99732-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="99732-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="99732-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99732-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99732-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99732-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="99732-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99732-133">\_ALARMDEVICE CIM</span><span class="sxs-lookup"><span data-stu-id="99732-133">CIM\_AlarmDevice</span></span>](reset-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[<span data-ttu-id="99732-134">**\_ALARMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="99732-134">**CIM\_AlarmDevice**</span></span>](cim-alarmdevice.md)
</dt> </dl>

 

 




