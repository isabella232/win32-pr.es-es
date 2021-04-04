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
# <a name="building-and-registering-a-proxy-dll"></a>Compilar y registrar un archivo DLL de proxy

Si seleccionó serialización de proxy/código auxiliar para su aplicación, los archivos. c y. h generados por MIDL se deben compilar y vincular para crear un archivo DLL de proxy, y ese archivo DLL debe especificarse en el registro del sistema para que los clientes puedan encontrar las interfaces. El archivo generado por MIDL, dlldata. c, contiene las rutinas necesarias y otra información para compilar y registrar un archivo DLL de proxy/código auxiliar.

El primer paso para crear el archivo DLL es escribir un archivo de definición de módulo para el vinculador, tal como se muestra en el ejemplo siguiente:

``` syntax
LIBRARY        example.dll
DESCRIPTION    'generic proxy/stub DLL'
EXPORTS        DllGetClassObject      @1 PRIVATE
               DllCanUnloadNow        @2 PRIVATE
               DllRegisterServer      @4 PRIVATE
               DllUnregisterServer    @5 PRIVATE
 
```

Como alternativa, puede especificar estas funciones exportadas en la línea de comandos de vínculo del archivo make.

Las funciones exportadas se declaran en rpcproxy. h, que dlldata. c incluye, y las implementaciones predeterminadas forman parte de la biblioteca en tiempo de ejecución de RPC. COM utiliza estas funciones para crear un generador de clases, descargar los archivos DLL (después de asegurarse de que no existen objetos o bloqueos), recuperar información acerca de la DLL del proxy y registrar y anular el registro de la DLL del proxy. Para aprovechar estas funciones predefinidas, debe invocar la opción Cpreprocessor/D (o-D) al compilar los archivos dlldata. c y \_ p. c de ejemplo, como se muestra en el siguiente archivo Make:

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

Si no especifica estas definiciones de preprocesador en tiempo de compilación, estas funciones no se definen automáticamente. (Es decir, las macros de rpcproxy. c se expanden a Nothing). Tendría que definirlas explícitamente en otro archivo de código fuente, cuyo módulo también se incluiría en la vinculación y la compilación finales en la línea de comandos del compilador de C.

Cuando \_ se define el archivo DLL del proxy de registro \_ , rpcproxy. h proporciona un control de compilación condicional adicional con el proxy \_ CLSID =*GUID*, el \_ CLSID \_ del proxy es = el *valor explícito de GUID* y la cadena de prefijo de entrada \_ . Estas definiciones de macro se describen con más detalle en [definiciones de compilador de C para proxy/stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) en la guía del programador de MIDL.

## <a name="manually-registering-the-proxy-dll"></a>Registrar manualmente el archivo DLL de proxy

Si, por alguna razón, no puede usar las rutinas de registro de código auxiliar de proxy predeterminado, puede registrar manualmente el archivo DLL agregando las siguientes entradas al registro del sistema, utilizando Regedt32.exe.

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

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Definiciones de compilador de C para proxy/códigos auxiliares](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs)
</dt> <dt>

[Registrar servidores COM](registering-com-servers.md)
</dt> <dt>

[Registro automático](self-registration.md)
</dt> </dl>

 

 