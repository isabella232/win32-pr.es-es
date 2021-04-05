---
title: El cuerpo ACF
description: El cuerpo ACF contiene atributos de configuración que se aplican a los tipos y funciones definidos en el cuerpo de la interfaz del archivo IDL.
ms.assetid: 7d6344d3-1117-40b9-be95-a400b81339d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19422762c61dee63c4f502448197aefb432c80c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104078517"
---
# <a name="the-acf-body"></a><span data-ttu-id="2b1f2-103">El cuerpo ACF</span><span class="sxs-lookup"><span data-stu-id="2b1f2-103">The ACF Body</span></span>

<span data-ttu-id="2b1f2-104">El cuerpo ACF contiene atributos de configuración que se aplican a los tipos y funciones definidos en el cuerpo de la interfaz del archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="2b1f2-104">The ACF body contains configuration attributes that apply to types and functions defined in the interface body of the IDL file.</span></span> <span data-ttu-id="2b1f2-105">El cuerpo de ACF puede estar vacío o puede contener atributos de [**inclusión**](/windows/desktop/Midl/include)ACF, [**typedef**](/windows/desktop/Midl/typedef), función y parámetro.</span><span class="sxs-lookup"><span data-stu-id="2b1f2-105">The body of the ACF can be empty or it can contain ACF [**include**](/windows/desktop/Midl/include), [**typedef**](/windows/desktop/Midl/typedef), function, and parameter attributes.</span></span> <span data-ttu-id="2b1f2-106">Todos estos elementos son opcionales.</span><span class="sxs-lookup"><span data-stu-id="2b1f2-106">All of these items are optional.</span></span> <span data-ttu-id="2b1f2-107">Los atributos que se aplican a tipos y funciones individuales en el cuerpo ACF reemplazan a los atributos del encabezado ACF.</span><span class="sxs-lookup"><span data-stu-id="2b1f2-107">Attributes applied to individual types and functions in the ACF body override attributes in the ACF header.</span></span>

<span data-ttu-id="2b1f2-108">ACF especifica el comportamiento en el equipo local y no afecta a los datos transmitidos a través de la red.</span><span class="sxs-lookup"><span data-stu-id="2b1f2-108">The ACF specifies behavior on the local computer and does not affect the data transmitted over the network.</span></span> <span data-ttu-id="2b1f2-109">Se utiliza para especificar los detalles de un código auxiliar que se va a generar.</span><span class="sxs-lookup"><span data-stu-id="2b1f2-109">It is used to specify details of a stub to be generated.</span></span> <span data-ttu-id="2b1f2-110">En el modo de compatibilidad de DCE ([**/OSF**](/windows/desktop/Midl/-osf)), el ACF no afecta a la interacción entre códigos auxiliares, sino entre el código auxiliar y el código de aplicación.</span><span class="sxs-lookup"><span data-stu-id="2b1f2-110">In DCE-compatibility mode ([**/osf**](/windows/desktop/Midl/-osf)), the ACF does not affect interaction between stubs, but between the stub and application code.</span></span>

<span data-ttu-id="2b1f2-111">Un parámetro especificado en ACF debe ser uno de los parámetros especificados en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="2b1f2-111">A parameter specified in the ACF must be one of the parameters specified in the IDL file.</span></span> <span data-ttu-id="2b1f2-112">El orden de especificación del parámetro en ACF no es significativo porque la coincidencia es por nombre, no por posición.</span><span class="sxs-lookup"><span data-stu-id="2b1f2-112">The order of specification of the parameter in the ACF is not significant because the matching is by name, not by position.</span></span> <span data-ttu-id="2b1f2-113">La lista de parámetros de ACF puede estar vacía, incluso si la lista de parámetros de la signatura IDL correspondiente no es (pero no se recomienda).</span><span class="sxs-lookup"><span data-stu-id="2b1f2-113">The parameter list in the ACF can be empty, even when the parameter list in the corresponding IDL signature is not (but this is not recommended).</span></span> <span data-ttu-id="2b1f2-114">Los declaradores abstractos (parámetros sin nombre) en el archivo IDL hacen que el compilador de MIDL informe de los errores al procesar el ACF porque no se encuentra el parámetro.</span><span class="sxs-lookup"><span data-stu-id="2b1f2-114">Abstract declarators (unnamed parameters) in the IDL file cause the MIDL compiler to report errors while processing the ACF because the parameter is not found.</span></span>

<span data-ttu-id="2b1f2-115">La Directiva de **inclusión** ACF especifica los archivos de encabezado que aparecen en el encabezado generado como parte de una instrucción **\# include** estándar de C-preprocesador.</span><span class="sxs-lookup"><span data-stu-id="2b1f2-115">The ACF **include** directive specifies the header files to appear in the generated header as part of a standard C-preprocessor **\#include** statement.</span></span> <span data-ttu-id="2b1f2-116">La palabra clave ACF **incluye** diferencias entre una directiva **\# include** .</span><span class="sxs-lookup"><span data-stu-id="2b1f2-116">The ACF keyword **include** differs from an **\#include** directive.</span></span> <span data-ttu-id="2b1f2-117">La palabra clave ACF **incluye** que la línea "**\# include** *filename*" aparezca en el archivo de encabezado generado, mientras que la Directiva del lenguaje C "**\# include** *filename*" hace que el contenido de ese archivo se coloque en el ACF.</span><span class="sxs-lookup"><span data-stu-id="2b1f2-117">The ACF keyword **include** causes the line "**\#include** *filename*" to appear in the generated header file, while the C-language directive "**\#include** *filename*" causes the contents of that file to be placed in the ACF.</span></span>

