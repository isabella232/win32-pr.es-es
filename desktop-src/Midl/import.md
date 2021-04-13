---
title: import (atributo)
description: La Directiva Import especifica otro archivo IDL, ODL o de encabezado que contiene las definiciones a las que desea hacer referencia desde el archivo IDL principal.
ms.assetid: b52fb2c7-ce60-474f-8833-7a821844f747
keywords:
- importar el atributo MIDL
topic_type:
- apiref
api_name:
- import
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff13c069c6bba819720a9d1120a42c25af4b51
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358851"
---
# <a name="import-attribute"></a><span data-ttu-id="d2a1e-104">import (atributo)</span><span class="sxs-lookup"><span data-stu-id="d2a1e-104">import attribute</span></span>

<span data-ttu-id="d2a1e-105">La directiva **Import** especifica otro archivo IDL, ODL o de encabezado que contiene las definiciones a las que desea hacer referencia desde el archivo IDL principal.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-105">The **import** directive specifies another IDL, ODL, or header file containing definitions you wish to reference from your main IDL file.</span></span>

``` syntax
import "filename" [[ , ... ]] ;
```

## <a name="parameters"></a><span data-ttu-id="d2a1e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2a1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a1e-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="d2a1e-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="d2a1e-108">Especifica el nombre del archivo de encabezado, IDL o ODL que se va a importar.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-108">Specifies the name of the header, IDL, or ODL file to import.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2a1e-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2a1e-109">Remarks</span></span>

<span data-ttu-id="d2a1e-110">Con la Directiva de **importación** , todas las instrucciones idl del archivo importado, como definiciones de tipo, declaraciones de constantes y definiciones de interfaz, pasan a estar disponibles para la importación. Archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-110">With the **import** directive, all IDL statements in the imported file, such as typedefs, constant declarations, and interface definitions become available to the importing .IDL file.</span></span>

<span data-ttu-id="d2a1e-111">El archivo importado se procesa por separado (lo que significa que el preprocesador CPP se invoca de forma independiente) desde el archivo IDL de importación.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-111">The imported file is processed separately (meaning that CPP preprocessor is invoked independently) from the importing IDL file.</span></span> <span data-ttu-id="d2a1e-112">De esta manera, las directivas de preprocesador, como \# definir, no se exportan desde un archivo IDL o de encabezado importado al archivo IDL de importación.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-112">In this way, pre-processor directives, such as \#define, do not carry over from an imported header or IDL file to the importing IDL file.</span></span>

<span data-ttu-id="d2a1e-113">Como la macro de preprocesador de lenguaje C **\# incluye**, la directiva **Import** indica al compilador que incluya los tipos de datos que se definieron en los archivos IDL importados.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-113">Like the C-language preprocessor macro **\#include**, the **import** directive tells the compiler to include data types that were defined in the imported IDL files.</span></span> <span data-ttu-id="d2a1e-114">A diferencia de la directiva **\# include** , la directiva **Import** omite los prototipos de procedimiento, ya que no se genera ningún código auxiliar para nada en el archivo importado.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-114">Unlike the **\#include** directive, the **import** directive ignores procedure prototypes, since no stubs are generated for anything in the imported file.</span></span>

<span data-ttu-id="d2a1e-115">Para obtener información específica sobre cómo usar **importar** para incluir archivos de encabezado en un archivo IDL, vea [importar archivos de encabezado del sistema](importing-system-header-files.md).</span><span class="sxs-lookup"><span data-stu-id="d2a1e-115">For specific information on using **import** to include header files in an IDL file, see [Importing System Header Files](importing-system-header-files.md).</span></span>

<span data-ttu-id="d2a1e-116">Encabezado del lenguaje C (. H) generado para la interfaz no contiene directamente los tipos importados, sino que genera una directiva **\# include** para el archivo de encabezado correspondiente a la interfaz importada.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-116">The C-language header (.H) file generated for the interface does not directly contain the imported types but instead generates a **\#include** directive for the header file corresponding to the imported interface.</span></span> <span data-ttu-id="d2a1e-117">Por ejemplo, al importar BASE. IDL en el derivado. IDL, derivado del archivo de encabezado generado. H contendrá la directiva **\# include** base. H.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-117">For example, when you import BASE.IDL into your DERIVED.IDL, the generated header file DERIVED.H will contain the directive **\#include** BASE.H.</span></span>

<span data-ttu-id="d2a1e-118">Se aplican las reglas siguientes:</span><span class="sxs-lookup"><span data-stu-id="d2a1e-118">The following rules apply:</span></span>

