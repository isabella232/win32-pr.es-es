---
title: Convenciones de estilo de codificación
description: Las convenciones de estilo de codificación se usan en esta serie de ejemplo para ayudar a la claridad y coherencia.
ms.assetid: d5e81a52-79f6-4561-891c-05fee125a1b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28e65e19d69f060a5f85d86976c4bd3694f7611
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797373"
---
# <a name="coding-style-conventions"></a><span data-ttu-id="6a765-103">Convenciones de estilo de codificación</span><span class="sxs-lookup"><span data-stu-id="6a765-103">Coding Style Conventions</span></span>

<span data-ttu-id="6a765-104">Las convenciones de estilo de codificación se usan en esta serie de ejemplo para ayudar a la claridad y coherencia.</span><span class="sxs-lookup"><span data-stu-id="6a765-104">Coding style conventions are used in this sample series to aid clarity and consistency.</span></span> <span data-ttu-id="6a765-105">Se usan las convenciones de notación "húngaro".</span><span class="sxs-lookup"><span data-stu-id="6a765-105">The "Hungarian" notation conventions are used.</span></span> <span data-ttu-id="6a765-106">Se han convertido en una práctica de codificación común en la programación de Win32.</span><span class="sxs-lookup"><span data-stu-id="6a765-106">These have become a common coding practice in Win32 programming.</span></span> <span data-ttu-id="6a765-107">Incluyen anotaciones de prefijo variables que proporcionan a los nombres de variable una sugerencia del tipo de la variable.</span><span class="sxs-lookup"><span data-stu-id="6a765-107">They include variable prefix notations that give to variable names a suggestion of the type of the variable.</span></span>

<span data-ttu-id="6a765-108">En la tabla siguiente se enumeran los prefijos comunes.</span><span class="sxs-lookup"><span data-stu-id="6a765-108">The following table lists common prefixes.</span></span>



