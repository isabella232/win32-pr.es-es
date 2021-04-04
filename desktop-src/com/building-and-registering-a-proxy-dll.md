---
title: Compilar y registrar un archivo DLL de proxy
description: Si seleccionó serialización de proxy/código auxiliar para su aplicación, los archivos. c y. h generados por MIDL se deben compilar y vincular para crear un archivo DLL de proxy, y ese archivo DLL debe especificarse en el registro del sistema para que los clientes puedan encontrar las interfaces.
ms.assetid: 939e6eed-2a2d-4d90-8fbb-c07142e7ba70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b0dcd28359172ff2f90391d44a66f8f51a4cbf
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794037"
---
# <a name="building-and-registering-a-proxy-dll"></a><span data-ttu-id="958d1-103">Compilar y registrar un archivo DLL de proxy</span><span class="sxs-lookup"><span data-stu-id="958d1-103">Building and Registering a Proxy DLL</span></span>

<span data-ttu-id="958d1-104">Si seleccionó serialización de proxy/código auxiliar para su aplicación, los archivos. c y. h generados por MIDL se deben compilar y vincular para crear un archivo DLL de proxy, y ese archivo DLL debe especificarse en el registro del sistema para que los clientes puedan encontrar las interfaces.</span><span class="sxs-lookup"><span data-stu-id="958d1-104">If you chose proxy/stub marshaling for your application, the .c and .h files that MIDL generated must be compiled and linked to create a proxy DLL, and that DLL must be entered into the system registry so that clients can locate your interfaces.</span></span> <span data-ttu-id="958d1-105">El archivo generado por MIDL, dlldata. c, contiene las rutinas necesarias y otra información para compilar y registrar un archivo DLL de proxy/código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="958d1-105">The MIDL-generated file Dlldata.c contains the necessary routines and other information to build and register a proxy/stub DLL.</span></span>

<span data-ttu-id="958d1-106">El primer paso para crear el archivo DLL es escribir un archivo de definición de módulo para el vinculador, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="958d1-106">The first step in building the DLL is to write a module definition file for the linker, as shown in the following example:</span></span>

``` syntax
LIBRARY        example.dll
DESCRIPTION    'generic proxy/stub DLL'
EXPORTS        DllGetClassObject      @1 PRIVATE
               DllCanUnloadNow        @2 PRIVATE
               DllRegisterServer      @4 PRIVATE
               DllUnregisterServer    @5 PRIVATE
 
```

<span data-ttu-id="958d1-107">Como alternativa, puede especificar estas funciones exportadas en la línea de comandos de vínculo del archivo make.</span><span class="sxs-lookup"><span data-stu-id="958d1-107">Alternatively, you can specify these exported functions on the LINK command line of your makefile.</span></span>

<span data-ttu-id="958d1-108">Las funciones exportadas se declaran en rpcproxy. h, que dlldata. c incluye, y las implementaciones predeterminadas forman parte de la biblioteca en tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="958d1-108">The exported functions are declared in Rpcproxy.h, which Dlldata.c includes, and default implementations are part of the RPC run-time library.</span></span> <span data-ttu-id="958d1-109">COM utiliza estas funciones para crear un generador de clases, descargar los archivos DLL (después de asegurarse de que no existen objetos o bloqueos), recuperar información acerca de la DLL del proxy y registrar y anular el registro de la DLL del proxy.</span><span class="sxs-lookup"><span data-stu-id="958d1-109">COM uses these functions to create a class factory, unload DLLs (after making sure that no objects or locks exist), retrieve information about the proxy DLL, and to self-register and unregister the proxy DLL.</span></span> <span data-ttu-id="958d1-110">Para aprovechar estas funciones predefinidas, debe invocar la opción Cpreprocessor/D (o-D) al compilar los archivos dlldata. c y \_ p. c de ejemplo, como se muestra en el siguiente archivo Make:</span><span class="sxs-lookup"><span data-stu-id="958d1-110">To take advantage of these predefined functions, you need to invoke the Cpreprocessor /D (or -D) option when you compile the Dlldata.c and Example\_p.c files, as shown in the following makefile:</span></span>

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcndr.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJX) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(ORIXYSTUBLIBS)
    regsvr32 /s proxy.dll
 
