---
title: atributo encode
description: El atributo \ encode \ ACF especifica que un procedimiento o un tipo de datos necesita compatibilidad de serialización.
ms.assetid: 2661021d-8a26-4216-935b-ca40b6f8b9ec
keywords:
- codificar el atributo MIDL
topic_type:
- apiref
api_name:
- encode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2a35c6d6910229a9e14026f6727db5c3176050
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995135"
---
# <a name="encode-attribute"></a><span data-ttu-id="d4e59-104">atributo encode</span><span class="sxs-lookup"><span data-stu-id="d4e59-104">encode attribute</span></span>

<span data-ttu-id="d4e59-105">El atributo **\[ encode \]** ACF especifica que un procedimiento o un tipo de datos necesita compatibilidad de serialización.</span><span class="sxs-lookup"><span data-stu-id="d4e59-105">The **\[encode\]** ACF attribute specifies that a procedure or a data type needs serialization support.</span></span>

``` syntax
[ 
    encode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ encode [ , op-attribute-list] ] proc-name

typedef [encode [ , type-attribute-list] ] type-name
```

## <a name="parameters"></a><span data-ttu-id="d4e59-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4e59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4e59-107">*interfaz-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="d4e59-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d4e59-108">Especifica otros atributos que se aplican a la interfaz en conjunto.</span><span class="sxs-lookup"><span data-stu-id="d4e59-108">Specifies other attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="d4e59-109">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="d4e59-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d4e59-110">Especifica el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="d4e59-110">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="d4e59-111">*definición de interfaz*</span><span class="sxs-lookup"><span data-stu-id="d4e59-111">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="d4e59-112">Especifica las instrucciones IDL que forman la definición de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="d4e59-112">Specifies IDL statements which form the definition of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="d4e59-113">*OP-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="d4e59-113">*op-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d4e59-114">Especifica otros atributos operativos que se aplican al procedimiento como **\[** [**descodificar**](decode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="d4e59-114">Specifies other operational attributes that apply to the procedure such as **\[**[**decode**](decode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="d4e59-115">*proc: nombre*</span><span class="sxs-lookup"><span data-stu-id="d4e59-115">*proc-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d4e59-116">Especifica el nombre del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="d4e59-116">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="d4e59-117">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="d4e59-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d4e59-118">Especifica otros atributos que se aplican al tipo, como **\[** [**Decode**](decode.md) **\]** y **\[** [**allocate**](allocate.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="d4e59-118">Specifies other attributes that apply to the type such as **\[**[**decode**](decode.md)**\]** and **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="d4e59-119">*nombre de tipo*</span><span class="sxs-lookup"><span data-stu-id="d4e59-119">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d4e59-120">Especifica un tipo definido en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="d4e59-120">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4e59-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4e59-121">Remarks</span></span>

<span data-ttu-id="d4e59-122">El atributo **\[ encode \]** hace que el compilador MIDL genere código que una aplicación puede utilizar para serializar los datos en un búfer.</span><span class="sxs-lookup"><span data-stu-id="d4e59-122">The **\[encode\]** attribute causes the MIDL compiler to generate code that an application can use to serialize data into a buffer.</span></span> <span data-ttu-id="d4e59-123">El **\[** atributo [**Decode**](decode.md) **\]** genera el código para calcular las referencias de los datos de un búfer.</span><span class="sxs-lookup"><span data-stu-id="d4e59-123">The **\[**[**decode**](decode.md)**\]** attribute generates the code for unmarshaling data from a buffer.</span></span>

<span data-ttu-id="d4e59-124">Use los atributos **\[ encode \]** y **\[** [**Decode**](decode.md) **\]** en un ACF para generar código de serialización para los procedimientos o tipos definidos en el archivo IDL de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="d4e59-124">Use the **\[encode\]** and **\[**[**decode**](decode.md)**\]** attributes in an ACF to generate serialization code for procedures or types defined in the IDL file of an interface.</span></span> <span data-ttu-id="d4e59-125">Cuando se usa como atributo de interfaz, **\[ encode \]** se aplica a todos los tipos y procedimientos definidos en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="d4e59-125">When used as an interface attribute, **\[encode\]** applies to all the types and procedures defined in the IDL file.</span></span> <span data-ttu-id="d4e59-126">Cuando se usa como atributo operativo, **\[ encode \]** solo se aplica al procedimiento especificado.</span><span class="sxs-lookup"><span data-stu-id="d4e59-126">When used as an operational attribute, **\[encode\]** applies only to the specified procedure.</span></span> <span data-ttu-id="d4e59-127">Cuando se usa como atributo de tipo, **\[ encode \]** solo se aplica al tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="d4e59-127">When used as a type attribute, **\[encode\]** applies only to the specified type.</span></span>