| <span data-ttu-id="6a765-109">Prefijo</span><span class="sxs-lookup"><span data-stu-id="6a765-109">Prefix</span></span> | <span data-ttu-id="6a765-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a765-110">Description</span></span>                         |
|--------|-------------------------------------|
| <span data-ttu-id="6a765-111">a</span><span class="sxs-lookup"><span data-stu-id="6a765-111">a</span></span>      | <span data-ttu-id="6a765-112">Array</span><span class="sxs-lookup"><span data-stu-id="6a765-112">Array</span></span>                               |
| <span data-ttu-id="6a765-113">b</span><span class="sxs-lookup"><span data-stu-id="6a765-113">b</span></span>      | <span data-ttu-id="6a765-114">BOOL (int)</span><span class="sxs-lookup"><span data-stu-id="6a765-114">BOOL (int)</span></span>                          |
| <span data-ttu-id="6a765-115">c</span><span class="sxs-lookup"><span data-stu-id="6a765-115">c</span></span>      | <span data-ttu-id="6a765-116">Char</span><span class="sxs-lookup"><span data-stu-id="6a765-116">Char</span></span>                                |
| <span data-ttu-id="6a765-117">CB</span><span class="sxs-lookup"><span data-stu-id="6a765-117">cb</span></span>     | <span data-ttu-id="6a765-118">Recuento de bytes</span><span class="sxs-lookup"><span data-stu-id="6a765-118">Count of bytes</span></span>                      |
| <span data-ttu-id="6a765-119">cr</span><span class="sxs-lookup"><span data-stu-id="6a765-119">cr</span></span>     | <span data-ttu-id="6a765-120">Valor de referencia de color</span><span class="sxs-lookup"><span data-stu-id="6a765-120">Color reference value</span></span>               |
| <span data-ttu-id="6a765-121">serie</span><span class="sxs-lookup"><span data-stu-id="6a765-121">cx</span></span>     | <span data-ttu-id="6a765-122">Recuento de x (corto)</span><span class="sxs-lookup"><span data-stu-id="6a765-122">Count of x (short)</span></span>                  |
| <span data-ttu-id="6a765-123">dw</span><span class="sxs-lookup"><span data-stu-id="6a765-123">dw</span></span>     | <span data-ttu-id="6a765-124">DWORD (unsigned Long)</span><span class="sxs-lookup"><span data-stu-id="6a765-124">DWORD (unsigned long)</span></span>               |
| <span data-ttu-id="6a765-125">f</span><span class="sxs-lookup"><span data-stu-id="6a765-125">f</span></span>      | <span data-ttu-id="6a765-126">Marcas (normalmente varios valores de bit)</span><span class="sxs-lookup"><span data-stu-id="6a765-126">Flags (usually multiple bit values)</span></span> |
| <span data-ttu-id="6a765-127">fn</span><span class="sxs-lookup"><span data-stu-id="6a765-127">fn</span></span>     | <span data-ttu-id="6a765-128">Función</span><span class="sxs-lookup"><span data-stu-id="6a765-128">Function</span></span>                            |
| <span data-ttu-id="6a765-129">i\_</span><span class="sxs-lookup"><span data-stu-id="6a765-129">g\_</span></span>    | <span data-ttu-id="6a765-130">Global</span><span class="sxs-lookup"><span data-stu-id="6a765-130">Global</span></span>                              |
| <span data-ttu-id="6a765-131">h</span><span class="sxs-lookup"><span data-stu-id="6a765-131">h</span></span>      | <span data-ttu-id="6a765-132">Handle</span><span class="sxs-lookup"><span data-stu-id="6a765-132">Handle</span></span>                              |
| <span data-ttu-id="6a765-133">i</span><span class="sxs-lookup"><span data-stu-id="6a765-133">i</span></span>      | <span data-ttu-id="6a765-134">Entero</span><span class="sxs-lookup"><span data-stu-id="6a765-134">Integer</span></span>                             |
| <span data-ttu-id="6a765-135">l</span><span class="sxs-lookup"><span data-stu-id="6a765-135">l</span></span>      | <span data-ttu-id="6a765-136">long</span><span class="sxs-lookup"><span data-stu-id="6a765-136">Long</span></span>                                |
| <span data-ttu-id="6a765-137">lp</span><span class="sxs-lookup"><span data-stu-id="6a765-137">lp</span></span>     | <span data-ttu-id="6a765-138">Puntero largo</span><span class="sxs-lookup"><span data-stu-id="6a765-138">Long pointer</span></span>                        |
| <span data-ttu-id="6a765-139">f\_</span><span class="sxs-lookup"><span data-stu-id="6a765-139">m\_</span></span>    | <span data-ttu-id="6a765-140">Miembro de datos de una clase</span><span class="sxs-lookup"><span data-stu-id="6a765-140">Data member of a class</span></span>              |
| <span data-ttu-id="6a765-141">n</span><span class="sxs-lookup"><span data-stu-id="6a765-141">n</span></span>      | <span data-ttu-id="6a765-142">Short int</span><span class="sxs-lookup"><span data-stu-id="6a765-142">Short int</span></span>                           |
| <span data-ttu-id="6a765-143">p</span><span class="sxs-lookup"><span data-stu-id="6a765-143">p</span></span>      | <span data-ttu-id="6a765-144">Puntero</span><span class="sxs-lookup"><span data-stu-id="6a765-144">Pointer</span></span>                             |
| <span data-ttu-id="6a765-145">s</span><span class="sxs-lookup"><span data-stu-id="6a765-145">s</span></span>      | <span data-ttu-id="6a765-146">String</span><span class="sxs-lookup"><span data-stu-id="6a765-146">String</span></span>                              |
| <span data-ttu-id="6a765-147">sz</span><span class="sxs-lookup"><span data-stu-id="6a765-147">sz</span></span>     | <span data-ttu-id="6a765-148">Cadena terminada en cero</span><span class="sxs-lookup"><span data-stu-id="6a765-148">Zero terminated String</span></span>              |
| <span data-ttu-id="6a765-149">tm</span><span class="sxs-lookup"><span data-stu-id="6a765-149">tm</span></span>     | <span data-ttu-id="6a765-150">Métrica de texto</span><span class="sxs-lookup"><span data-stu-id="6a765-150">Text metric</span></span>                         |
| <span data-ttu-id="6a765-151">u</span><span class="sxs-lookup"><span data-stu-id="6a765-151">u</span></span>      | <span data-ttu-id="6a765-152">Unsigned int</span><span class="sxs-lookup"><span data-stu-id="6a765-152">Unsigned int</span></span>                        |
| <span data-ttu-id="6a765-153">UL</span><span class="sxs-lookup"><span data-stu-id="6a765-153">ul</span></span>     | <span data-ttu-id="6a765-154">Unsigned Long (ULONG)</span><span class="sxs-lookup"><span data-stu-id="6a765-154">Unsigned long (ULONG)</span></span>               |
| <span data-ttu-id="6a765-155">w</span><span class="sxs-lookup"><span data-stu-id="6a765-155">w</span></span>      | <span data-ttu-id="6a765-156">WORD (corto sin signo)</span><span class="sxs-lookup"><span data-stu-id="6a765-156">WORD (unsigned short)</span></span>               |
| <span data-ttu-id="6a765-157">x, y</span><span class="sxs-lookup"><span data-stu-id="6a765-157">x,y</span></span>    | <span data-ttu-id="6a765-158">coordenadas x, y (cortas)</span><span class="sxs-lookup"><span data-stu-id="6a765-158">x, y coordinates (short)</span></span>            |



 

