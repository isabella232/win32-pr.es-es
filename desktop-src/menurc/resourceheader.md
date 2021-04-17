---
title: Estructura RESOURCEHEADER
description: Contiene información sobre el propio encabezado de recursos y los datos específicos de este recurso.
ms.assetid: e0eba7b3-a275-4ffe-9347-46361213cf48
keywords:
- Menús de la estructura RESOURCEHEADER y otros recursos
topic_type:
- apiref
api_name:
- RESOURCEHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41b436ebd6aeb5dc31f8ed773fbe7b12a1586185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714554"
---
# <a name="resourceheader-structure"></a><span data-ttu-id="1927d-104">Estructura RESOURCEHEADER</span><span class="sxs-lookup"><span data-stu-id="1927d-104">RESOURCEHEADER structure</span></span>

<span data-ttu-id="1927d-105">Contiene información sobre el propio encabezado de recursos y los datos específicos de este recurso.</span><span class="sxs-lookup"><span data-stu-id="1927d-105">Contains information about the resource header itself and the data specific to this resource.</span></span> <span data-ttu-id="1927d-106">Esta estructura no es una verdadera estructura de lenguaje C, porque contiene miembros de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="1927d-106">This structure is not a true C-language structure, because it contains variable-length members.</span></span> <span data-ttu-id="1927d-107">La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.</span><span class="sxs-lookup"><span data-stu-id="1927d-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1927d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1927d-108">Syntax</span></span>


```C++
typedef struct {
  DWORD DataSize;
  DWORD HeaderSize;
  DWORD TYPE;
  DWORD NAME;
  DWORD DataVersion;
  WORD  MemoryFlags;
  WORD  LanguageId;
  DWORD Version;
  DWORD Characteristics;
} RESOURCEHEADER;
```



## <a name="members"></a><span data-ttu-id="1927d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="1927d-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="1927d-110">**DataSize**</span><span class="sxs-lookup"><span data-stu-id="1927d-110">**DataSize**</span></span>
</dt> <dd>

<span data-ttu-id="1927d-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1927d-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1927d-112">Tamaño, en bytes, de los datos que siguen al encabezado de recursos para este recurso concreto.</span><span class="sxs-lookup"><span data-stu-id="1927d-112">The size, in bytes, of the data that follows the resource header for this particular resource.</span></span> <span data-ttu-id="1927d-113">No incluye ningún relleno de archivos entre este recurso y cualquier recurso que lo siga en el archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1927d-113">It does not include any file padding between this resource and any resource that follows it in the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="1927d-114">**HeaderSize**</span><span class="sxs-lookup"><span data-stu-id="1927d-114">**HeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="1927d-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1927d-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1927d-116">Tamaño, en bytes, de los datos del encabezado de recursos que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="1927d-116">The size, in bytes, of the resource header data that follows.</span></span>

</dd> <dt>

<span data-ttu-id="1927d-117">**TYPE**</span><span class="sxs-lookup"><span data-stu-id="1927d-117">**TYPE**</span></span>
</dt> <dd>

<span data-ttu-id="1927d-118">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1927d-118">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1927d-119">El tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="1927d-119">The resource type.</span></span> <span data-ttu-id="1927d-120">El miembro de **tipo** puede ser un valor numérico o una cadena Unicode terminada en null que especifica el nombre del tipo.</span><span class="sxs-lookup"><span data-stu-id="1927d-120">The **TYPE** member can either be a numeric value or a null-terminated Unicode string that specifies the name of the type.</span></span> <span data-ttu-id="1927d-121">Vea la siguiente sección de comentarios para obtener una descripción de los miembros de **nombre** o de tipo **ordinal** .</span><span class="sxs-lookup"><span data-stu-id="1927d-121">See the following Remarks section for a description of **Name** or **Ordinal** type members.</span></span>

<span data-ttu-id="1927d-122">Si el miembro de **tipo** es un valor numérico, puede especificar un tipo de recurso estándar o definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="1927d-122">If the **TYPE** member is a numeric value, it can specify either a standard or a user-defined resource type.</span></span> <span data-ttu-id="1927d-123">Si el miembro es una cadena, se trata de un tipo de recurso definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="1927d-123">If the member is a string, then it is a user-defined resource type.</span></span> <span data-ttu-id="1927d-124">Para obtener una lista de los tipos de recursos predefinidos, consulte [tipos de recursos](/windows/desktop/menurc/resource-types).</span><span class="sxs-lookup"><span data-stu-id="1927d-124">For a list of the predefined resource types, see [Resource Types](/windows/desktop/menurc/resource-types).</span></span>

