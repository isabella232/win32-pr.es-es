---
title: Usar objetos COM en Windows Script Host
description: Microsoft Windows Script Host es una utilidad de scripting que puede usar para ejecutar scripts en el sistema operativo base.
ms.assetid: b13c1bdf-91ce-42a2-b66a-20d68952bb34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cb28fc0e388ba69f28c56e780d058d27f9e165
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820471"
---
# <a name="using-com-objects-in-windows-script-host"></a><span data-ttu-id="87968-103">Usar objetos COM en Windows Script Host</span><span class="sxs-lookup"><span data-stu-id="87968-103">Using COM Objects in Windows Script Host</span></span>

<span data-ttu-id="87968-104">Microsoft Windows Script Host es una utilidad de scripting que puede usar para ejecutar scripts en el sistema operativo base.</span><span class="sxs-lookup"><span data-stu-id="87968-104">Microsoft Windows Script Host is a scripting utility you can use to run scripts within the base operating system.</span></span> <span data-ttu-id="87968-105">Puede usar Windows Script Host para automatizar las tareas comunes y crear macros eficaces y scripts de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="87968-105">You can use Windows Script Host to automate common tasks and to create powerful macros and logon scripts.</span></span> <span data-ttu-id="87968-106">Windows Script Host incluye los motores de scripting de VBScript y JScript ActiveX.</span><span class="sxs-lookup"><span data-stu-id="87968-106">Windows Script Host comes with VBScript and JScript ActiveX scripting engines.</span></span> <span data-ttu-id="87968-107">Otras compañías de software proporcionan motores de scripting ActiveX para lenguajes como PerlScript, PScript, Python y otros.</span><span class="sxs-lookup"><span data-stu-id="87968-107">Other software companies provide ActiveX scripting engines for languages such as PerlScript, PScript, Python, and others.</span></span>

<span data-ttu-id="87968-108">Para usar un objeto COM en un script ejecutado por Windows Script Host, primero debe crear una instancia del objeto.</span><span class="sxs-lookup"><span data-stu-id="87968-108">To use a COM object in a script run by Windows Script Host, you must first create an instance of the object.</span></span> <span data-ttu-id="87968-109">Después de crear un objeto COM, puede usarlo en scripts.</span><span class="sxs-lookup"><span data-stu-id="87968-109">After a COM object has been created, you can then use it in scripts.</span></span>

<span data-ttu-id="87968-110">Windows Script Host se compone de dos aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="87968-110">Windows Script Host consists of two applications.</span></span> <span data-ttu-id="87968-111">Una ejecuta scripts desde el escritorio de Windows ( `WScript.exe` ); el otro ejecuta scripts desde el símbolo del sistema ( `CScript.exe` ).</span><span class="sxs-lookup"><span data-stu-id="87968-111">One runs scripts from the Windows desktop (`WScript.exe`); the other runs scripts from the command prompt (`CScript.exe`).</span></span>

<span data-ttu-id="87968-112">Para ejecutar un script desde el escritorio, simplemente haga doble clic en un archivo de script.</span><span class="sxs-lookup"><span data-stu-id="87968-112">To run a script from the desktop, simply double-click a script file.</span></span> <span data-ttu-id="87968-113">Los archivos de script son archivos de texto.</span><span class="sxs-lookup"><span data-stu-id="87968-113">Script files are text files.</span></span> <span data-ttu-id="87968-114">Por Convención, los archivos de VBScript tienen la extensión `.vbs` y los archivos JScript `.js` .</span><span class="sxs-lookup"><span data-stu-id="87968-114">By convention, VBScript files have the extension `.vbs` and JScript files `.js`.</span></span>

<span data-ttu-id="87968-115">Para ejecutar un script desde el símbolo del sistema, ejecute la `Cscript.exe` aplicación con una línea de comandos como la siguiente:</span><span class="sxs-lookup"><span data-stu-id="87968-115">To run a script from the command prompt, run the `Cscript.exe` application with a command line such as the following:</span></span>

```console
cscript "c:\\sample scripts\\chart.vbs"
```

<span data-ttu-id="87968-116">donde `c:\\sample scripts\\chart.vbs` es la ruta de acceso al archivo que contiene el script.</span><span class="sxs-lookup"><span data-stu-id="87968-116">where `c:\\sample scripts\\chart.vbs` is the path to the file containing the script.</span></span>

<span data-ttu-id="87968-117">Puede imprimir una lista de los parámetros admitidos por Cscript.exe escribiendo la siguiente línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="87968-117">You can print out a list of the parameters supported by Cscript.exe by entering the following command line:</span></span>

```console
call cscript //?
```

<span data-ttu-id="87968-118">Para usar un objeto COM en un script ejecutado por Windows Script Host, primero debe crear una instancia del objeto.</span><span class="sxs-lookup"><span data-stu-id="87968-118">To use a COM object in a script run by Windows Script Host, you must first create an instance of the object.</span></span> <span data-ttu-id="87968-119">En VBScript puede hacerlo llamando al `CreateObject()` método.</span><span class="sxs-lookup"><span data-stu-id="87968-119">In VBScript you can do this by calling the `CreateObject()` method.</span></span> <span data-ttu-id="87968-120">En JScript, puede utilizar el `ActiveXObject` objeto o el `WScript.CreateObject()` método.</span><span class="sxs-lookup"><span data-stu-id="87968-120">In JScript one can use either the `ActiveXObject` object or the `WScript.CreateObject()` method.</span></span> <span data-ttu-id="87968-121">En el ejemplo siguiente se muestra cómo llamar a `CreateObject()` mediante VBScript:</span><span class="sxs-lookup"><span data-stu-id="87968-121">The following example illustrates calling `CreateObject()` using VBScript:</span></span>


```VB
Dim objXL
Set objXL = CreateObject("Excel.Application")
 
```



<span data-ttu-id="87968-122">En el ejemplo siguiente se muestra cómo crear un `ActiveXObject` objeto mediante JScript:</span><span class="sxs-lookup"><span data-stu-id="87968-122">The following example illustrates creating an `ActiveXObject` object using JScript:</span></span>


```JScript
var objXL = new ActiveXObject("Excel.Application");
 
```
<span data-ttu-id="87968-123">También puede usar el `WScript.CreateObject()` método en JScript:</span><span class="sxs-lookup"><span data-stu-id="87968-123">Alternatively using `WScript.CreateObject()` method inside JScript:</span></span>

```JScript
var objXL = WScript.CreateObject("Excel.Application");
```


<span data-ttu-id="87968-124">Después de crear una instancia del objeto COM, puede escribir un script que utilice el objeto, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="87968-124">After you have created an instance of the COM object, you can write script that uses the object, for example:</span></span>


```VB
objXL.Visible = true;
 
```



<span data-ttu-id="87968-125">Además del método CreateObject y el objeto ActiveXObject, tanto VBScript como JScript proporcionan el método GetObject, que devuelve una instancia de objeto.</span><span class="sxs-lookup"><span data-stu-id="87968-125">In addition to the CreateObject method and ActiveXObject object, both VBScript and JScript provide the method GetObject, which returns an object instance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87968-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="87968-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87968-127">Scripting con objetos COM</span><span class="sxs-lookup"><span data-stu-id="87968-127">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




