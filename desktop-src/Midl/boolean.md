---
title: Atributo booleano
description: La palabra clave Boolean indica que la expresión o expresión constante asociada con el identificador solo toma los valores TRUE y FALSE.
ms.assetid: ed3b00a4-880f-4674-9f6d-8f5faf1eea66
keywords:
- Atributo booleano MIDL
topic_type:
- apiref
api_name:
- boolean
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68959cabcef1f439ffb6df30b77aeee7056f4fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419617"
---
# <a name="boolean-attribute"></a><span data-ttu-id="99947-104">Atributo booleano</span><span class="sxs-lookup"><span data-stu-id="99947-104">boolean attribute</span></span>

<span data-ttu-id="99947-105">La palabra clave **Boolean** indica que la expresión o expresión constante asociada con el identificador solo toma los valores **true** y **false**.</span><span class="sxs-lookup"><span data-stu-id="99947-105">The keyword **boolean** indicates that the expression or constant expression associated with the identifier takes only the values **TRUE** and **FALSE**.</span></span>

``` syntax
boolean identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="99947-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99947-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99947-107">*identificador: nombre*</span><span class="sxs-lookup"><span data-stu-id="99947-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="99947-108">Especifica un identificador de MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="99947-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="99947-109">Los identificadores de MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado, y deben comenzar por un carácter alfabético o de subrayado.</span><span class="sxs-lookup"><span data-stu-id="99947-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99947-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99947-110">Remarks</span></span>

<span data-ttu-id="99947-111">El tipo **booleano** es uno de los tipos base del lenguaje IDL.</span><span class="sxs-lookup"><span data-stu-id="99947-111">The **boolean** type is one of the base types of the IDL language.</span></span> <span data-ttu-id="99947-112">El tipo **Boolean** puede aparecer como un especificador de tipo en declaraciones [**const**](const.md) , declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como un especificador de tipo de valor devuelto de función y como especificador de tipo de parámetro).</span><span class="sxs-lookup"><span data-stu-id="99947-112">The **boolean** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="99947-113">Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="99947-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

> [!Note]  
> <span data-ttu-id="99947-114">El tipo base **booleano** no es compatible con el atributo [**oleautomation**](oleautomation.md) .</span><span class="sxs-lookup"><span data-stu-id="99947-114">The **boolean** base type is not compatible with the [**oleautomation**](oleautomation.md) attribute.</span></span> <span data-ttu-id="99947-115">Use VARIANT \_ bool en las interfaces compatibles con Automation.</span><span class="sxs-lookup"><span data-stu-id="99947-115">Use VARIANT\_BOOL in your Automation-compatible interfaces.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="99947-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="99947-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99947-117">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="99947-117">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="99947-118">**const**</span><span class="sxs-lookup"><span data-stu-id="99947-118">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="99947-119">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="99947-119">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="99947-120">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="99947-120">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="99947-121">**typedef**</span><span class="sxs-lookup"><span data-stu-id="99947-121">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




