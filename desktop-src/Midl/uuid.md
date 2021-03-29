---
title: uuid (atributo)
description: El atributo \ UUID \ interface designa un identificador único universal (UUID) que se asigna a la interfaz y que lo distingue de otras interfaces.
ms.assetid: 72cf12f5-49cd-440d-9665-73211509d050
keywords:
- atributo de UUID (MIDL)
topic_type:
- apiref
api_name:
- uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5688bafe8343bdc1ab508a4e65984cc15c88b124
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784072"
---
# <a name="uuid-attribute"></a><span data-ttu-id="f81e8-104">uuid (atributo)</span><span class="sxs-lookup"><span data-stu-id="f81e8-104">uuid attribute</span></span>

<span data-ttu-id="f81e8-105">El atributo **\[ UUID \]** interface designa un identificador único universal (UUID) que se asigna a la interfaz y que lo distingue de otras interfaces.</span><span class="sxs-lookup"><span data-stu-id="f81e8-105">The **\[uuid\]** interface attribute designates a universally unique identifier (UUID) that is assigned to the interface and that distinguishes it from other interfaces.</span></span>

``` syntax
uuid (string-uuid) 
uuid ("string-uuid")
```

## <a name="parameters"></a><span data-ttu-id="f81e8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f81e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f81e8-107">*cadena: UUID*</span><span class="sxs-lookup"><span data-stu-id="f81e8-107">*string-uuid*</span></span> 
</dt> <dd>

<span data-ttu-id="f81e8-108">Especifica una cadena que consta de 8 dígitos hexadecimales seguidos de un guion y, a continuación, tres grupos de 4 dígitos hexadecimales, seguidos de un guion y 12 dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="f81e8-108">Specifies a string consisting of 8 hexadecimal digits followed by a hyphen, then three groups of 4 hexadecimal digits each followed by a hyphen, then 12 hexadecimal digits.</span></span> <span data-ttu-id="f81e8-109">Puede incluir la cadena UUID entre comillas, excepto cuando se usa el modificador de compilador MIDL [**/OSF**](-osf.md).</span><span class="sxs-lookup"><span data-stu-id="f81e8-109">You can enclose the UUID string in quotes, except when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f81e8-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f81e8-110">Remarks</span></span>

<span data-ttu-id="f81e8-111">La biblioteca en tiempo de ejecución utiliza el UUID de la interfaz que el atributo **\[ UUID \]** designa para ayudar a establecer la comunicación entre las aplicaciones cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="f81e8-111">The run-time library uses the interface UUID that the **\[uuid\]** attribute designates to help establish communication between the client and server applications.</span></span> <span data-ttu-id="f81e8-112">El atributo **\[ UUID \]** puede aparecer en la lista de atributos de interfaz para una interfaz RPC o una interfaz com.</span><span class="sxs-lookup"><span data-stu-id="f81e8-112">The **\[uuid\]** attribute can appear in the interface attribute list for either an RPC interface or a COM interface.</span></span>