<span data-ttu-id="6a765-159">A menudo se combinan, como en el siguiente.</span><span class="sxs-lookup"><span data-stu-id="6a765-159">These are often combined, as in the following.</span></span>



| <span data-ttu-id="6a765-160">Combinación de prefijo</span><span class="sxs-lookup"><span data-stu-id="6a765-160">Prefix combination</span></span> | <span data-ttu-id="6a765-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a765-161">Description</span></span>                                             |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="6a765-162">pszMyString</span><span class="sxs-lookup"><span data-stu-id="6a765-162">pszMyString</span></span>        | <span data-ttu-id="6a765-163">Puntero a una cadena.</span><span class="sxs-lookup"><span data-stu-id="6a765-163">A pointer to a string.</span></span>                                  |
| <span data-ttu-id="6a765-164">m \_ pszMyString</span><span class="sxs-lookup"><span data-stu-id="6a765-164">m\_pszMyString</span></span>     | <span data-ttu-id="6a765-165">Puntero a una cadena que es un miembro de datos de una clase.</span><span class="sxs-lookup"><span data-stu-id="6a765-165">A pointer to a string that is a data member of a class.</span></span> |



 

<span data-ttu-id="6a765-166">En la tabla siguiente se enumeran otras convenciones.</span><span class="sxs-lookup"><span data-stu-id="6a765-166">Other conventions are listed in the following table.</span></span>



| <span data-ttu-id="6a765-167">Convención</span><span class="sxs-lookup"><span data-stu-id="6a765-167">Convention</span></span>       | <span data-ttu-id="6a765-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a765-168">Description</span></span>                                              |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="6a765-169">CMyClass</span><span class="sxs-lookup"><span data-stu-id="6a765-169">CMyClass</span></span>         | <span data-ttu-id="6a765-170">Prefijo ' C ' para los nombres de clase de C++.</span><span class="sxs-lookup"><span data-stu-id="6a765-170">Prefix 'C' for C++ class names.</span></span>                          |
| <span data-ttu-id="6a765-171">COMyObjectClass</span><span class="sxs-lookup"><span data-stu-id="6a765-171">COMyObjectClass</span></span>  | <span data-ttu-id="6a765-172">Prefijo ' CO ' para los nombres de clase de objeto COM.</span><span class="sxs-lookup"><span data-stu-id="6a765-172">Prefix 'CO' for COM object class names.</span></span>                  |
| <span data-ttu-id="6a765-173">CFMyClassFactory</span><span class="sxs-lookup"><span data-stu-id="6a765-173">CFMyClassFactory</span></span> | <span data-ttu-id="6a765-174">Prefijo ' CF ' para los nombres de generador de clases COM.</span><span class="sxs-lookup"><span data-stu-id="6a765-174">Prefix 'CF' for COM class factory names.</span></span>                 |
| <span data-ttu-id="6a765-175">IMyInterface</span><span class="sxs-lookup"><span data-stu-id="6a765-175">IMyInterface</span></span>     | <span data-ttu-id="6a765-176">Prefijo ' I ' para los nombres de clase de interfaz COM.</span><span class="sxs-lookup"><span data-stu-id="6a765-176">Prefix 'I' for COM interface class names.</span></span>                |
| <span data-ttu-id="6a765-177">CImpIMyInterface</span><span class="sxs-lookup"><span data-stu-id="6a765-177">CImpIMyInterface</span></span> | <span data-ttu-id="6a765-178">Prefijo ' CImpI ' para las clases de implementación de interfaz COM.</span><span class="sxs-lookup"><span data-stu-id="6a765-178">Prefix 'CImpI' for COM interface implementation classes.</span></span> |



 