<span data-ttu-id="1927d-125">Los valores inferiores a 256 se reservan para uso del sistema.</span><span class="sxs-lookup"><span data-stu-id="1927d-125">Values less than 256 are reserved for system use.</span></span>

</dd> <dt>

<span data-ttu-id="1927d-126">**NOMBRE**</span><span class="sxs-lookup"><span data-stu-id="1927d-126">**NAME**</span></span>
</dt> <dd>

<span data-ttu-id="1927d-127">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1927d-127">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1927d-128">Nombre que identifica el recurso en particular.</span><span class="sxs-lookup"><span data-stu-id="1927d-128">A name that identifies the particular resource.</span></span> <span data-ttu-id="1927d-129">El miembro de **nombre** , al igual que el miembro de **tipo** , puede ser un valor numérico o una cadena Unicode terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="1927d-129">The **NAME** member, like the **TYPE** member, can either be a numeric value or a null-terminated Unicode string.</span></span> <span data-ttu-id="1927d-130">Vea la siguiente sección de comentarios para obtener una descripción de los miembros de **nombre** o de tipo **ordinal** .</span><span class="sxs-lookup"><span data-stu-id="1927d-130">See the following Remarks section for a description of **Name** or **Ordinal** type members.</span></span>

<span data-ttu-id="1927d-131">No es necesario agregar relleno para la alineación **DWORD** entre los miembros **Type** y **Name** porque contienen datos de **Word** .</span><span class="sxs-lookup"><span data-stu-id="1927d-131">You do not need to add padding for **DWORD** alignment between the **TYPE** and **NAME** members because they contain **WORD** data.</span></span> <span data-ttu-id="1927d-132">Sin embargo, puede que tenga que agregar una **palabra** de relleno después del miembro de **nombre** para alinear el resto del encabezado en los límites de **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="1927d-132">However, you may need to add a **WORD** of padding after the **NAME** member to align the rest of the header on **DWORD** boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="1927d-133">**DataVersion**</span><span class="sxs-lookup"><span data-stu-id="1927d-133">**DataVersion**</span></span>
</dt> <dd>

<span data-ttu-id="1927d-134">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1927d-134">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1927d-135">Una versión de datos de recursos predefinida.</span><span class="sxs-lookup"><span data-stu-id="1927d-135">A predefined resource data version.</span></span> <span data-ttu-id="1927d-136">Esto determinará qué versión de los datos de recursos debe usar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1927d-136">This will determine which version of the resource data the application should use.</span></span>

</dd> <dt>

<span data-ttu-id="1927d-137">**MemoryFlags**</span><span class="sxs-lookup"><span data-stu-id="1927d-137">**MemoryFlags**</span></span>
</dt> <dd>

<span data-ttu-id="1927d-138">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="1927d-138">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1927d-139">Un conjunto de marcas de atributo que pueden describir el estado del recurso.</span><span class="sxs-lookup"><span data-stu-id="1927d-139">A set of attribute flags that can describe the state of the resource.</span></span> <span data-ttu-id="1927d-140">Modificadores de. Archivo de script RC asigne estos atributos al recurso.</span><span class="sxs-lookup"><span data-stu-id="1927d-140">Modifiers in the .RC script file assign these attributes to the resource.</span></span> <span data-ttu-id="1927d-141">Los identificadores de script pueden asignar los siguientes valores de marca.</span><span class="sxs-lookup"><span data-stu-id="1927d-141">The script identifiers can assign the following flag values.</span></span>

<span data-ttu-id="1927d-142">Las aplicaciones no usan ninguno de estos atributos.</span><span class="sxs-lookup"><span data-stu-id="1927d-142">Applications do not use any of these attributes.</span></span> <span data-ttu-id="1927d-143">Los atributos se permiten en el script para la compatibilidad con versiones anteriores de los scripts existentes, pero se omiten.</span><span class="sxs-lookup"><span data-stu-id="1927d-143">The attributes are permitted in the script for backward compatibility with existing scripts, but they are ignored.</span></span> <span data-ttu-id="1927d-144">Los recursos se cargan cuando se carga el módulo correspondiente y se liberan cuando se descarga el módulo.</span><span class="sxs-lookup"><span data-stu-id="1927d-144">Resources are loaded when the corresponding module is loaded, and are freed when the module is unloaded.</span></span>

