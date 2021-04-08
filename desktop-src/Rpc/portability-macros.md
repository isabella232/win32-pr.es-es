---
title: Macros de portabilidad (RPC. h)
description: Las herramientas de RPC logran el modelo, la llamada y la independencia de la Convención de nomenclatura al asociar los tipos de datos y los tipos de valor devueltos en los archivos de código auxiliar y los archivos de encabezado generados con definiciones que son específicas de cada plataforma.
ms.assetid: 94de1138-5a84-41d8-bf88-97f0ac630f5f
keywords:
- Macros de portabilidad RPC
topic_type:
- apiref
api_name:
- Portability Macros
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c184365496db7757524a12f1b0807c3c53e24b27
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104003297"
---
# <a name="portability-macros"></a><span data-ttu-id="73796-104">Macros de portabilidad</span><span class="sxs-lookup"><span data-stu-id="73796-104">Portability Macros</span></span>

<span data-ttu-id="73796-105">Las herramientas de RPC logran el modelo, la llamada y la independencia de la Convención de nomenclatura al asociar los tipos de datos y los tipos de valor devueltos en los archivos de código auxiliar y los archivos de encabezado generados con definiciones que son específicas de cada plataforma.</span><span class="sxs-lookup"><span data-stu-id="73796-105">The RPC tools achieve model, calling, and naming-convention independence by associating data types and function-return types in the generated stub files and header files with definitions that are specific to each platform.</span></span> <span data-ttu-id="73796-106">Estas definiciones de macro garantizan que todos los tipos de datos y funciones que requieran la designación de **\_ \_ Far** se especifiquen como objetos Far.</span><span class="sxs-lookup"><span data-stu-id="73796-106">These macro definitions ensure that any data types and functions that require the designation of **\_\_far** are specified as far objects.</span></span>

<span data-ttu-id="73796-107">La siguiente ilustración muestra las definiciones de macro que el compilador MIDL aplica a las llamadas de función entre los componentes RPC:</span><span class="sxs-lookup"><span data-stu-id="73796-107">The following figure shows the macro definitions that the MIDL compiler applies to function calls between RPC components:</span></span>

![Diagrama que muestra las definiciones de macros MIDL se aplica a las llamadas a funciones.](images/prog-a29.png)

<span data-ttu-id="73796-109">Las macros RPC se definen como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="73796-109">RPC macros are defined as follows.</span></span>



| <span data-ttu-id="73796-110">Definición</span><span class="sxs-lookup"><span data-stu-id="73796-110">Definition</span></span>    | <span data-ttu-id="73796-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="73796-111">Description</span></span>                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73796-112">\_\_API de RPC \_</span><span class="sxs-lookup"><span data-stu-id="73796-112">\_\_RPC\_API</span></span>  | <span data-ttu-id="73796-113">Se aplica a las llamadas realizadas por el código auxiliar a la aplicación de usuario.</span><span class="sxs-lookup"><span data-stu-id="73796-113">Applied to calls made by the stub to the user application.</span></span> <span data-ttu-id="73796-114">Ambas funciones se encuentran en el mismo programa ejecutable.</span><span class="sxs-lookup"><span data-stu-id="73796-114">Both functions are in the same executable program.</span></span>                                       |
| <span data-ttu-id="73796-115">\_\_extremo de RPC \_</span><span class="sxs-lookup"><span data-stu-id="73796-115">\_\_RPC\_FAR</span></span>  | <span data-ttu-id="73796-116">Se aplica a la definición de macro estándar para los punteros.</span><span class="sxs-lookup"><span data-stu-id="73796-116">Applied to the standard macro definition for pointers.</span></span> <span data-ttu-id="73796-117">Esta definición de macro debe aparecer como parte de la firma de todas las funciones proporcionadas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="73796-117">This macro definition should appear as part of the signature of all user-supplied functions.</span></span> |
| <span data-ttu-id="73796-118">\_\_\_código auxiliar de RPC</span><span class="sxs-lookup"><span data-stu-id="73796-118">\_\_RPC\_STUB</span></span> | <span data-ttu-id="73796-119">Se aplica a las llamadas realizadas desde la biblioteca en tiempo de ejecución al código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="73796-119">Applied to calls made from the run-time library to the stub.</span></span> <span data-ttu-id="73796-120">Estas llamadas se pueden considerar privadas.</span><span class="sxs-lookup"><span data-stu-id="73796-120">These calls can be considered private.</span></span>                                                 |
| <span data-ttu-id="73796-121">\_\_\_usuario RPC</span><span class="sxs-lookup"><span data-stu-id="73796-121">\_\_RPC\_USER</span></span> | <span data-ttu-id="73796-122">Se aplica a las llamadas realizadas por la biblioteca en tiempo de ejecución a la aplicación de usuario.</span><span class="sxs-lookup"><span data-stu-id="73796-122">Applied to calls made by the run-time library to the user application.</span></span> <span data-ttu-id="73796-123">Estos cruzan el límite entre un archivo DLL y una aplicación.</span><span class="sxs-lookup"><span data-stu-id="73796-123">These cross the boundary between a DLL and an application.</span></span>                   |
| <span data-ttu-id="73796-124">\_entrada RPC</span><span class="sxs-lookup"><span data-stu-id="73796-124">RPC\_ENTRY</span></span>    | <span data-ttu-id="73796-125">Se aplica a las llamadas realizadas por la aplicación o el código auxiliar a la biblioteca en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="73796-125">Applied to calls made by the application or stub to the run-time library.</span></span> <span data-ttu-id="73796-126">Esta definición de macro se aplica a todas las funciones de tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="73796-126">This macro definition is applied to all RPC run-time functions.</span></span>           |



 