<span data-ttu-id="d4e59-128">Cuando se aplica el atributo de **\[ codificación \]** o **\[** [**descodificación**](decode.md) **\]** a un procedimiento, el compilador MIDL genera un código auxiliar de serialización de forma similar a como se generan los códigos auxiliares remotos para las rutinas remotas.</span><span class="sxs-lookup"><span data-stu-id="d4e59-128">When the **\[encode\]** or **\[**[**decode**](decode.md)**\]** attribute is applied to a procedure, the MIDL compiler generates a serialization stub in a similar fashion as remote stubs are generated for remote routines.</span></span> <span data-ttu-id="d4e59-129">Un procedimiento puede ser un procedimiento remoto o de serialización, pero no puede ser ambos.</span><span class="sxs-lookup"><span data-stu-id="d4e59-129">A procedure can be either a remote or a serializing procedure, but it cannot be both.</span></span> <span data-ttu-id="d4e59-130">El prototipo de la rutina generada se envía al código auxiliar. H mientras el propio código auxiliar entra en el \_ archivo stub c. c.</span><span class="sxs-lookup"><span data-stu-id="d4e59-130">The prototype of the generated routine is sent to the STUB.H file while the stub itself goes into the STUB\_C.C file.</span></span>

<span data-ttu-id="d4e59-131">El compilador MIDL genera dos funciones para cada tipo al que se aplica el atributo **\[ \] encode** y una función adicional para cada tipo al **\[** que se aplica el atributo [**descode**](decode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="d4e59-131">The MIDL compiler generates two functions for each type the **\[encode\]** attribute applies to, and one additional function for each type the **\[**[**decode**](decode.md)**\]** attribute applies to.</span></span> <span data-ttu-id="d4e59-132">Por ejemplo, para un tipo definido por el usuario denominado mi tipo, el compilador genera código para las \_ funciones de codificación, \_ descodificación y tipo \_ AlignSize.</span><span class="sxs-lookup"><span data-stu-id="d4e59-132">For example, for a user-defined type named MyType, the compiler generates code for the MyType\_Encode, MyType\_Decode, and MyType\_AlignSize functions.</span></span> <span data-ttu-id="d4e59-133">Para estas funciones, el compilador escribe prototipos en STUB. H y código fuente para STUB \_ C.C.</span><span class="sxs-lookup"><span data-stu-id="d4e59-133">For these functions, the compiler writes prototypes to STUB.H and source code to STUB\_C.C.</span></span>

<span data-ttu-id="d4e59-134">Para obtener más información sobre los identificadores de serialización y la codificación o descodificación de datos, vea [servicios de serialización](/windows/desktop/Rpc/serialization-services).</span><span class="sxs-lookup"><span data-stu-id="d4e59-134">For additional information about serialization handles and encoding or decoding data, see [Serialization Services](/windows/desktop/Rpc/serialization-services).</span></span>

## <a name="examples"></a><span data-ttu-id="d4e59-135">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d4e59-135">Examples</span></span>

``` syntax
/* 
    ACF file example; 
    Assumes MyType1, MyType2, MyType3, MyProc1, MyProc2, MyProc3 defined 
    in IDL file  
    MyType1, MyType2, MyProc1, MyProc2 have encode and decode 
    serialization support 
    MyType3 and MyProc3 have encode serialization support only 
*/ 
[ 
    encode, 
    implicit_handle(handle_t bh) 
]    
interface regress 
{ 
    typedef [ decode ] MyType1; 
    typedef [ encode, decode ] MyType2; 
    [ decode ] MyProcc1(); 
    [ encode ] MyProc2(); 
}
```

## <a name="see-also"></a><span data-ttu-id="d4e59-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4e59-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4e59-137">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="d4e59-137">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="d4e59-138">**allocate**</span><span class="sxs-lookup"><span data-stu-id="d4e59-138">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="d4e59-139">**descodificar**</span><span class="sxs-lookup"><span data-stu-id="d4e59-139">**decode**</span></span>](decode.md)
</dt> </dl>

 

 