<dt>

<span id="MOVEABLE"></span><span id="moveable"></span>

<span data-ttu-id="1927d-145">**Móvil** (0x0010)</span><span class="sxs-lookup"><span data-stu-id="1927d-145">**MOVEABLE** (0x0010)</span></span>


</dt> <dd></dd> <dt>

<span id="FIXED"></span><span id="fixed"></span>

<span data-ttu-id="1927d-146">**corregido** (~ movible)</span><span class="sxs-lookup"><span data-stu-id="1927d-146">**FIXED** (~MOVEABLE)</span></span>


</dt> <dd></dd> <dt>

<span id="PURE"></span><span id="pure"></span>

<span data-ttu-id="1927d-147">**Puro** (0x0020)</span><span class="sxs-lookup"><span data-stu-id="1927d-147">**PURE** (0x0020)</span></span>


</dt> <dd></dd> <dt>

<span id="IMPURE"></span><span id="impure"></span>

<span data-ttu-id="1927d-148">**IMpurar** (~ puro)</span><span class="sxs-lookup"><span data-stu-id="1927d-148">**IMPURE** (~PURE)</span></span>


</dt> <dd></dd> <dt>

<span id="PRELOAD"></span><span id="preload"></span>

<span data-ttu-id="1927d-149">**Carga previa** (0x0040)</span><span class="sxs-lookup"><span data-stu-id="1927d-149">**PRELOAD** (0x0040)</span></span>


</dt> <dd></dd> <dt>

<span id="LOADONCALL"></span><span id="loadoncall"></span>

<span data-ttu-id="1927d-150">**LOADONCALL** (~ preload)</span><span class="sxs-lookup"><span data-stu-id="1927d-150">**LOADONCALL** (~PRELOAD)</span></span>


</dt> <dd></dd> <dt>

<span id="DISCARDABLE"></span><span id="discardable"></span>

<span data-ttu-id="1927d-151">**DEScartable** (0x1000)</span><span class="sxs-lookup"><span data-stu-id="1927d-151">**DISCARDABLE** (0x1000)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="1927d-152">**LanguageId**</span><span class="sxs-lookup"><span data-stu-id="1927d-152">**LanguageId**</span></span>
</dt> <dd>

<span data-ttu-id="1927d-153">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="1927d-153">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1927d-154">Lenguaje del recurso o conjunto de recursos.</span><span class="sxs-lookup"><span data-stu-id="1927d-154">The language for the resource or set of resources.</span></span> <span data-ttu-id="1927d-155">Establezca el valor de este miembro con la instrucción de definición de recursos de [lenguaje](./language-statement.md) opcional.</span><span class="sxs-lookup"><span data-stu-id="1927d-155">Set the value for this member with the optional [LANGUAGE](./language-statement.md) resource definition statement.</span></span> <span data-ttu-id="1927d-156">Los parámetros son constantes del archivo winnt. h.</span><span class="sxs-lookup"><span data-stu-id="1927d-156">The parameters are constants from the Winnt.h file.</span></span>

<span data-ttu-id="1927d-157">Cada recurso incluye un identificador de idioma, por lo que el sistema o la aplicación pueden seleccionar un idioma adecuado para la configuración regional actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="1927d-157">Each resource includes a language identifier so the system or application can select a language appropriate for the current locale of the system.</span></span> <span data-ttu-id="1927d-158">Si hay varios recursos del mismo tipo y nombre que solo difieren en el idioma de las cadenas dentro de los recursos, deberá especificar un **iddeidioma** para cada uno.</span><span class="sxs-lookup"><span data-stu-id="1927d-158">If there are multiple resources of the same type and name that differ only in the language of the strings within the resources, you will need to specify a **LanguageId** for each one.</span></span>

</dd> <dt>

<span data-ttu-id="1927d-159">**Versión**</span><span class="sxs-lookup"><span data-stu-id="1927d-159">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="1927d-160">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1927d-160">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1927d-161">Un número de versión definido por el usuario para los datos de recursos que las herramientas pueden utilizar para leer y escribir archivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="1927d-161">A user-defined version number for the resource data that tools can use to read and write resource files.</span></span> <span data-ttu-id="1927d-162">Establezca este valor con la instrucción de definición de recursos de [versión](./version-statement.md) opcional.</span><span class="sxs-lookup"><span data-stu-id="1927d-162">Set this value with the optional [VERSION](./version-statement.md) resource definition statement.</span></span>