<span data-ttu-id="6a765-179">En esta serie de ejemplos se usan algunas convenciones coherentes para los bloques de encabezado de comentario, como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="6a765-179">Some consistent conventions for comment header blocks are used in this sample series as follows.</span></span>

## <a name="file-header"></a><span data-ttu-id="6a765-180">Encabezado de archivo</span><span class="sxs-lookup"><span data-stu-id="6a765-180">File Header</span></span>

``` syntax
/*+===================================================================
  File:      MYFILE.EXT

  Summary:   Brief summary of the file contents and purpose.

  Classes:   Classes declared or used (in source files).

  Functions: Functions exported (in source files).

  Origin:    Indications of where content may have come from. This
             is not a change history but rather a reference to the
             editor-inheritance behind the content or other
             indications about the origin of the source.

  Copyright and Legal notices.
  Copyright and Legal notices.
===================================================================+*/
```

## <a name="plain-comment-block"></a><span data-ttu-id="6a765-181">Bloque de comentario sin formato</span><span class="sxs-lookup"><span data-stu-id="6a765-181">Plain Comment Block</span></span>

``` syntax
/*--------------------------------------------------------------------
  Plain block of comment text that usually takes several lines.
  Plain block of comment text that usually takes several lines.
--------------------------------------------------------------------*/
```

## <a name="class-declaration-header"></a><span data-ttu-id="6a765-182">Encabezado de declaración de clase</span><span class="sxs-lookup"><span data-stu-id="6a765-182">Class Declaration Header</span></span>

``` syntax
/*C+C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C
  Class:    CMyClass

  Summary:  Short summary of purpose and content of CMyClass.
            Short summary of purpose and content of CMyClass.

  Methods:  MyMethodOne
              Short description of MyMethodOne.
            MyMethodTwo
              Short description of MyMethodTwo.
            CMyClass
              Constructor.
            ~CMyClass
              Destructor.
C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C-C*/
```

## <a name="class-method-definition-header"></a><span data-ttu-id="6a765-183">Encabezado de definición del método de clase</span><span class="sxs-lookup"><span data-stu-id="6a765-183">Class Method Definition Header</span></span>

``` syntax
/*M+M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M
  Method:   CMyClass::MyMethodOne

  Summary:  Short summary of purpose and content of MyMethodOne.
            Short summary of purpose and content of MyMethodOne.

  Args:     MYTYPE MyArgOne
              Short description of argument MyArgOne.
            MYTYPE MyArgTwo
              Short description of argument MyArgTwo.

  Modifies: [list of member data variables modified by this method].

  Returns:  MYRETURNTYPE
              Short description of meaning of the return type values.
M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M-M*/
```

## <a name="unexported-or-local-function"></a><span data-ttu-id="6a765-184">Función no exportada o local</span><span class="sxs-lookup"><span data-stu-id="6a765-184">Unexported or Local Function</span></span>

``` syntax
/*F+F+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
  Function: MyLocalFunction

  Summary:  What MyLocalFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
-----------------------------------------------------------------F-F*/
```

## <a name="exported-function-definition-header"></a><span data-ttu-id="6a765-185">Encabezado de definición de función exportada</span><span class="sxs-lookup"><span data-stu-id="6a765-185">Exported Function Definition Header</span></span>

``` syntax
/*F+F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F
  Function: MyFunction

  Summary:  What MyFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F-F*/
```

## <a name="com-interface-declaration-header"></a><span data-ttu-id="6a765-186">Encabezado de declaración de interfaz COM</span><span class="sxs-lookup"><span data-stu-id="6a765-186">COM Interface Declaration Header</span></span>

