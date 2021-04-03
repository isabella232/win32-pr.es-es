---
description: El \_ método Clone del objeto SWbemObject devuelve un nuevo objeto que es un clon del objeto actual.
ms.assetid: d0773c94-30b5-4217-8a9a-0bceb9e75f02
ms.tgt_platform: multiple
title: Método SWbemObject.Clone_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Clone_
- ISWbemObject.Clone_
- ISWbemObject.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84ca02bf749fd69db01ca7925b554c4eb0d95c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083214"
---
# <a name="swbemobjectclone_-method"></a><span data-ttu-id="ae92d-103">SWbemObject. Clone ( \_ método)</span><span class="sxs-lookup"><span data-stu-id="ae92d-103">SWbemObject.Clone\_ method</span></span>

<span data-ttu-id="ae92d-104">El **método \_ Clone** del objeto [**SWbemObject**](swbemobject.md) devuelve un nuevo objeto que es un clon del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="ae92d-104">The **Clone\_** method of the [**SWbemObject**](swbemobject.md) object returns a new object that is a clone of the current object.</span></span>

<span data-ttu-id="ae92d-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ae92d-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ae92d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae92d-106">Syntax</span></span>


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a><span data-ttu-id="ae92d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae92d-107">Parameters</span></span>

<span data-ttu-id="ae92d-108">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ae92d-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae92d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae92d-109">Return value</span></span>

<span data-ttu-id="ae92d-110">Si es correcto, este método devuelve un nuevo objeto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="ae92d-110">If successful, this method returns a new [**SWbemObject**](swbemobject.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ae92d-111">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ae92d-111">Error codes</span></span>

<span data-ttu-id="ae92d-112">Después de completar el **método \_ Clone** , el objeto **Err** puede contener uno de los códigos de error siguientes.</span><span class="sxs-lookup"><span data-stu-id="ae92d-112">After completion of the **Clone\_** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="ae92d-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ae92d-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ae92d-114">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="ae92d-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="ae92d-115">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="ae92d-115">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="ae92d-116">No se especificó **nada** como parámetro y no es aceptable en este uso.</span><span class="sxs-lookup"><span data-stu-id="ae92d-116">**Nothing** was specified as a parameter, and it is not acceptable in this usage.</span></span>

</dd> <dt>

<span data-ttu-id="ae92d-117">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="ae92d-117">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="ae92d-118">No hay suficiente memoria para clonar el objeto.</span><span class="sxs-lookup"><span data-stu-id="ae92d-118">Not enough memory to clone the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae92d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae92d-119">Remarks</span></span>

<span data-ttu-id="ae92d-120">Use el **método \_ Clone** para duplicar una definición de clase o una instancia de.</span><span class="sxs-lookup"><span data-stu-id="ae92d-120">Use the **Clone\_** method to duplicate a class definition or an instance.</span></span> <span data-ttu-id="ae92d-121">Esto resulta útil cuando se necesita la copia original del objeto con fines de copia de seguridad mientras se modifica una nueva copia.</span><span class="sxs-lookup"><span data-stu-id="ae92d-121">This is useful when you need the original copy of the object for backup purposes while you are modifying a new copy.</span></span> <span data-ttu-id="ae92d-122">Del mismo modo, use este método para crear muchas instancias nuevas a partir de una instancia de origen única.</span><span class="sxs-lookup"><span data-stu-id="ae92d-122">Likewise, use this method to create many new instances from a single source instance.</span></span> <span data-ttu-id="ae92d-123">Por ejemplo, use [**SWbemObject. SpawnInstance \_**](swbemobject-spawninstance-.md) para crear una única instancia de inicio y use **SWbemObject. Clone \_** para generar 100 copias de la instancia rápidamente.</span><span class="sxs-lookup"><span data-stu-id="ae92d-123">For example, use [**SWbemObject.SpawnInstance\_**](swbemobject-spawninstance-.md) to create a single starting instance, and use **SWbemObject.Clone\_** to produce 100 copies of the instance quickly.</span></span> <span data-ttu-id="ae92d-124">Posteriormente, puede modificar los objetos, asignando cada uno de los valores específicos.</span><span class="sxs-lookup"><span data-stu-id="ae92d-124">Subsequently, you can modify the objects, giving each one specific values.</span></span>

<span data-ttu-id="ae92d-125">No es posible utilizar este método para convertir una definición de clase en una instancia de o para convertir una instancia de en una definición de clase.</span><span class="sxs-lookup"><span data-stu-id="ae92d-125">It is not possible to use this method to convert a class definition to an instance, or to convert an instance to a class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae92d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae92d-126">Requirements</span></span>



| <span data-ttu-id="ae92d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae92d-127">Requirement</span></span> | <span data-ttu-id="ae92d-128">Value</span><span class="sxs-lookup"><span data-stu-id="ae92d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae92d-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae92d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ae92d-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae92d-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ae92d-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae92d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ae92d-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae92d-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ae92d-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae92d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae92d-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae92d-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ae92d-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ae92d-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="ae92d-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ae92d-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ae92d-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ae92d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae92d-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae92d-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ae92d-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="ae92d-139">CLSID</span></span><br/>                    | <span data-ttu-id="ae92d-140">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="ae92d-140">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="ae92d-141">IID</span><span class="sxs-lookup"><span data-stu-id="ae92d-141">IID</span></span><br/>                      | <span data-ttu-id="ae92d-142">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="ae92d-142">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