```

<span data-ttu-id="958d1-111">Si no especifica estas definiciones de preprocesador en tiempo de compilación, estas funciones no se definen automáticamente.</span><span class="sxs-lookup"><span data-stu-id="958d1-111">If you do not specify these preprocessor definitions at compile time, these functions are not automatically defined.</span></span> <span data-ttu-id="958d1-112">(Es decir, las macros de rpcproxy. c se expanden a Nothing). Tendría que definirlas explícitamente en otro archivo de código fuente, cuyo módulo también se incluiría en la vinculación y la compilación finales en la línea de comandos del compilador de C.</span><span class="sxs-lookup"><span data-stu-id="958d1-112">(That is, the macros in Rpcproxy.c expand to nothing.) You would have to have defined them explicitly in another source file, whose module would also be included in the final linking and compilation on the C compiler command line.</span></span>

<span data-ttu-id="958d1-113">Cuando \_ se define el archivo DLL del proxy de registro \_ , rpcproxy. h proporciona un control de compilación condicional adicional con el proxy \_ CLSID =*GUID*, el \_ CLSID \_ del proxy es = el *valor explícito de GUID* y la cadena de prefijo de entrada \_ .</span><span class="sxs-lookup"><span data-stu-id="958d1-113">When REGISTER\_PROXY\_DLL is defined, Rpcproxy.h provides for additional conditional compilation control with PROXY\_CLSID=*guid*, PROXY\_CLSID\_IS=*explicit value of guid*, and ENTRY\_PREFIX=*prefix string*.</span></span> <span data-ttu-id="958d1-114">Estas definiciones de macro se describen con más detalle en [definiciones de compilador de C para proxy/stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) en la guía del programador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="958d1-114">These macro definitions are described in greater detail in [C-Compiler Definitions for Proxy/Stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) in the MIDL Programmer's Guide.</span></span>

## <a name="manually-registering-the-proxy-dll"></a><span data-ttu-id="958d1-115">Registrar manualmente el archivo DLL de proxy</span><span class="sxs-lookup"><span data-stu-id="958d1-115">Manually Registering the Proxy DLL</span></span>

<span data-ttu-id="958d1-116">Si, por alguna razón, no puede usar las rutinas de registro de código auxiliar de proxy predeterminado, puede registrar manualmente el archivo DLL agregando las siguientes entradas al registro del sistema, utilizando Regedt32.exe.</span><span class="sxs-lookup"><span data-stu-id="958d1-116">If for some reason you cannot use the default proxy stub registration routines, you can manually register the DLL by adding the following entries to the system registry, using Regedt32.exe.</span></span>

```
HKEY_CLASSES_ROOT
   Interface
      iid
         (Default) = ICustomInterfaceName
         ProxyStubClsid32 = {clsid}
```

```
HKEY_CLASSES_ROOT
   CLSID
      clsid
         (Default) = ICustomInterfaceName_PSFactory
         InprocServer32 = proxstub.dll
```

## <a name="related-topics"></a><span data-ttu-id="958d1-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="958d1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="958d1-118">Definiciones de compilador de C para proxy/códigos auxiliares</span><span class="sxs-lookup"><span data-stu-id="958d1-118">C-Compiler Definitions for Proxy/Stubs</span></span>](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs)
</dt> <dt>

[<span data-ttu-id="958d1-119">Registrar servidores COM</span><span class="sxs-lookup"><span data-stu-id="958d1-119">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="958d1-120">Registro automático</span><span class="sxs-lookup"><span data-stu-id="958d1-120">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 