``` syntax
/*I+I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I
  Interface: IMyInterface

  Summary:   Short summary of what features the interface can bring to
             a COM Component.

  Methods:   MYTYPE MyMethodOne
               Description.
             MYTYPE MyMethodTwo
               Description.
I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I-I*/
```

## <a name="com-object-class-declaration-header"></a><span data-ttu-id="6a765-187">Encabezado de declaración de clase de objeto COM</span><span class="sxs-lookup"><span data-stu-id="6a765-187">COM Object Class Declaration Header</span></span>

``` syntax
/*O+O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O
  ObjectClass: COMyCOMObject

  Summary:     Short summary of purpose and content of this object.

  Interfaces:  IUnknown
                 Standard interface providing COM object features.
               IMyInterfaceOne
                 Description.
               IMyInterfaceTwo
                 Description.

  Aggregation: [whether this COM Object is aggregatable or not]
O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O-O*/
```

<span data-ttu-id="6a765-188">Todas estas convenciones de bloque de comentario tienen cadenas de token de inicio y finalización coherentes.</span><span class="sxs-lookup"><span data-stu-id="6a765-188">All of these comment block conventions have consistent beginning and ending token strings.</span></span> <span data-ttu-id="6a765-189">Esta coherencia admite el procesamiento automático de los encabezados de alguna manera.</span><span class="sxs-lookup"><span data-stu-id="6a765-189">This consistency supports automatic processing of the headers in some fashion.</span></span> <span data-ttu-id="6a765-190">Por ejemplo, se pueden escribir scripts de AWK para filtrar los encabezados de función en un archivo de texto independiente que puede servir como base para un documento de especificación.</span><span class="sxs-lookup"><span data-stu-id="6a765-190">For example, AWK scripts can be written to filter the function headers into a separate text file that can then serve as the basis for a specification document.</span></span> <span data-ttu-id="6a765-191">Del mismo modo, las herramientas como la utilidad autoduck no admitida (actualmente disponible en el CD-ROM de la biblioteca de desarrollo de Microsoft Developer Network) se pueden usar para procesar los bloques de comentarios de estos encabezados.</span><span class="sxs-lookup"><span data-stu-id="6a765-191">Similarly, tools like the unsupported AUTODUCK utility (currently available on the Microsoft Developer Network Development Library CD-ROM) can be used to process the comment blocks in these headers.</span></span>

<span data-ttu-id="6a765-192">En la tabla siguiente se enumeran las cadenas de token de inicio y finalización usadas en los tutoriales de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="6a765-192">The following table lists beginning and ending token strings used in sample tutorials.</span></span>