<span data-ttu-id="2b1f2-118">La instrucción [**typedef**](/windows/desktop/Midl/typedef) de ACF permite aplicar atributos de tipo ACF a los tipos definidos anteriormente en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="2b1f2-118">The ACF [**typedef**](/windows/desktop/Midl/typedef) statement lets you apply ACF type attributes to types previously defined in the IDL file.</span></span> <span data-ttu-id="2b1f2-119">La sintaxis de **typedef** de ACF difiere de la sintaxis de **typedef** de C.</span><span class="sxs-lookup"><span data-stu-id="2b1f2-119">The ACF **typedef** syntax differs from the C **typedef** syntax.</span></span>

<span data-ttu-id="2b1f2-120">Los atributos de función ACF permiten especificar los atributos que se aplican a la función en conjunto.</span><span class="sxs-lookup"><span data-stu-id="2b1f2-120">The ACF function attributes let you specify attributes that apply to the function as a whole.</span></span> <span data-ttu-id="2b1f2-121">Para obtener más información, vea **\[** [**código**](/windows/desktop/Midl/code) **\]** , **\[** [**optimizar**](/windows/desktop/Midl/optimize) **\]** y **\[** [**nocode**](/windows/desktop/Midl/nocode) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2b1f2-121">For more information, see **\[**[**code**](/windows/desktop/Midl/code)**\]**, **\[**[**optimize**](/windows/desktop/Midl/optimize)**\]**, and **\[**[**nocode**](/windows/desktop/Midl/nocode)**\]**.</span></span>

<span data-ttu-id="2b1f2-122">Los atributos del parámetro ACF permiten especificar los atributos que se aplican a los parámetros individuales de la función.</span><span class="sxs-lookup"><span data-stu-id="2b1f2-122">The ACF parameter attributes let you specify attributes that apply to individual parameters of the function.</span></span> <span data-ttu-id="2b1f2-123">Para obtener más información, vea **\[** [**\_ recuento de bytes**](/windows/desktop/Midl/byte-count) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2b1f2-123">For more information, see **\[**[**byte\_count**](/windows/desktop/Midl/byte-count)**\]**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b1f2-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2b1f2-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b1f2-125">**configuración de/APP \_**</span><span class="sxs-lookup"><span data-stu-id="2b1f2-125">**/app\_config**</span></span>](/windows/desktop/Midl/-app-config)
</dt> <dt>

[<span data-ttu-id="2b1f2-126">**/osf**</span><span class="sxs-lookup"><span data-stu-id="2b1f2-126">**/osf**</span></span>](/windows/desktop/Midl/-osf)
</dt> <dt>

<span data-ttu-id="2b1f2-127">[**\[\_identificador automático\]**](../midl/auto-handle.md)</span><span class="sxs-lookup"><span data-stu-id="2b1f2-127">[**\[auto\_handle\]**](../midl/auto-handle.md)</span></span>
</dt> <dt>

<span data-ttu-id="2b1f2-128">[**\[codifica\]**](../midl/code.md)</span><span class="sxs-lookup"><span data-stu-id="2b1f2-128">[**\[code\]**](../midl/code.md)</span></span>
</dt> <dt>

<span data-ttu-id="2b1f2-129">[**\[\_identificador explícito\]**](../midl/explicit-handle.md)</span><span class="sxs-lookup"><span data-stu-id="2b1f2-129">[**\[explicit\_handle\]**](../midl/explicit-handle.md)</span></span>
</dt> <dt>

[<span data-ttu-id="2b1f2-130">El archivo de lenguaje de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="2b1f2-130">The Interface Definition Language (IDL) File</span></span>](the-interface-definition-language-idl-file.md)
</dt> <dt>

<span data-ttu-id="2b1f2-131">[**\[\_identificador implícito\]**](../midl/implicit-handle.md)</span><span class="sxs-lookup"><span data-stu-id="2b1f2-131">[**\[implicit\_handle\]**](../midl/implicit-handle.md)</span></span>
</dt> <dt>

[<span data-ttu-id="2b1f2-132">**inclui**</span><span class="sxs-lookup"><span data-stu-id="2b1f2-132">**include**</span></span>](/windows/desktop/Midl/include)
</dt> <dt>

[<span data-ttu-id="2b1f2-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="2b1f2-133">midl</span></span>](/windows/desktop/Midl/midl-language-reference)
</dt> <dt>

<span data-ttu-id="2b1f2-134">[**\[nocode\]**](../midl/nocode.md)</span><span class="sxs-lookup"><span data-stu-id="2b1f2-134">[**\[nocode\]**](../midl/nocode.md)</span></span>
</dt> <dt>

<span data-ttu-id="2b1f2-135">[**\[optimiz\]**](../midl/optimize.md)</span><span class="sxs-lookup"><span data-stu-id="2b1f2-135">[**\[optimize\]**](../midl/optimize.md)</span></span>
</dt> <dt>

<span data-ttu-id="2b1f2-136">[**\[representar \_ como\]**](../midl/represent-as.md)</span><span class="sxs-lookup"><span data-stu-id="2b1f2-136">[**\[represent\_as\]**](../midl/represent-as.md)</span></span>
</dt> <dt>

[<span data-ttu-id="2b1f2-137">**typedef**</span><span class="sxs-lookup"><span data-stu-id="2b1f2-137">**typedef**</span></span>](/windows/desktop/Midl/typedef)
</dt> </dl>

 

 