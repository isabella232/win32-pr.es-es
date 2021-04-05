---
title: Usar MIDL
description: Crear y compilar una interfaz de Lenguaje de definición de interfaz de Microsoft (MIDL) y una llamada a procedimiento remoto (RPC).
ms.assetid: 2594e3d6-d44a-4e12-8286-b9700e67702e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22da60f20cba6c558c7f1a67478adef7b407d591
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793660"
---
# <a name="using-midl"></a><span data-ttu-id="56a29-103">Usar MIDL</span><span class="sxs-lookup"><span data-stu-id="56a29-103">Using MIDL</span></span>

<span data-ttu-id="56a29-104">Todas las interfaces de los programas que usan RPC deben definirse en Lenguaje de definición de interfaz de Microsoft (MIDL) y compilarse con el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="56a29-104">All interfaces for programs using RPC must be defined in Microsoft Interface Definition Language (MIDL) and compiled with the MIDL compiler.</span></span> <span data-ttu-id="56a29-105">En los siguientes temas se presenta una breve introducción a la creación y compilación de una interfaz MIDL:</span><span class="sxs-lookup"><span data-stu-id="56a29-105">The following topics present a brief overview of creating and compiling a MIDL interface:</span></span>

-   [<span data-ttu-id="56a29-106">Definir una interfaz con MIDL</span><span class="sxs-lookup"><span data-stu-id="56a29-106">Defining an Interface with MIDL</span></span>](#defining-an-interface-with-midl)
-   [<span data-ttu-id="56a29-107">Compilar un archivo MIDL</span><span class="sxs-lookup"><span data-stu-id="56a29-107">Compiling a MIDL File</span></span>](#compiling-a-midl-file)

<span data-ttu-id="56a29-108">Para obtener una explicación detallada de estos temas, vea [los archivos IDL y ACF](the-idl-and-acf-files.md).</span><span class="sxs-lookup"><span data-stu-id="56a29-108">For a detailed discussion of these topics, see [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

## <a name="defining-an-interface-with-midl"></a><span data-ttu-id="56a29-109">Definir una interfaz con MIDL</span><span class="sxs-lookup"><span data-stu-id="56a29-109">Defining an Interface with MIDL</span></span>

<span data-ttu-id="56a29-110">Los archivos MIDL son archivos de texto que se pueden crear y editar con un editor de texto.</span><span class="sxs-lookup"><span data-stu-id="56a29-110">MIDL files are text files that you can create and edit with a text editor.</span></span> <span data-ttu-id="56a29-111">Si genera un UUID para la interfaz, normalmente almacenará la salida en un archivo MIDL de plantilla.</span><span class="sxs-lookup"><span data-stu-id="56a29-111">If you generate a UUID for your interface, you will typically store the output in a template MIDL file.</span></span> <span data-ttu-id="56a29-112">Para obtener más información sobre el UUID, consulte [generación de UUID de interfaz](generating-interface-uuids.md).</span><span class="sxs-lookup"><span data-stu-id="56a29-112">For more information on UUIDs, see [Generating Interface UUIDs](generating-interface-uuids.md).</span></span>

<span data-ttu-id="56a29-113">Todas las interfaces de MIDL tienen el mismo formato.</span><span class="sxs-lookup"><span data-stu-id="56a29-113">All interfaces in MIDL follow the same format.</span></span> <span data-ttu-id="56a29-114">Comienzan con un encabezado que contiene una lista de atributos de interfaz y el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="56a29-114">They begin with a header that contains a list of interface attributes and the interface name.</span></span> <span data-ttu-id="56a29-115">Los atributos se incluyen entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="56a29-115">The attributes are enclosed in square brackets.</span></span> <span data-ttu-id="56a29-116">El encabezado de la interfaz va seguido de su cuerpo, que se incluye entre llaves.</span><span class="sxs-lookup"><span data-stu-id="56a29-116">The interface header is followed by its body, which is enclosed in curly brackets.</span></span> <span data-ttu-id="56a29-117">En el ejemplo siguiente se muestra una interfaz simple:</span><span class="sxs-lookup"><span data-stu-id="56a29-117">A simple interface is shown in the following example:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface MyInterface
{
  const unsigned short INT_ARRAY_LEN = 100;

  void MyRemoteProc( 
      [in] int param1,
      [out] int outArray[INT_ARRAY_LEN]
  );
}
```

<span data-ttu-id="56a29-118">Algunos de los atributos que normalmente aparecen en una definición de interfaz MIDL son el UUID y el número de versión de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="56a29-118">Some of the attributes that typically appear in a MIDL interface definition are the UUID and the interface version number.</span></span> <span data-ttu-id="56a29-119">El cuerpo de la definición de interfaz debe contener las declaraciones de procedimiento de todos los procedimientos remotos en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="56a29-119">The body of the interface definition must contain the procedure declarations of all of the remote procedures in the interface.</span></span> <span data-ttu-id="56a29-120">También puede contener las declaraciones de tipos de datos y constantes que requiere la interfaz.</span><span class="sxs-lookup"><span data-stu-id="56a29-120">It can also contain the declarations of data types and constants required by the interface.</span></span>

<span data-ttu-id="56a29-121">Todos los parámetros de las declaraciones de procedimiento remoto se deben declarar como \[ [**in**](/windows/desktop/Midl/in) \] , \[ [**out**](/windows/desktop/Midl/out-idl) \] o \[ **in**, **out** \] .</span><span class="sxs-lookup"><span data-stu-id="56a29-121">All parameters in the remote procedure declarations must be declared as \[[**in**](/windows/desktop/Midl/in)\], \[[**out**](/windows/desktop/Midl/out-idl)\], or \[**in**, **out**\].</span></span> <span data-ttu-id="56a29-122">Estas declaraciones especifican que el programa cliente pasa los datos a un procedimiento remoto, obtiene los datos de un procedimiento remoto o ambos.</span><span class="sxs-lookup"><span data-stu-id="56a29-122">These declarations specify that the client program passes data into a remote procedure, gets data out of a remote procedure, or both.</span></span> <span data-ttu-id="56a29-123">Para obtener información más detallada sobre las declaraciones de parámetros de interfaz, vea [el cuerpo de la interfaz IDL](the-idl-interface-body.md).</span><span class="sxs-lookup"><span data-stu-id="56a29-123">For more detailed information about interface parameter declarations, see [The IDL Interface Body](the-idl-interface-body.md).</span></span>

## <a name="compiling-a-midl-file"></a><span data-ttu-id="56a29-124">Compilar un archivo MIDL</span><span class="sxs-lookup"><span data-stu-id="56a29-124">Compiling a MIDL File</span></span>

<span data-ttu-id="56a29-125">El compilador MIDL es una herramienta de línea de comandos que se instala automáticamente con el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="56a29-125">The MIDL compiler is a command-line tool that is automatically installed with the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="56a29-126">Para invocarlo en una ventana de comandos, escriba el comando **MIDL**, seguido del nombre de un archivo MIDL, en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="56a29-126">Invoke it in a command window by typing the command **midl**, followed by the name of a MIDL file, at the command line.</span></span> <span data-ttu-id="56a29-127">Asegúrese de que el directorio que contiene el compilador MIDL está en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="56a29-127">Make sure that the directory containing the MIDL compiler is in your path.</span></span> <span data-ttu-id="56a29-128">En el ejemplo siguiente se muestra su uso:</span><span class="sxs-lookup"><span data-stu-id="56a29-128">The following example illustrates its use:</span></span>

<span data-ttu-id="56a29-129">**MyApp. idl de MIDL**</span><span class="sxs-lookup"><span data-stu-id="56a29-129">**midl MyApp.idl**</span></span>

<span data-ttu-id="56a29-130">Tenga en cuenta que no tiene que incluir la extensión si el nombre de archivo tiene la extensión. idl.</span><span class="sxs-lookup"><span data-stu-id="56a29-130">Note that you do not have to include the extension if the file name has the .idl extension.</span></span> <span data-ttu-id="56a29-131">También puede usar los [modificadores de la línea de comandos](/windows/desktop/Midl/midl-command-line-reference) del compilador MIDL si los inserta entre el comando **MIDL** y el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="56a29-131">You can also use the MIDL compiler [command-line switches](/windows/desktop/Midl/midl-command-line-reference) by inserting them between the **midl** command and the file name.</span></span> <span data-ttu-id="56a29-132">Esto se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="56a29-132">This is demonstrated in the following example:</span></span>

<span data-ttu-id="56a29-133">**/ACF de MIDL MyApp. ACF MyApp. idl**</span><span class="sxs-lookup"><span data-stu-id="56a29-133">**midl /acf MyApp.acf MyApp.idl**</span></span>

<span data-ttu-id="56a29-134">En este ejemplo, el compilador MIDL se ejecuta utilizando el archivo MyApp. idl como archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="56a29-134">In this example, the MIDL compiler is executed using the file MyApp.idl as the input file.</span></span> <span data-ttu-id="56a29-135">El modificador de la línea de comandos **/ACF** indica al compilador que utilice también un archivo de configuración de la aplicación (ACF) para la entrada.</span><span class="sxs-lookup"><span data-stu-id="56a29-135">The command line switch **/acf** instructs the compiler to use an application configuration file (ACF) for input as well.</span></span> <span data-ttu-id="56a29-136">Los archivos de configuración de la aplicación se describen con más detalle en [los archivos IDL y ACF](the-idl-and-acf-files.md).</span><span class="sxs-lookup"><span data-stu-id="56a29-136">Application configuration files are discussed more thoroughly in [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

<span data-ttu-id="56a29-137">Para obtener información más detallada sobre cómo utilizar el compilador MIDL, vea el [lenguaje de definición de interfaz de Microsoft (MIDL)](/windows/desktop/Midl/midl-start-page), que contiene información sobre los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="56a29-137">For more detailed information on using the MIDL compiler, see the [Microsoft Interface Definition Language (MIDL)](/windows/desktop/Midl/midl-start-page), which contains information on the following topics:</span></span>

-   [<span data-ttu-id="56a29-138">Requisitos del preprocesador de C para MIDL</span><span class="sxs-lookup"><span data-stu-id="56a29-138">C-Preprocessor Requirements for MIDL</span></span>](/windows/desktop/Midl/c-preprocessor-requirements-for-midl)
-   [<span data-ttu-id="56a29-139">Consideraciones del compilador de C/C++</span><span class="sxs-lookup"><span data-stu-id="56a29-139">C/C++-Compiler Considerations</span></span>](/windows/desktop/Midl/c-c-compiler-considerations)
-   [<span data-ttu-id="56a29-140">Archivos generados para una interfaz RPC</span><span class="sxs-lookup"><span data-stu-id="56a29-140">Files Generated for an RPC Interface</span></span>](/windows/desktop/Midl/files-generated-for-an-rpc-interface)
-   [<span data-ttu-id="56a29-141">Referencia de la línea de comandos de MIDL</span><span class="sxs-lookup"><span data-stu-id="56a29-141">MIDL Command-line Reference</span></span>](/windows/desktop/Midl/midl-command-line-reference)
-   [<span data-ttu-id="56a29-142">Referencia del lenguaje MIDL</span><span class="sxs-lookup"><span data-stu-id="56a29-142">MIDL Language Reference</span></span>](/windows/desktop/Midl/midl-language-reference)
-   [<span data-ttu-id="56a29-143">Errores y advertencias del compilador de MIDL</span><span class="sxs-lookup"><span data-stu-id="56a29-143">MIDL Compiler Errors and Warnings</span></span>](/windows/desktop/Midl/midl-compiler-errors-and-warnings)

 

 