</dd> <dt>

<span data-ttu-id="1927d-163">**Características**</span><span class="sxs-lookup"><span data-stu-id="1927d-163">**Characteristics**</span></span>
</dt> <dd>

<span data-ttu-id="1927d-164">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1927d-164">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1927d-165">Especifica la información definida por el usuario sobre el recurso que las herramientas pueden utilizar para leer y escribir archivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="1927d-165">Specifies user-defined information about the resource that tools can use to read and write resource files.</span></span> <span data-ttu-id="1927d-166">Establezca este valor con la instrucción de definición de recursos de [características](./characteristics-statement.md) opcionales.</span><span class="sxs-lookup"><span data-stu-id="1927d-166">Set this value with the optional [CHARACTERISTICS](./characteristics-statement.md) resource definition statement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1927d-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1927d-167">Remarks</span></span>

<span data-ttu-id="1927d-168">Un miembro de tipo variable se denomina **nombre** o miembro **ordinal** , y se usa en la mayoría de los lugares del archivo de recursos donde aparece un identificador.</span><span class="sxs-lookup"><span data-stu-id="1927d-168">A variable type member is called a **Name** or **Ordinal** member, and it is used in most places in the resource file where an identifier appears.</span></span> <span data-ttu-id="1927d-169">La primera **palabra** de un miembro de **nombre** o de tipo **ordinal** indica si el miembro es un valor numérico o una cadena.</span><span class="sxs-lookup"><span data-stu-id="1927d-169">The first **WORD** of a **Name** or **Ordinal** type member indicates whether the member is a numeric value or a string.</span></span> <span data-ttu-id="1927d-170">Si la primera **palabra** del miembro es igual al valor 0xFFFF, que es un carácter Unicode no válido, la **palabra** siguiente es un número de tipo.</span><span class="sxs-lookup"><span data-stu-id="1927d-170">If the first **WORD** in the member is equal to the value 0xffff, which is an invalid Unicode character, then the following **WORD** is a type number.</span></span> <span data-ttu-id="1927d-171">De lo contrario, el miembro contiene una cadena Unicode y la primera **palabra** del miembro es el primer carácter de la cadena de nombre.</span><span class="sxs-lookup"><span data-stu-id="1927d-171">Otherwise, the member contains a Unicode string and the first **WORD** in the member is the first character in the name string.</span></span> <span data-ttu-id="1927d-172">Para obtener más información sobre las instrucciones de definición de recursos, vea [instrucciones de definición de recursos](./resource-definition-statements.md).</span><span class="sxs-lookup"><span data-stu-id="1927d-172">For additional information about resource definition statements, see [Resource-Definition Statements](./resource-definition-statements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1927d-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1927d-173">Requirements</span></span>



| <span data-ttu-id="1927d-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="1927d-174">Requirement</span></span> | <span data-ttu-id="1927d-175">Value</span><span class="sxs-lookup"><span data-stu-id="1927d-175">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1927d-176">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1927d-176">Minimum supported client</span></span><br/> | <span data-ttu-id="1927d-177">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1927d-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1927d-178">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1927d-178">Minimum supported server</span></span><br/> | <span data-ttu-id="1927d-179">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1927d-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1927d-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="1927d-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="1927d-181">**Vista**</span><span class="sxs-lookup"><span data-stu-id="1927d-181">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1927d-182">Recursos</span><span class="sxs-lookup"><span data-stu-id="1927d-182">Resources</span></span>](resources.md)
</dt> <dt>

<span data-ttu-id="1927d-183">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="1927d-183">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="1927d-184">Instrucción CHARACTERISTICS</span><span class="sxs-lookup"><span data-stu-id="1927d-184">CHARACTERISTICS Statement</span></span>](./characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="1927d-185">LANGUAGE (instrucción)</span><span class="sxs-lookup"><span data-stu-id="1927d-185">LANGUAGE Statement</span></span>](./language-statement.md)
</dt> <dt>

[<span data-ttu-id="1927d-186">VERSION (instrucción)</span><span class="sxs-lookup"><span data-stu-id="1927d-186">VERSION Statement</span></span>](./version-statement.md)
</dt> </dl>

 

