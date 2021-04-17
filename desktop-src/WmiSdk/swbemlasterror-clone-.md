---
description: El \_ método Clone del objeto SWbemLastError devuelve un nuevo objeto que es un clon del objeto SWbemLastError actual.
ms.assetid: 577be060-309f-40a2-a4db-c0a477c21f11
ms.tgt_platform: multiple
title: Método SWbemLastError.Clone_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Clone_
- ISWbemLastError.Clone_
- ISWbemLastError.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7d4d43f73ab42021235db39adba0a77bc783b97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697360"
---
# <a name="swbemlasterrorclone_-method"></a><span data-ttu-id="a2a93-103">SWbemLastError. Clone ( \_ método)</span><span class="sxs-lookup"><span data-stu-id="a2a93-103">SWbemLastError.Clone\_ method</span></span>

<span data-ttu-id="a2a93-104">El **método \_ Clone** del objeto [**SWbemLastError**](swbemlasterror.md) devuelve un nuevo objeto que es un clon del objeto **SWbemLastError** actual.</span><span class="sxs-lookup"><span data-stu-id="a2a93-104">The **Clone\_** method of the [**SWbemLastError**](swbemlasterror.md) object returns a new object that is a clone of the current **SWbemLastError** object.</span></span>

<span data-ttu-id="a2a93-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a2a93-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2a93-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2a93-106">Syntax</span></span>


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a><span data-ttu-id="a2a93-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2a93-107">Parameters</span></span>

<span data-ttu-id="a2a93-108">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a2a93-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2a93-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2a93-109">Return value</span></span>

<span data-ttu-id="a2a93-110">Si el **método \_ Clone** se realiza correctamente, devuelve un nuevo objeto [**SWbemLastError**](swbemlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="a2a93-110">If the **Clone\_** method is successful, it returns a new [**SWbemLastError**](swbemlasterror.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a2a93-111">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a2a93-111">Error codes</span></span>

<span data-ttu-id="a2a93-112">Tras completar el método **Clone \_** , el objeto **Err** puede contener uno de los códigos de error siguientes.</span><span class="sxs-lookup"><span data-stu-id="a2a93-112">Upon the completion of the **Clone\_** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="a2a93-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="a2a93-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="a2a93-114">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="a2a93-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="a2a93-115">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="a2a93-115">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="a2a93-116">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="a2a93-116">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a2a93-117">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="a2a93-117">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="a2a93-118">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="a2a93-118">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2a93-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2a93-119">Remarks</span></span>

<span data-ttu-id="a2a93-120">Use el **método \_ Clone** para duplicar una instancia o una definición de clase.</span><span class="sxs-lookup"><span data-stu-id="a2a93-120">Use the **Clone\_** method to duplicate a class definition or instance.</span></span> <span data-ttu-id="a2a93-121">Este método es útil cuando se necesita realizar una copia de seguridad de la copia original del objeto mientras se modifica una nueva copia.</span><span class="sxs-lookup"><span data-stu-id="a2a93-121">This method is useful when you need to back up the original copy of the object while you modify a new copy.</span></span> <span data-ttu-id="a2a93-122">Además, use este método para crear muchas instancias nuevas a partir de una instancia de origen única.</span><span class="sxs-lookup"><span data-stu-id="a2a93-122">Also, use this method to create many new instances from a single source instance.</span></span> <span data-ttu-id="a2a93-123">Por ejemplo, use [**SWbemObject. SpawnInstance \_**](swbemobject-spawninstance-.md) para crear una única instancia de inicio y use **SWbemLastError. \_ Clone** para generar 100 copias de la instancia rápidamente.</span><span class="sxs-lookup"><span data-stu-id="a2a93-123">For example, use [**SWbemObject.SpawnInstance\_**](swbemobject-spawninstance-.md) to create a single starting instance and use **SWbemLastError.Clone\_** to produce 100 copies of the instance quickly.</span></span> <span data-ttu-id="a2a93-124">Posteriormente, puede modificar los objetos, asignando valores específicos a cada objeto.</span><span class="sxs-lookup"><span data-stu-id="a2a93-124">Subsequently, you can modify the objects, giving specific values to each object.</span></span>

<span data-ttu-id="a2a93-125">No es posible utilizar este método para convertir una definición de clase en una instancia de o para convertir una instancia de en una definición de clase.</span><span class="sxs-lookup"><span data-stu-id="a2a93-125">It is not possible to use this method to convert a class definition to an instance or to convert an instance to a class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2a93-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2a93-126">Requirements</span></span>



| <span data-ttu-id="a2a93-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2a93-127">Requirement</span></span> | <span data-ttu-id="a2a93-128">Value</span><span class="sxs-lookup"><span data-stu-id="a2a93-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2a93-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2a93-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a2a93-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2a93-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a2a93-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2a93-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a2a93-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2a93-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a2a93-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2a93-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2a93-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2a93-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2a93-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a2a93-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="a2a93-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a2a93-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a2a93-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a2a93-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2a93-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2a93-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a2a93-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="a2a93-139">CLSID</span></span><br/>                    | <span data-ttu-id="a2a93-140">CLSID \_ SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="a2a93-140">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="a2a93-141">IID</span><span class="sxs-lookup"><span data-stu-id="a2a93-141">IID</span></span><br/>                      | <span data-ttu-id="a2a93-142">\_ISWBEMLASTERROR IID</span><span class="sxs-lookup"><span data-stu-id="a2a93-142">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