<span data-ttu-id="73796-127">Para vincular correctamente las bibliotecas en tiempo de ejecución de Microsoft RPC, los códigos auxiliares y las rutinas de soporte técnico, algunas funciones proporcionadas por el usuario también deben incluir estas macros en la definición de función.</span><span class="sxs-lookup"><span data-stu-id="73796-127">To link correctly with the Microsoft RPC run-time libraries, stubs, and support routines, some user-supplied functions must also include these macros in the function definition.</span></span> <span data-ttu-id="73796-128">Use la **\_ \_ \_ API de RPC** de macros al definir las funciones asociadas a la administración de memoria, identificadores de enlace definidos por el usuario y el atributo **transmitir \_ como** , y use la macro **\_ \_ RPC \_ User** cuando defina la rutina de ejecución de contexto asociada al identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="73796-128">Use the macro **\_\_RPC\_API** when you define the functions associated with memory management, user-defined binding handles, and the **transmit\_as** attribute, and use the macro **\_\_RPC\_USER** when you define the context run-down routine associated with the context handle.</span></span> <span data-ttu-id="73796-129">Especifique las funciones como:</span><span class="sxs-lookup"><span data-stu-id="73796-129">Specify the functions as:</span></span>

<dl> <dt>

<span data-ttu-id="73796-130"><span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_\_Asignación de *\_ usuarios de MIDL* de usuario RPC \_ (...)</span><span class="sxs-lookup"><span data-stu-id="73796-130"><span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_RPC\_USER *midl\_user*\_allocate(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="73796-131"><span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_Usuario de RPC \_ usuario de *MIDL \_* \_ gratis (...)</span><span class="sxs-lookup"><span data-stu-id="73796-131"><span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_RPC\_USER *midl\_user*\_free(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="73796-132"><span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_\_Enlace de *handletype* de usuario de RPC \_ (...)</span><span class="sxs-lookup"><span data-stu-id="73796-132"><span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_RPC\_USER  *handletype*\_bind(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="73796-133"><span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_Handletype de usuario de RPC \_  \_ Desenlazar (...)</span><span class="sxs-lookup"><span data-stu-id="73796-133"><span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_RPC\_USER *handletype*\_unbind(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="73796-134"><span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_\_ *Tipo* de usuario RPC \_ a \_ local</span><span class="sxs-lookup"><span data-stu-id="73796-134"><span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_RPC\_USER *type*\_to\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="73796-135"><span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_\_ *Tipo* de usuario RPC \_ de \_ local</span><span class="sxs-lookup"><span data-stu-id="73796-135"><span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_RPC\_USER *type*\_from\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="73796-136"><span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_\_Tipo de usuario RPC \_ para la \_ transmisión (...)</span><span class="sxs-lookup"><span data-stu-id="73796-136"><span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_RPC\_USER type\_to\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="73796-137"><span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_\_ *Tipo* de usuario RPC \_ de \_ transmisión (...)</span><span class="sxs-lookup"><span data-stu-id="73796-137"><span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_RPC\_USER *type*\_from\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="73796-138"><span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_\_ *Tipo* de usuario RPC \_ gratis \_ local</span><span class="sxs-lookup"><span data-stu-id="73796-138"><span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_RPC\_USER *type*\_free\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="73796-139"><span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_\_Inst. de *tipo* de usuario RPC \_ \_ (...)</span><span class="sxs-lookup"><span data-stu-id="73796-139"><span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_RPC\_USER *type*\_free\_inst(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="73796-140"><span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_\_Transmisión gratuita del *tipo* de usuario RPC \_ \_ (...)</span><span class="sxs-lookup"><span data-stu-id="73796-140"><span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_RPC\_USER *type*\_free\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="73796-141"><span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_Detención de contexto de usuario de RPC \_ \_ (...)</span><span class="sxs-lookup"><span data-stu-id="73796-141"><span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_RPC\_USER context\_rundown(...)</span></span>
<span data-ttu-id="73796-142"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="73796-142"></dt> <dd></dd> </dl></span></span>

> [!Note]  
> <span data-ttu-id="73796-143">Todos los parámetros de puntero en estas funciones se deben especificar mediante la macro **\_ \_ RPC \_ Far**.</span><span class="sxs-lookup"><span data-stu-id="73796-143">All pointer parameters in these functions must be specified using the macro **\_\_RPC\_FAR**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="73796-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73796-144">Requirements</span></span>



| <span data-ttu-id="73796-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="73796-145">Requirement</span></span> | <span data-ttu-id="73796-146">Value</span><span class="sxs-lookup"><span data-stu-id="73796-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="73796-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73796-147">Minimum supported client</span></span><br/> | <span data-ttu-id="73796-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="73796-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="73796-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73796-149">Minimum supported server</span></span><br/> | <span data-ttu-id="73796-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="73796-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="73796-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73796-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="73796-152"><dt>RPC. h</dt></span><span class="sxs-lookup"><span data-stu-id="73796-152"><dt>Rpc.h</dt></span></span> </dl> |



 

 