-   <span data-ttu-id="d2a1e-119">La palabra clave **Import** es opcional y puede aparecer cero o más veces en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-119">The **import** keyword is optional and can appear zero or more times in the IDL file.</span></span>
-   <span data-ttu-id="d2a1e-120">Cada palabra clave de **importación** puede asociarse a más de un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-120">Each **import** keyword can be associated with more than one file name.</span></span>
-   <span data-ttu-id="d2a1e-121">Separe varios nombres de archivo con comas.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-121">Separate multiple file names with commas.</span></span>
-   <span data-ttu-id="d2a1e-122">Debe escribir el nombre de archivo entre comillas y finalizar la instrucción de importación con un punto y coma (;).</span><span class="sxs-lookup"><span data-stu-id="d2a1e-122">You must enclose the file name within quotation marks and end the import statement with a semicolon (;).</span></span>
-   <span data-ttu-id="d2a1e-123">Puede importar una interfaz que no tenga atributos en otro archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-123">You can import an interface that has no attributes into another IDL file.</span></span> <span data-ttu-id="d2a1e-124">Sin embargo, la interfaz debe contener solo tipos de contenido; no puede contener ningún procedimiento.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-124">However, the interface must contain only datatypes; it cannot contain any procedures.</span></span> <span data-ttu-id="d2a1e-125">Si hay un procedimiento incluido en la interfaz importada, debe especificar un atributo [**local**](local.md) o [**UUID**](uuid.md) .</span><span class="sxs-lookup"><span data-stu-id="d2a1e-125">If even one procedure is contained in the imported interface, you must specify a [**local**](local.md) or [**UUID**](uuid.md) attribute.</span></span>
-   <span data-ttu-id="d2a1e-126">La función de **importación** es idempotentÂ â € "â es decir, la importación de una interfaz más de una vez no tiene ningún efecto adicional.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-126">The **import** function is idempotentÂ â€”Â that is, importing an interface more than once has no additional effect.</span></span>

> [!Note]  
> <span data-ttu-id="d2a1e-127">El comportamiento de la Directiva de **importación** es independiente del modo de compilador de MIDL modificadores [**/MS \_ ext**](-ms-ext.md) (el valor predeterminado), [**/OSF**](-osf.md)y [**/App \_ config**](-app-config.md).</span><span class="sxs-lookup"><span data-stu-id="d2a1e-127">The behavior of the **import** directive is independent of the MIDL compiler mode switches [**/ms\_ext**](-ms-ext.md) (the default), [**/osf**](-osf.md), and [**/app\_config**](-app-config.md).</span></span> <span data-ttu-id="d2a1e-128">Sin embargo, el modo de compilador (**/OSF** o **/MS \_ ext**) puede afectar a la decoración de atributos de puntero en los tipos importados.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-128">However, the compiler mode (**/osf** or **/ms\_ext**) can affect pointer attribute decoration on imported types.</span></span> <span data-ttu-id="d2a1e-129">Para obtener más información, vea [herencia de tipos de atributos de puntero](/windows/desktop/Rpc/pointer-attribute-type-inheritance).</span><span class="sxs-lookup"><span data-stu-id="d2a1e-129">For details see [Pointer-Attribute Type Inheritance](/windows/desktop/Rpc/pointer-attribute-type-inheritance).</span></span>

 

## <a name="examples"></a><span data-ttu-id="d2a1e-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d2a1e-130">Examples</span></span>

``` syntax
import "myoldodl.odl";  
import "unknwn.idl";
import "part1.idl", "part2.idl", "part3.idl"; 
```

## <a name="see-also"></a><span data-ttu-id="d2a1e-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2a1e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2a1e-132">**configuración de/APP \_**</span><span class="sxs-lookup"><span data-stu-id="d2a1e-132">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="d2a1e-133">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="d2a1e-133">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="d2a1e-134">**importlib**</span><span class="sxs-lookup"><span data-stu-id="d2a1e-134">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="d2a1e-135">**inclui**</span><span class="sxs-lookup"><span data-stu-id="d2a1e-135">**include**</span></span>](include.md)
</dt> <dt>

[<span data-ttu-id="d2a1e-136">Importación de archivos de encabezado del sistema</span><span class="sxs-lookup"><span data-stu-id="d2a1e-136">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> <dt>

[<span data-ttu-id="d2a1e-137">Importar archivos y bibliotecas de tipos</span><span class="sxs-lookup"><span data-stu-id="d2a1e-137">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="d2a1e-138">**\_ext/MS**</span><span class="sxs-lookup"><span data-stu-id="d2a1e-138">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="d2a1e-139">**/osf**</span><span class="sxs-lookup"><span data-stu-id="d2a1e-139">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 