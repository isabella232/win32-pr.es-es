---
title: Definiciones de compilador de C para proxy/códigos auxiliares
description: El archivo de encabezado rpcproxy. h incluye las siguientes definiciones de macro, cada una de las cuales puede ser útil al compilar una aplicación COM distribuida. Estas macros se invocan con el modificador de preprocesador/D (o-D) en el tiempo de compilación de C.
ms.assetid: 697f0b63-76ae-410d-8bbf-bb95295ffba9
keywords:
- MIDL del compilador de MIDL, compilador de C, definiciones de proxy/código auxiliar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1504c600c3f86a934ab3daa132b041c7310af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076118"
---
# <a name="c-compiler-definitions-for-proxystubs"></a><span data-ttu-id="5bc79-105">Definiciones de compilador de C para proxy/códigos auxiliares</span><span class="sxs-lookup"><span data-stu-id="5bc79-105">C-Compiler Definitions for Proxy/Stubs</span></span>

<span data-ttu-id="5bc79-106">El archivo de encabezado rpcproxy. h incluye las siguientes definiciones de macro, cada una de las cuales puede ser útil al compilar una aplicación COM distribuida.</span><span class="sxs-lookup"><span data-stu-id="5bc79-106">The header file Rpcproxy.h includes the following macro definitions, each of which may be convenient when building distributed COM application.</span></span> <span data-ttu-id="5bc79-107">Estas macros se invocan con el modificador de preprocesador [**/d**](-d.md) (o-D) en el tiempo de compilación de C.</span><span class="sxs-lookup"><span data-stu-id="5bc79-107">These macros are invoked with the [**/D**](-d.md) (or -D) preprocessor switch at the C-compile time.</span></span>



| <span data-ttu-id="5bc79-108">MACRO</span><span class="sxs-lookup"><span data-stu-id="5bc79-108">MACRO</span></span>                                                                                                                                                                                           | <span data-ttu-id="5bc79-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5bc79-109">Description</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bc79-110">REGISTRAR \_ dll de proxy \_</span><span class="sxs-lookup"><span data-stu-id="5bc79-110">REGISTER\_PROXY\_DLL</span></span>                                                                                                                                                                            | <span data-ttu-id="5bc79-111">Genera funciones **DllMain**, **DllRegisterServer** y **DllUnregisterServer** para registrar automáticamente un archivo dll de proxy.</span><span class="sxs-lookup"><span data-stu-id="5bc79-111">Generates **DllMain**, **DllRegisterServer**, and **DllUnregisterServer** functions for automatically registering a proxy DLL.</span></span>                                                                                       |
| <span data-ttu-id="5bc79-112">CLSID de PROXY \_ =<clsid></span><span class="sxs-lookup"><span data-stu-id="5bc79-112">PROXY\_CLSID=<clsid></span></span>                                                                                                                                                                      | <span data-ttu-id="5bc79-113">Especifica un identificador de clase para el servidor.</span><span class="sxs-lookup"><span data-stu-id="5bc79-113">Specifies a class identifier for the server.</span></span> <span data-ttu-id="5bc79-114">Si no se define esta macro, el CLSID predeterminado es el primer identificador de interfaz que encuentra el compilador MIDL en la especificación IDL para el servidor proxy/código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="5bc79-114">If this macro is not defined, the default CLSID is the first interface identifier that the MIDL compiler encounters in the IDL specification for the Proxy/Stub server.</span></span> |
| <span data-ttu-id="5bc79-115">El \_ CLSID del proxy \_ es = {0x *8hexdigits*, 0x *4hexdigits*, 0x *4hexdigits*, {0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*,}}</span><span class="sxs-lookup"><span data-stu-id="5bc79-115">PROXY\_CLSID\_IS={0x *8hexdigits*, 0x *4hexdigits*,0x *4hexdigits*, {0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*,}}</span></span> | <span data-ttu-id="5bc79-116">Especifica el valor del identificador de clase del servidor en formato hexadecimal binario.</span><span class="sxs-lookup"><span data-stu-id="5bc79-116">Specifies the value of the server's class identifier in binary hex format.</span></span>                                                                                                                                           |



 

<span data-ttu-id="5bc79-117">Al definir la **macro Register \_ proxy \_ dll** al compilar dlldata. c, el archivo dll de serialización de proxy/stub incluirá automáticamente las definiciones predeterminadas para las funciones **DllMain**, **DllRegisterServer** y **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="5bc79-117">By defining the **REGISTER\_PROXY\_DLL** macro when compiling Dlldata.c, your proxy/stub marshaling DLL will automatically include default definitions for the **DllMain**, **DllRegisterServer**, and **DllUnregisterServer** functions.</span></span> <span data-ttu-id="5bc79-118">Puede usar estas funciones para registrar automáticamente el archivo DLL del proxy en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="5bc79-118">You can use these functions to self-register your proxy DLL in the system registry.</span></span>

