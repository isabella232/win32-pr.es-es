---
description: El nuevo método inicializa un comando que se va a ejecutar y devuelve un nuevo objeto CDeferredCommand.
ms.assetid: bdd80747-a15b-422a-b742-ebfa4076bdf7
title: Método CCmdQueue. New (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.New
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 58c3aee63005010b9ed7366cfb63a69fcc7348b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678958"
---
# <a name="ccmdqueuenew-method"></a><span data-ttu-id="ef497-103">CCmdQueue. New (método)</span><span class="sxs-lookup"><span data-stu-id="ef497-103">CCmdQueue.New method</span></span>

<span data-ttu-id="ef497-104">El `New` método inicializa un comando que se va a ejecutar y devuelve un nuevo objeto [**CDeferredCommand**](cdeferredcommand.md) .</span><span class="sxs-lookup"><span data-stu-id="ef497-104">The `New` method initializes a command to be run and returns a new [**CDeferredCommand**](cdeferredcommand.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef497-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef497-105">Syntax</span></span>


```C++
virtual HRESULT New(
   CDeferredCommand **ppCmd,
   LPUNKNOWN        pUnk,
   REFTIME          time,
   GUID             *iid,
   long             dispidMethod,
   short            wFlags,
   long             cArgs,
   VARIANT          *pDispParams,
   VARIANT          *pvarResult,
   short            *puArgErr,
   BOOL             bStream
);
```



## <a name="parameters"></a><span data-ttu-id="ef497-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef497-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef497-107">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="ef497-107">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="ef497-108">Dirección de un puntero a un objeto [**CDeferredCommand**](cdeferredcommand.md) por el que una aplicación puede cancelar el comando, establecer un nuevo tiempo de presentación para el mismo o recuperar la información de estimación.</span><span class="sxs-lookup"><span data-stu-id="ef497-108">Address of a pointer to a [**CDeferredCommand**](cdeferredcommand.md) object by which an application can cancel the command, set a new presentation time for it, or retrieve estimate information.</span></span>

</dd> <dt>

<span data-ttu-id="ef497-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="ef497-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="ef497-110">Puntero al objeto que ejecutará el comando.</span><span class="sxs-lookup"><span data-stu-id="ef497-110">Pointer to the object that will run the command.</span></span>

</dd> <dt>

<span data-ttu-id="ef497-111">*time*</span><span class="sxs-lookup"><span data-stu-id="ef497-111">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="ef497-112">Hora a la que se va a ejecutar el comando o comandos en cola.</span><span class="sxs-lookup"><span data-stu-id="ef497-112">Time at which to run the queued command or commands.</span></span>

</dd> <dt>

<span data-ttu-id="ef497-113">*suscripto*</span><span class="sxs-lookup"><span data-stu-id="ef497-113">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="ef497-114">Puntero al identificador único global (**GUID**) de la interfaz a la que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="ef497-114">Pointer to the globally unique identifier (**GUID**) of the interface to call.</span></span>

</dd> <dt>

<span data-ttu-id="ef497-115">*dispidMethod*</span><span class="sxs-lookup"><span data-stu-id="ef497-115">*dispidMethod*</span></span> 
</dt> <dd>

<span data-ttu-id="ef497-116">Método en la interfaz a la que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="ef497-116">Method on the interface to be called.</span></span>

</dd> <dt>

<span data-ttu-id="ef497-117">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="ef497-117">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="ef497-118">Marcas que describen el contexto de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ef497-118">Flags describing the context of the call.</span></span> <span data-ttu-id="ef497-119">Este parámetro admite las mismas marcas que el método **IDispatch:: Invoke** .</span><span class="sxs-lookup"><span data-stu-id="ef497-119">This parameter supports the same flags as the **IDispatch::Invoke** method.</span></span>

</dd> <dt>

<span data-ttu-id="ef497-120">*cArgs*</span><span class="sxs-lookup"><span data-stu-id="ef497-120">*cArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="ef497-121">Número de argumentos pasados.</span><span class="sxs-lookup"><span data-stu-id="ef497-121">Number of arguments passed.</span></span>

</dd> <dt>

<span data-ttu-id="ef497-122">*pDispParams*</span><span class="sxs-lookup"><span data-stu-id="ef497-122">*pDispParams*</span></span> 
</dt> <dd>

<span data-ttu-id="ef497-123">Puntero a la lista de tipos Variant asociados a los parámetros de envío.</span><span class="sxs-lookup"><span data-stu-id="ef497-123">Pointer to the list of variant types associated with the dispatch parameters.</span></span>

</dd> <dt>

<span data-ttu-id="ef497-124">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="ef497-124">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="ef497-125">Puntero a la lista donde se van a devolver los resultados, si los hay.</span><span class="sxs-lookup"><span data-stu-id="ef497-125">Pointer to the list where results, if any, are to be returned.</span></span>

</dd> <dt>

<span data-ttu-id="ef497-126">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="ef497-126">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="ef497-127">Puntero al índice de la lista de parámetros *pDispParams* donde se produjo el último error.</span><span class="sxs-lookup"><span data-stu-id="ef497-127">Pointer to the index within the *pDispParams* parameter list where the last error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="ef497-128">*bStream*</span><span class="sxs-lookup"><span data-stu-id="ef497-128">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="ef497-129">Valor que indica si el parámetro de *hora* es un valor de tiempo de secuencia (**true**) o un valor de tiempo de presentación (**false**).</span><span class="sxs-lookup"><span data-stu-id="ef497-129">Value indicating whether the *time* parameter is a stream-time value (**TRUE**) or a presentation-time value (**FALSE**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef497-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef497-130">Return value</span></span>

<span data-ttu-id="ef497-131">Devuelve S \_ correcto si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="ef497-131">Returns S\_OK if successful.</span></span> <span data-ttu-id="ef497-132">Devuelve E \_ OUTOFMEMORY si *ppCmd* vuelve de crear el nuevo objeto [**CDeferredCommand**](cdeferredcommand.md) con un valor **null**.</span><span class="sxs-lookup"><span data-stu-id="ef497-132">Returns E\_OUTOFMEMORY if *ppCmd* returns from creating the new [**CDeferredCommand**](cdeferredcommand.md) object with a value of **NULL**.</span></span> <span data-ttu-id="ef497-133">De lo contrario, devuelve un **valor HRESULT** que indica un error al intentar crear un nuevo objeto **CDeferredCommand** .</span><span class="sxs-lookup"><span data-stu-id="ef497-133">Otherwise, returns an **HRESULT** that indicates an error from attempting to create a new **CDeferredCommand** object.</span></span> <span data-ttu-id="ef497-134">Si se produce un error, no se ha puesto en cola ningún objeto.</span><span class="sxs-lookup"><span data-stu-id="ef497-134">If there is an error, no object has been queued.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef497-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef497-135">Remarks</span></span>

<span data-ttu-id="ef497-136">El nuevo objeto [**CDeferredCommand**](cdeferredcommand.md) se inicializará con los parámetros y se agregará a la cola durante la construcción.</span><span class="sxs-lookup"><span data-stu-id="ef497-136">The new [**CDeferredCommand**](cdeferredcommand.md) object will be initialized with the parameters and will be added to the queue during construction.</span></span> <span data-ttu-id="ef497-137">Este método es similar al método **IDispatch:: Invoke** .</span><span class="sxs-lookup"><span data-stu-id="ef497-137">This method is similar to the **IDispatch::Invoke** method.</span></span>

<span data-ttu-id="ef497-138">Los valores para el parámetro *wFlags* son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="ef497-138">Values for the *wFlags* parameter include the following:</span></span>



| <span data-ttu-id="ef497-139">Value</span><span class="sxs-lookup"><span data-stu-id="ef497-139">Value</span></span>                    | <span data-ttu-id="ef497-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef497-140">Description</span></span>                                                                                                                                                          |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef497-141">DISPATCH ( \_ método)</span><span class="sxs-lookup"><span data-stu-id="ef497-141">DISPATCH\_METHOD</span></span>         | <span data-ttu-id="ef497-142">El miembro se está ejecutando como un método.</span><span class="sxs-lookup"><span data-stu-id="ef497-142">The member is being run as a method.</span></span> <span data-ttu-id="ef497-143">Si una propiedad tiene el mismo nombre, se pueden establecer tanto esta marca como la de envío \_ PropertyGet (.</span><span class="sxs-lookup"><span data-stu-id="ef497-143">If a property has the same name, both this and the DISPATCH\_PROPERTYGET flag can be set.</span></span>                                       |
| <span data-ttu-id="ef497-144">ENVIAR \_ PropertyGet (</span><span class="sxs-lookup"><span data-stu-id="ef497-144">DISPATCH\_PROPERTYGET</span></span>    | <span data-ttu-id="ef497-145">El miembro se recupera como una propiedad o miembro de datos.</span><span class="sxs-lookup"><span data-stu-id="ef497-145">The member is being retrieved as a property or data member.</span></span>                                                                                                          |
| <span data-ttu-id="ef497-146">ENVIAR \_ PROPERTYPUT</span><span class="sxs-lookup"><span data-stu-id="ef497-146">DISPATCH\_PROPERTYPUT</span></span>    | <span data-ttu-id="ef497-147">El miembro se está cambiando como una propiedad o un miembro de datos.</span><span class="sxs-lookup"><span data-stu-id="ef497-147">The member is being changed as a property or data member.</span></span>                                                                                                            |
| <span data-ttu-id="ef497-148">ENVIAR \_ PROPERTYPUTREF</span><span class="sxs-lookup"><span data-stu-id="ef497-148">DISPATCH\_PROPERTYPUTREF</span></span> | <span data-ttu-id="ef497-149">El miembro se está cambiando a través de una asignación de referencia, en lugar de una asignación de valores.</span><span class="sxs-lookup"><span data-stu-id="ef497-149">The member is being changed via a reference assignment, rather than a value assignment.</span></span> <span data-ttu-id="ef497-150">Este valor solo es válido cuando la propiedad acepta una referencia a un objeto.</span><span class="sxs-lookup"><span data-stu-id="ef497-150">This value is valid only when the property accepts a reference to an object.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="ef497-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef497-151">Requirements</span></span>



| <span data-ttu-id="ef497-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef497-152">Requirement</span></span> | <span data-ttu-id="ef497-153">Value</span><span class="sxs-lookup"><span data-stu-id="ef497-153">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef497-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef497-154">Header</span></span><br/>  | <dl> <span data-ttu-id="ef497-155"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef497-155"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ef497-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef497-156">Library</span></span><br/> | <dl> <span data-ttu-id="ef497-157"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ef497-157"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef497-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef497-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef497-159">**Clase CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="ef497-159">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