<span data-ttu-id="f81e8-113">En el caso de una interfaz RPC, la lista de atributos de interfaz debe incluir el atributo **\[ UUID \]** o el **\[** [](local.md) **\]** atributo local y el que elija debe aparecer exactamente una vez.</span><span class="sxs-lookup"><span data-stu-id="f81e8-113">For an RPC interface, the interface attribute list must include either the **\[uuid\]** attribute or the **\[**[**local**](local.md)**\]** attribute, and the one you choose must occur exactly once.</span></span> <span data-ttu-id="f81e8-114">Si la lista incluye el atributo **\[ UUID \]** , también puede incluir el atributo **\[** [**version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="f81e8-114">If the list includes the **\[uuid\]** attribute, it can also include the **\[**[**version**](version.md)**\]** attribute.</span></span>

<span data-ttu-id="f81e8-115">En el caso de una interfaz COM (identificada por el atributo de la interfaz de **\[** [**objeto**](object.md) **\]** ), la lista de atributos de interfaz debe incluir el atributo de **\[ UUID \]** , pero no puede incluir el atributo de **\[ versión \]** .</span><span class="sxs-lookup"><span data-stu-id="f81e8-115">For a COM interface (identified by the **\[**[**object**](object.md)**\]** interface attribute), the interface attribute list must include the **\[uuid\]** attribute, but it cannot include the **\[version\]** attribute.</span></span> <span data-ttu-id="f81e8-116">La lista de una interfaz COM puede incluir el atributo **\[ local \]** aunque el atributo **\[ UUID \]** esté presente.</span><span class="sxs-lookup"><span data-stu-id="f81e8-116">The list for a COM interface can include the **\[local\]** attribute even though the **\[uuid\]** attribute is present.</span></span>

<span data-ttu-id="f81e8-117">Microsoft RPC es compatible con una extensión de DCE IDL que permite escribir el UUID entre comillas dobles ("" ").</span><span class="sxs-lookup"><span data-stu-id="f81e8-117">Microsoft RPC supports an extension to DCE IDL that allows the UUID to be enclosed in double quotation marks ("" "").</span></span> <span data-ttu-id="f81e8-118">El formulario entrecomillado es necesario para los preprocesadores del compilador de C que interpretan los números de UUID como números de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="f81e8-118">The quoted form is needed for C-compiler preprocessors that interpret UUID numbers as floating-point numbers.</span></span>

<span data-ttu-id="f81e8-119">Todos los valores UUID deben ser generados por el equipo para garantizar la exclusividad.</span><span class="sxs-lookup"><span data-stu-id="f81e8-119">All UUID values should be computer-generated to guarantee uniqueness.</span></span> <span data-ttu-id="f81e8-120">Use la utilidad uuidgen para generar valores únicos de UUID.</span><span class="sxs-lookup"><span data-stu-id="f81e8-120">Use the Uuidgen utility to generate unique UUID values.</span></span>

<span data-ttu-id="f81e8-121">El UUID y los números de versión de la interfaz se usan para determinar si el cliente puede enlazar con el servidor.</span><span class="sxs-lookup"><span data-stu-id="f81e8-121">The UUID and version numbers of the interface are used to determine whether the client can bind to the server.</span></span> <span data-ttu-id="f81e8-122">Para que el cliente se enlace al servidor, el UUID especificado en las interfaces de cliente y de servidor debe ser el mismo.</span><span class="sxs-lookup"><span data-stu-id="f81e8-122">For the client to bind to the server, the UUID specified in the client and server interfaces must be the same.</span></span>

<span data-ttu-id="f81e8-123">Tenga en cuenta que una interfaz sin atributos se puede importar en un archivo IDL base.</span><span class="sxs-lookup"><span data-stu-id="f81e8-123">Note that an interface without attributes can be imported into a base IDL file.</span></span> <span data-ttu-id="f81e8-124">Sin embargo, la interfaz debe contener solo tipos de contenido sin procedimientos.</span><span class="sxs-lookup"><span data-stu-id="f81e8-124">However, the interface must contain only datatypes with no procedures.</span></span> <span data-ttu-id="f81e8-125">Si hay un procedimiento incluido en la interfaz, se debe especificar un atributo local o UUID.</span><span class="sxs-lookup"><span data-stu-id="f81e8-125">If even one procedure is contained in the interface, a local or UUID attribute must be specified.</span></span>

## <a name="examples"></a><span data-ttu-id="f81e8-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f81e8-126">Examples</span></span>

``` syntax
uuid(6B29FC40-CA47-1067-B31D-00DD010662DA) 
 
uuid("6B29FC40-CA47-1067-B31D-00DD010662DA")
```

## <a name="see-also"></a><span data-ttu-id="f81e8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f81e8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f81e8-128">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="f81e8-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="f81e8-129">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="f81e8-129">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="f81e8-130">**localizar**</span><span class="sxs-lookup"><span data-stu-id="f81e8-130">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="f81e8-131">**objeto**</span><span class="sxs-lookup"><span data-stu-id="f81e8-131">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="f81e8-132">**/osf**</span><span class="sxs-lookup"><span data-stu-id="f81e8-132">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="f81e8-133">**Versión**</span><span class="sxs-lookup"><span data-stu-id="f81e8-133">**version**</span></span>](version.md)
</dt> </dl>

 

 