<span data-ttu-id="5bc79-119">Este código de registro predeterminado usa el GUID de la primera interfaz que se encuentra como CLSID para registrar todo el servidor DLL de proxy/código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="5bc79-119">This default registration code uses the GUID of the first interface encountered as the CLSID for registering the entire proxy/stub DLL server.</span></span> <span data-ttu-id="5bc79-120">COM más adelante utiliza este CLSID para buscar y cargar el servidor proxy/stub compilado para el cálculo de referencias de cualquiera de las interfaces que el servidor está registrado para controlar.</span><span class="sxs-lookup"><span data-stu-id="5bc79-120">COM later uses this CLSID to locate and load the compiled proxy/stub server for the marshaling of any of the interfaces the server is registered to handle.</span></span> <span data-ttu-id="5bc79-121">Cuando una aplicación realiza una llamada a un método de interfaz que cruza los límites de subprocesos, procesos o equipos, COM usa la entrada del registro del identificador de interfaz para buscar la entrada del registro CLSID para el servidor de serialización de proxy/código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="5bc79-121">When an application makes an interface method call that crosses thread, process, or computer boundaries, COM uses the interface identifier registry entry to locate the CLSID registry entry for the proxy/stub marshaling server.</span></span> <span data-ttu-id="5bc79-122">A continuación, usa este CLSID para cargar el servidor (si aún no está cargado), de modo que se pueda calcular la llamada a la interfaz.</span><span class="sxs-lookup"><span data-stu-id="5bc79-122">It then uses this CLSID to load the server (if it isn't already loaded) so that the interface call can then be marshaled.</span></span>

<span data-ttu-id="5bc79-123">Use la **macro \_ CLSID** = <clsid> de proxy si desea especificar explícitamente el CLSID del servidor proxy/código auxiliar en lugar de confiar en el CLSID predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5bc79-123">Use the **PROXY\_CLSID**=<clsid> macro when you want to explicitly specify the proxy/stub server's CLSID rather than rely on the default CLSID.</span></span> <span data-ttu-id="5bc79-124">Por ejemplo, si va a compilar un archivo DLL de serialización estándar como su propio servidor COM en proceso, o si necesita definir su propio **DllMain** para controlar la Asociación del proceso de dll \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5bc79-124">For example, if you are building a standard marshaling DLL as your own in-process COM server, or if you need to define your own **DllMain** to handle DLL\_PROCESS\_ATTACH.</span></span>

<span data-ttu-id="5bc79-125">Usar **CLSID de proxy \_ \_ es**= macro en lugar **de \_ CLSID del proxy** para definir el valor del CLSID en el formato hexadecimal binario que utiliza la macro de **definición de \_ GUID** .</span><span class="sxs-lookup"><span data-stu-id="5bc79-125">Use **PROXY\_CLSID\_IS**= macro instead of **PROXY\_CLSID** to define the value of the CLSID in the binary hexadecimal format that the **DEFINE\_GUID** macro uses.</span></span>

<span data-ttu-id="5bc79-126">Tenga en cuenta también que cuando se ejecuta la función predeterminada **DllRegisterServer** , se registra el servidor con ThreadingModel = both.</span><span class="sxs-lookup"><span data-stu-id="5bc79-126">Also note that when the default **DllRegisterServer** function runs, it registers the server with ThreadingModel=Both.</span></span>

<span data-ttu-id="5bc79-127">En el siguiente ejemplo de archivo make se usa la **\_ \_ dll del proxy de registro** y el **proxy \_ CLSID**= macros:</span><span class="sxs-lookup"><span data-stu-id="5bc79-127">The following makefile example uses the **REGISTER\_PROXY\_DLL** and **PROXY\_CLSID**= macros:</span></span>

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL \
    /DPROXY_CLSID=7a98c250-6808-11cf-b73b-00aa00b677a7
example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJX) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
```

<span data-ttu-id="5bc79-128">Para obtener más información sobre la opción de preprocesador [**/d**](-d.md) , consulte la documentación del compilador de C.</span><span class="sxs-lookup"><span data-stu-id="5bc79-128">For more information on the [**/D**](-d.md) preprocessor option, see your C compiler documentation.</span></span>

 

 




