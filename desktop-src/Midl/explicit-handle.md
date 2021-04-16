---
title: explicit_handle atributo)
description: El atributo \ \_ ACF de identificador explícito especifica que cada procedimiento tiene, como su primer parámetro, un identificador primitivo, como un tipo de identificador \_ t.
ms.assetid: c95d005e-dcc7-4d83-885d-91c0773c0ed8
keywords:
- explicit_handle el atributo MIDL
topic_type:
- apiref
api_name:
- explicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4fa677f1bb5a3414e6cf6dc761b83414c2d68b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105651332"
---
# <a name="explicit_handle-attribute"></a><span data-ttu-id="9b965-104">\_atributo de identificador explícito</span><span class="sxs-lookup"><span data-stu-id="9b965-104">explicit\_handle attribute</span></span>

<span data-ttu-id="9b965-105">El \[ atributo ACF de **\_ identificador explícito** \] especifica que cada procedimiento tiene, como su primer parámetro, un identificador primitivo, como un tipo de [**identificador \_ t**](handle-t.md) .</span><span class="sxs-lookup"><span data-stu-id="9b965-105">The \[**explicit\_handle**\] ACF attribute specifies that each procedure has, as its first parameter, a primitive handle, such as a [**handle\_t**](handle-t.md) type.</span></span>

``` syntax
[
    explicit_handle
] 
interface interface-name
{
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="9b965-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b965-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b965-107">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="9b965-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9b965-108">Especifica el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="9b965-108">Specifies the name of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b965-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b965-109">Remarks</span></span>

<span data-ttu-id="9b965-110">Cuando se usa el atributo de **\[ \_ identificador \] explícito** , cada procedimiento tiene un identificador primitivo como primer parámetro aunque el archivo IDL no contenga este identificador en su lista de parámetros.</span><span class="sxs-lookup"><span data-stu-id="9b965-110">When you use the **\[explicit\_handle\]** attribute, each procedure has a primitive handle as its first parameter even if the IDL file does not contain this handle in its parameter list.</span></span> <span data-ttu-id="9b965-111">Los prototipos emitidos para el archivo de encabezado y las rutinas de código auxiliar contienen el parámetro adicional, y ese parámetro se usa como identificador para dirigir la llamada remota.</span><span class="sxs-lookup"><span data-stu-id="9b965-111">The prototypes emitted to the header file and stub routines contain the additional parameter, and that parameter is used as the handle for directing the remote call.</span></span>

<span data-ttu-id="9b965-112">El atributo de **\[ \_ identificador \] explícito** afecta tanto a los procedimientos remotos como a los procedimientos de serialización.</span><span class="sxs-lookup"><span data-stu-id="9b965-112">The **\[explicit\_handle\]** attribute affects both remote procedures and serialization procedures.</span></span> <span data-ttu-id="9b965-113">Para la serialización de tipos, las rutinas de soporte se generan con el parámetro inicial como un identificador explícito (serialización).</span><span class="sxs-lookup"><span data-stu-id="9b965-113">For type serialization, the support routines are generated with the initial parameter as an explicit (serialization) handle.</span></span> <span data-ttu-id="9b965-114">Si no se utiliza el atributo de **\[ \_ identificador \] explícito** , la aplicación puede seguir especificando que una operación tiene un identificador explícito (enlace o serialización) que dirige la llamada.</span><span class="sxs-lookup"><span data-stu-id="9b965-114">If the **\[explicit\_handle\]** attribute is not used, the application can still specify that an operation have an explicit handle (binding or serialization) directing the call.</span></span> <span data-ttu-id="9b965-115">Para ello, se proporciona un prototipo con un argumento que contiene un tipo de identificador al archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="9b965-115">To do this, a prototype with an argument containing a handle type is supplied to the IDL file.</span></span> <span data-ttu-id="9b965-116">Tenga en cuenta que en el modo predeterminado, un argumento que no aparece en primer lugar también se puede usar como un identificador que dirige la llamada.</span><span class="sxs-lookup"><span data-stu-id="9b965-116">Note that in default mode, an argument that does not appear first can also be used as a handle directing the call.</span></span>

<span data-ttu-id="9b965-117">Por lo tanto, mientras que el atributo de **\[ \_ identificador \] explícito** es una forma de asignar al prototipo IDL un atributo de **\[ \_ identificador \] explícito** primitivo, no requiere necesariamente un cambio en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="9b965-117">Therefore, while the **\[explicit\_handle\]** attribute is a way of giving the IDL prototype a primitive **\[explicit\_handle\]** attribute, it does not necessarily require a change to the IDL file.</span></span> <span data-ttu-id="9b965-118">En el modo [**/OSF**](-osf.md) , solo se puede usar el primer argumento como un tipo de identificador explícito.</span><span class="sxs-lookup"><span data-stu-id="9b965-118">In [**/osf**](-osf.md) mode only the first argument can be used as an explicit handle type.</span></span>

<span data-ttu-id="9b965-119">El atributo de **\[ \_ identificador \] explícito** se puede usar como un atributo de interfaz o un atributo de operación.</span><span class="sxs-lookup"><span data-stu-id="9b965-119">The **\[explicit\_handle\]** attribute can be used as either an interface attribute or an operation attribute.</span></span> <span data-ttu-id="9b965-120">Como atributo de interfaz, afecta a todas las operaciones de la interfaz y a todos los tipos que requieren compatibilidad con la serialización.</span><span class="sxs-lookup"><span data-stu-id="9b965-120">As an interface attribute, it affects all the operations in the interface and all the types that require serialization support.</span></span> <span data-ttu-id="9b965-121">Sin embargo, si se usa como atributo de operación, solo afecta a esa operación concreta.</span><span class="sxs-lookup"><span data-stu-id="9b965-121">If, however, it is used as an operation attribute, it affects only that particular operation.</span></span> <span data-ttu-id="9b965-122">Si un método contiene uno o más \[ \] identificadores de contexto, se usa la parte más a la izquierda \[ en \] el identificador de contexto como identificador de enlace y no se crea ningún identificador explícito adicional.</span><span class="sxs-lookup"><span data-stu-id="9b965-122">If a method contains one or more \[in\] context handles, the left most \[in\] context handle is used as the binding handle, and no additional explicit handle is created.</span></span>

## <a name="examples"></a><span data-ttu-id="9b965-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9b965-123">Examples</span></span>

``` syntax
/* ACF File */ 
[
    explicit_handle
] 
interface iface
{ 
    // Interface definition statements.
};
```

## <a name="see-also"></a><span data-ttu-id="9b965-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b965-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b965-125">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="9b965-125">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="9b965-126">**\_identificador automático**</span><span class="sxs-lookup"><span data-stu-id="9b965-126">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="9b965-127">**\_identificador implícito**</span><span class="sxs-lookup"><span data-stu-id="9b965-127">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="9b965-128">**/osf**</span><span class="sxs-lookup"><span data-stu-id="9b965-128">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 