| <span data-ttu-id="6a765-193">Token</span><span class="sxs-lookup"><span data-stu-id="6a765-193">Token</span></span> | <span data-ttu-id="6a765-194">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a765-194">Description</span></span>                      |
|-------|----------------------------------|
| /\*+  | <span data-ttu-id="6a765-195">Inicio del encabezado de archivo</span><span class="sxs-lookup"><span data-stu-id="6a765-195">File Header Begin</span></span>                |
| +\*/  | <span data-ttu-id="6a765-196">Fin del encabezado de archivo</span><span class="sxs-lookup"><span data-stu-id="6a765-196">File Header End</span></span>                  |
| /\*-  | <span data-ttu-id="6a765-197">Inicio de encabezado de bloque de comentario sin formato</span><span class="sxs-lookup"><span data-stu-id="6a765-197">Plain comment block Header Begin</span></span> |
| -\*/  | <span data-ttu-id="6a765-198">Final de encabezado de bloque de comentario sin formato</span><span class="sxs-lookup"><span data-stu-id="6a765-198">Plain comment block Header End</span></span>   |
| <span data-ttu-id="6a765-199">/\*Unidad</span><span class="sxs-lookup"><span data-stu-id="6a765-199">/\*C</span></span>  | <span data-ttu-id="6a765-200">Inicio del encabezado de clase</span><span class="sxs-lookup"><span data-stu-id="6a765-200">Class Header Begin</span></span>               |
| <span data-ttu-id="6a765-201">Unidad\*/</span><span class="sxs-lookup"><span data-stu-id="6a765-201">C\*/</span></span>  | <span data-ttu-id="6a765-202">Fin de encabezado de clase</span><span class="sxs-lookup"><span data-stu-id="6a765-202">Class Header End</span></span>                 |
| <span data-ttu-id="6a765-203">/\*F</span><span class="sxs-lookup"><span data-stu-id="6a765-203">/\*M</span></span>  | <span data-ttu-id="6a765-204">Inicio de encabezado de método</span><span class="sxs-lookup"><span data-stu-id="6a765-204">Method Header Begin</span></span>              |
| <span data-ttu-id="6a765-205">F\*/</span><span class="sxs-lookup"><span data-stu-id="6a765-205">M\*/</span></span>  | <span data-ttu-id="6a765-206">Fin del encabezado de método</span><span class="sxs-lookup"><span data-stu-id="6a765-206">Method Header End</span></span>                |
| <span data-ttu-id="6a765-207">/\*Formato</span><span class="sxs-lookup"><span data-stu-id="6a765-207">/\*F</span></span>  | <span data-ttu-id="6a765-208">Inicio del encabezado de función</span><span class="sxs-lookup"><span data-stu-id="6a765-208">Function Header Begin</span></span>            |
| <span data-ttu-id="6a765-209">Formato\*/</span><span class="sxs-lookup"><span data-stu-id="6a765-209">F\*/</span></span>  | <span data-ttu-id="6a765-210">Fin del encabezado de función</span><span class="sxs-lookup"><span data-stu-id="6a765-210">Function Header End</span></span>              |
| <span data-ttu-id="6a765-211">/\*Configur</span><span class="sxs-lookup"><span data-stu-id="6a765-211">/\*I</span></span>  | <span data-ttu-id="6a765-212">Inicio de encabezado de interfaz</span><span class="sxs-lookup"><span data-stu-id="6a765-212">Interface Header Begin</span></span>           |
| <span data-ttu-id="6a765-213">Configur\*/</span><span class="sxs-lookup"><span data-stu-id="6a765-213">I\*/</span></span>  | <span data-ttu-id="6a765-214">Fin de encabezado de interfaz</span><span class="sxs-lookup"><span data-stu-id="6a765-214">Interface Header End</span></span>             |
| <span data-ttu-id="6a765-215">/\*Aceptar</span><span class="sxs-lookup"><span data-stu-id="6a765-215">/\*O</span></span>  | <span data-ttu-id="6a765-216">Inicio del encabezado de clase de objeto COM</span><span class="sxs-lookup"><span data-stu-id="6a765-216">COM Object Class Header Begin</span></span>    |
| <span data-ttu-id="6a765-217">Aceptar\*/</span><span class="sxs-lookup"><span data-stu-id="6a765-217">O\*/</span></span>  | <span data-ttu-id="6a765-218">Fin de encabezado de clase de objeto COM</span><span class="sxs-lookup"><span data-stu-id="6a765-218">COM Object Class Header End</span></span>      |



 

<span data-ttu-id="6a765-219">Estos encabezados también se pueden usar como indicaciones visuales para el examen rápido de archivos de código fuente.</span><span class="sxs-lookup"><span data-stu-id="6a765-219">These headers can also be used as visual cues for rapid scanning of source files.</span></span> <span data-ttu-id="6a765-220">También proporcionan comodidad para obtener rápidamente una ubicación de origen si configura cadenas de búsqueda en el editor y, a continuación, "repetir la última búsqueda" para encontrar rápidamente estos encabezados.</span><span class="sxs-lookup"><span data-stu-id="6a765-220">They also provide convenience for rapidly getting to some source location if you set up search strings in your editor and then 'repeat last search' to quickly locate these headers.</span></span>

<span data-ttu-id="6a765-221">Por ejemplo, la cadena de búsqueda "M + M" buscará el inicio de los encabezados de método y "M-M" buscará el principio del código de implementación o la definición de método real.</span><span class="sxs-lookup"><span data-stu-id="6a765-221">For example, the search string "M+M" will locate the start of method headers, and "M-M" will locate the beginning of the actual method definition/implementation code.</span></span>

 

 




