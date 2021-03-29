---
title: implicit_handle atributo)
description: El atributo \ \_ ACF de identificador implícito especifica el identificador que se usa para las funciones que no incluyen un identificador explícito como parámetro de procedimiento.
ms.assetid: 09c17473-87b5-4fd6-beb9-3d9b7bc82d8c
keywords:
- implicit_handle el atributo MIDL
topic_type:
- apiref
api_name:
- implicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22f410fa048a27e1f7626690e6308de4c1a31c2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904016"
---
# <a name="implicit_handle-attribute"></a><span data-ttu-id="f1100-104">\_atributo de identificador implícito</span><span class="sxs-lookup"><span data-stu-id="f1100-104">implicit\_handle attribute</span></span>

<span data-ttu-id="f1100-105">El atributo ACF de **\[ \_ identificador \] implícito** especifica el identificador que se usa para las funciones que no incluyen un identificador explícito como parámetro de procedimiento.</span><span class="sxs-lookup"><span data-stu-id="f1100-105">The **\[implicit\_handle\]** ACF attribute specifies the handle used for functions that do not include an explicit handle as a procedure parameter.</span></span>

``` syntax
implicit_handle(handle-type handle-name)
```

## <a name="parameters"></a><span data-ttu-id="f1100-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1100-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1100-107">*tipo de identificador*</span><span class="sxs-lookup"><span data-stu-id="f1100-107">*handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="f1100-108">Especifica el tipo de datos Handle, como el identificador de tipo base [**\_ t**](handle-t.md) o un tipo de identificador definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f1100-108">Specifies the handle data type, such as the base type [**handle\_t**](handle-t.md) or a user-defined handle type.</span></span>

</dd> <dt>

<span data-ttu-id="f1100-109">*identificador: nombre*</span><span class="sxs-lookup"><span data-stu-id="f1100-109">*handle-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f1100-110">Especifica el nombre del identificador.</span><span class="sxs-lookup"><span data-stu-id="f1100-110">Specifies the name of the handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1100-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1100-111">Remarks</span></span>

<span data-ttu-id="f1100-112">El identificador especificado por el atributo de **\[ \_ identificador \] implícito** se utiliza de maneras diferentes en función de la naturaleza del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="f1100-112">The handle specified by the **\[implicit\_handle\]** attribute is used in different ways depending on the nature of the procedure.</span></span> <span data-ttu-id="f1100-113">Si el procedimiento es remoto, el identificador se utilizará como identificador de enlace para la llamada remota.</span><span class="sxs-lookup"><span data-stu-id="f1100-113">If the procedure is remote, the handle will be used as the binding handle for the remote call.</span></span> <span data-ttu-id="f1100-114">El identificador implícito también puede usarse para establecer un enlace inicial para una función que usa un identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="f1100-114">The implicit handle may also be used to establish an initial binding for a function that uses a context handle.</span></span> <span data-ttu-id="f1100-115">Si el procedimiento es un procedimiento de serialización, el identificador se usa como un identificador de serialización que controla la operación.</span><span class="sxs-lookup"><span data-stu-id="f1100-115">If the procedure is a serializing procedure, the handle is used as a serializing handle controlling the operation.</span></span> <span data-ttu-id="f1100-116">En el caso de la serialización de tipos, el identificador se usa como el identificador de serialización para todos los tipos serializados.</span><span class="sxs-lookup"><span data-stu-id="f1100-116">In the case of type serialization, the handle is used as the serialization handle for all the serialized types.</span></span>

<span data-ttu-id="f1100-117">El atributo de **\[ \_ identificador \] implícito** especifica una variable global que contiene un identificador usado por cualquier función que necesite identificadores implícitos.</span><span class="sxs-lookup"><span data-stu-id="f1100-117">The **\[implicit\_handle\]** attribute specifies a global variable that contains a handle used by any function needing implicit handles.</span></span>

<span data-ttu-id="f1100-118">El tipo de identificador de enlace implícito debe ser [**Handle \_ t**](handle-t.md) (o un tipo basado en el **identificador \_ t**) o un tipo de identificador definido por el usuario especificado con el atributo [**Handle**](handle.md) .</span><span class="sxs-lookup"><span data-stu-id="f1100-118">The implicit binding handle type must be either [**handle\_t**](handle-t.md) (or a type based on **handle\_t**) or a user-defined handle type specified with the [**handle**](handle.md) attribute.</span></span> <span data-ttu-id="f1100-119">El identificador de serialización implícito debe ser un tipo basado en el **identificador \_ t**.</span><span class="sxs-lookup"><span data-stu-id="f1100-119">The implicit serializing handle must be a type based on **handle\_t**.</span></span>

<span data-ttu-id="f1100-120">Si el tipo de identificador implícito no está definido en el archivo IDL o en los archivos incluidos y importados por el archivo IDL para el equipo MIDL, debe proporcionar el archivo que contiene la definición del tipo de identificador al compilar el código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="f1100-120">If the implicit handle type is not defined in the IDL file or in any files included and imported by the IDL file for the MIDL computer, you must supply the file containing the handle-type definition when you compile the stubs.</span></span> <span data-ttu-id="f1100-121">Utilice la instrucción ACF [**include**](include.md) para incluir el archivo que contiene la definición del tipo de identificador.</span><span class="sxs-lookup"><span data-stu-id="f1100-121">Use the ACF [**include**](include.md) statement to include the file containing the handle-type definition.</span></span>

<span data-ttu-id="f1100-122">El atributo de **\[ \_ identificador \] implícito** puede aparecer una vez, como máximo.</span><span class="sxs-lookup"><span data-stu-id="f1100-122">The **\[implicit\_handle\]** attribute can occur once, at most.</span></span> <span data-ttu-id="f1100-123">El atributo de **\[ \_ identificador \] implícito** solo puede producirse [**\[ \_ \]**](auto-handle.md) si no se producen los atributos de identificador automático y [**\[ \_ identificador \] explícito**](explicit-handle.md) .</span><span class="sxs-lookup"><span data-stu-id="f1100-123">The **\[implicit\_handle\]** attribute can occur only if the [**\[auto\_handle\]**](auto-handle.md) and [**\[explicit\_handle\]**](explicit-handle.md) attributes do not occur.</span></span>

## <a name="examples"></a><span data-ttu-id="f1100-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f1100-124">Examples</span></span>

``` syntax
/* ACF file */ 
[
    implicit_handle(handle_t hMyHandle)
] 
interface iface
{ 
    // Attribute configuration statements
}
```

## <a name="see-also"></a><span data-ttu-id="f1100-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1100-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1100-126">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="f1100-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="f1100-127">**\_identificador automático**</span><span class="sxs-lookup"><span data-stu-id="f1100-127">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="f1100-128">**\_identificador explícito**</span><span class="sxs-lookup"><span data-stu-id="f1100-128">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="f1100-129">**identificador \_ t**</span><span class="sxs-lookup"><span data-stu-id="f1100-129">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="f1100-130">**inclui**</span><span class="sxs-lookup"><span data-stu-id="f1100-130">**include**</span></span>](include.md)
</dt> </dl>

 

 




