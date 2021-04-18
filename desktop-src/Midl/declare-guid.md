---
title: palabra clave declare_guid
description: La \_ palabra clave declare GUID indica a MIDL que emita una variable GUID en el archivo de encabezado generado.
keywords:
- palabra clave declare_guid MIDL
topic_type:
- apiref
api_name:
- declare_guid
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 495acd64e79544d067ff124a88289219919a7fb6
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "105721321"
---
# <a name="declare_guid-keyword"></a><span data-ttu-id="667c4-104">declare la \_ palabra clave GUID</span><span class="sxs-lookup"><span data-stu-id="667c4-104">declare\_guid keyword</span></span>

<span data-ttu-id="667c4-105">La palabra clave **declare \_ GUID** indica a MIDL que emita una variable GUID en el archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="667c4-105">The **declare\_guid** keyword instructs MIDL to emit a GUID variable into the generated header file.</span></span>

``` syntax
declare_guid(variable-name, guid)
```

## <a name="parameters"></a><span data-ttu-id="667c4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="667c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="667c4-107">*nombre-variable*</span><span class="sxs-lookup"><span data-stu-id="667c4-107">*variable-name*</span></span> 
</dt> <dd>

<span data-ttu-id="667c4-108">Especifica un nombre de variable para el identificador en el archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="667c4-108">Specifies a variable name for the identifier in the generated header file.</span></span>

</dd> <dt>

<span data-ttu-id="667c4-109">*guid*</span><span class="sxs-lookup"><span data-stu-id="667c4-109">*guid*</span></span>
</dt> <dd>

<span data-ttu-id="667c4-110">Especifica el [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) que se aplicará al nombre de variable en el archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="667c4-110">Specifies the [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) that will apply to the variable name in the generated header file.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="667c4-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="667c4-111">Examples</span></span>

``` syntax
declare_guid(SID_Widget, 5144C348-169E-4359-A79D-5482461D9929)  
```

## <a name="remarks"></a><span data-ttu-id="667c4-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="667c4-112">Remarks</span></span>

<span data-ttu-id="667c4-113">`declare_guid`El uso de es equivalente al uso de `cpp_quote` para generar una invocación de la `EXTERN_GUID` macro.</span><span class="sxs-lookup"><span data-stu-id="667c4-113">Using `declare_guid` is equivalent to using `cpp_quote` to generate an invocation of the `EXTERN_GUID` macro.</span></span>

<span data-ttu-id="667c4-114">En el ejemplo anterior se obtiene el siguiente resultado:</span><span class="sxs-lookup"><span data-stu-id="667c4-114">The above example results in the following output:</span></span>

```C
cpp_quote("EXTERN_GUID(SID_Widget, 0x5144c348, 0x169e, 0x4359, 0xa7, 0x9d, 0x54, 0x82, 0x46, 0x1d, 0x99, 0x29);")
```

<span data-ttu-id="667c4-115">La `declare_guid` instrucción se proporciona por comodidad.</span><span class="sxs-lookup"><span data-stu-id="667c4-115">The `declare_guid` statement is provided as a convenience.</span></span> <span data-ttu-id="667c4-116">Tiene la ventaja de usar la misma sintaxis GUID que el [ `uuid` atributo](uuid.md).</span><span class="sxs-lookup"><span data-stu-id="667c4-116">It has the advantage of using the same GUID syntax as the [`uuid` attribute](uuid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="667c4-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="667c4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="667c4-118">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="667c4-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="667c4-119">**cpp_quote**</span><span class="sxs-lookup"><span data-stu-id="667c4-119">**cpp_quote**</span></span>](cpp-quote.md)
</dt> <dt>

[<span data-ttu-id="667c4-120">**uuid (atributo)**</span><span class="sxs-lookup"><span data-stu-id="667c4-120">**uuid attribute**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="667c4-121">**Estructura GUID**</span><span class="sxs-lookup"><span data-stu-id="667c4-121">**GUID structure**</span></span>](/windows/win32/api/guiddef/ns-guiddef-guid)
</dt> </dl>
