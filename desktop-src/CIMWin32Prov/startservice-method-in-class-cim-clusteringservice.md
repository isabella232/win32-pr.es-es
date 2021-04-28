---
description: 'Método StartService de la CIM_ClusteringService : el método StartService coloca el servicio en un estado iniciado.'
ms.assetid: 2efd2a06-a03c-4f4c-b2fa-889f84faac0f
ms.tgt_platform: multiple
title: Método StartService de la CIM_ClusteringService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dcd18af37da9302256776cfee844fd83f989c9b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086193"
---
# <a name="startservice-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="f63d4-103">Método StartService de la clase \_ ClusteringService de CIM</span><span class="sxs-lookup"><span data-stu-id="f63d4-103">StartService method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="f63d4-104">El **método StartService** coloca el servicio en estado iniciado.</span><span class="sxs-lookup"><span data-stu-id="f63d4-104">The **StartService** method puts the service in a started state.</span></span> <span data-ttu-id="f63d4-105">En una subclase, el conjunto de códigos de retorno posibles se puede especificar mediante un **calificador ValueMap** en el método .</span><span class="sxs-lookup"><span data-stu-id="f63d4-105">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="f63d4-106">Las cadenas a las que se traduce el contenido de **ValueMap** también se pueden especificar en la subclase como calificador de **matriz Values.**</span><span class="sxs-lookup"><span data-stu-id="f63d4-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="f63d4-107">Este método se hereda del [**servicio CIM \_**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="f63d4-107">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f63d4-108">Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI.</span><span class="sxs-lookup"><span data-stu-id="f63d4-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f63d4-109">WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f63d4-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f63d4-110">En este tema se Managed Object Format sintaxis de MOF .</span><span class="sxs-lookup"><span data-stu-id="f63d4-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f63d4-111">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f63d4-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f63d4-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f63d4-112">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="f63d4-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f63d4-113">Parameters</span></span>

<span data-ttu-id="f63d4-114">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f63d4-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f63d4-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f63d4-115">Return value</span></span>

<span data-ttu-id="f63d4-116">Devuelve un valor de 0 (cero) si el servicio se inició correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="f63d4-116">Returns a value of 0 (zero) if the service was successfully started, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f63d4-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f63d4-117">Remarks</span></span>

<span data-ttu-id="f63d4-118">Wmi no implementa actualmente este método.</span><span class="sxs-lookup"><span data-stu-id="f63d4-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f63d4-119">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="f63d4-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f63d4-120">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="f63d4-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f63d4-121">Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="f63d4-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f63d4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f63d4-122">Requirements</span></span>



| <span data-ttu-id="f63d4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f63d4-123">Requirement</span></span> | <span data-ttu-id="f63d4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f63d4-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f63d4-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f63d4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f63d4-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f63d4-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f63d4-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f63d4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f63d4-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f63d4-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f63d4-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f63d4-129">Namespace</span></span><br/>                | <span data-ttu-id="f63d4-130">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="f63d4-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f63d4-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f63d4-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f63d4-132"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="f63d4-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f63d4-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f63d4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f63d4-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f63d4-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f63d4-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f63d4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f63d4-136">CIM \_ ClusteringService</span><span class="sxs-lookup"><span data-stu-id="f63d4-136">CIM\_ClusteringService</span></span>](startservice-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="f63d4-137">**CIM \_ ClusteringService**</span><span class="sxs-lookup"><span data-stu-id="f63d4-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

