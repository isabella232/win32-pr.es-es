---
title: Compilar y registrar un archivo DLL de proxy
description: Si eligió la serialización de proxy o código auxiliar para la aplicación, los archivos .c y .h generados por MIDL deben compilarse y vincularse para crear un archivo DLL de proxy, y ese archivo DLL debe especificarse en el registro del sistema para que los clientes puedan encontrar las interfaces.
ms.assetid: 939e6eed-2a2d-4d90-8fbb-c07142e7ba70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d4cafbe2be56d9e9a02a451e3daf905496c424
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826810"
---
# <a name="building-and-registering-a-proxy-dll"></a>Compilar y registrar un archivo DLL de proxy

Si eligió la serialización de proxy o código auxiliar para la aplicación, los archivos .c y .h generados por MIDL deben compilarse y vincularse para crear un archivo DLL de proxy, y ese archivo DLL debe especificarse en el registro del sistema para que los clientes puedan encontrar las interfaces. El archivo dlldata.c generado por MIDL contiene las rutinas necesarias y otra información para compilar y registrar un archivo DLL de proxy o código auxiliar.

El primer paso para compilar el archivo DLL es escribir un archivo de definición de módulo para el vinculador, como se muestra en el ejemplo siguiente:

``` syntax
LIBRARY        example.dll
DESCRIPTION    'generic proxy/stub DLL'
EXPORTS        DllGetClassObject      @1 PRIVATE
               DllCanUnloadNow        @2 PRIVATE
               DllRegisterServer      @4 PRIVATE
               DllUnregisterServer    @5 PRIVATE
 
```

Como alternativa, puede especificar estas funciones exportadas en la línea de comandos LINK del archivo Make.

Las funciones exportadas se declaran en Rpcproxy.h, que incluye Dlldata.c, y las implementaciones predeterminadas forman parte de la biblioteca en tiempo de ejecución de RPC. COM usa estas funciones para crear un generador de clases, descargar archivos DLL (después de asegurarse de que no existen objetos o bloqueos), recuperar información sobre el archivo DLL de proxy y registrar automáticamente y anular el registro del archivo DLL del proxy. Para aprovechar estas funciones predefinidas, debe invocar la opción Cpreprocessor /D (o -D) al compilar los archivos Dlldata.c y Example p.c, como se muestra en el siguiente \_ archivo Make:

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
proxy.dll : $(PROXYSTUBOBJS) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
 
```

Si no especifica estas definiciones de preprocesador en tiempo de compilación, estas funciones no se definen automáticamente. (Es decir, las macros de Rpcproxy.c no se expanden a nada). Tendría que haberlas definido explícitamente en otro archivo de código fuente, cuyo módulo también se incluiría en la vinculación y compilación finales en la línea de comandos del compilador de C.

Cuando se define REGISTER PROXY DLL, Rpcproxy.h proporciona un control de compilación condicional adicional con \_ \_ PROXY \_ CLSID=*guid,* proxy \_ CLSID IS= \_ *valor* \_ explícito de guid y cadena de prefijo ENTRY PREFIX=. Estas definiciones de macro se describen con más detalle en [C-Compiler Definitions for Proxy/Stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) (Definiciones del compilador de C para proxy/stubs) en midl Programmer's Guide (Guía del programador de MIDL).

## <a name="manually-registering-the-proxy-dll"></a>Registro manual del archivo DLL de proxy

Si por alguna razón no puede usar las rutinas de registro de código auxiliar de proxy predeterminadas, puede registrar manualmente el archivo DLL agregando las siguientes entradas al registro del sistema mediante Regedt32.exe.

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

[Definiciones de C-Compiler para proxy/código auxiliar](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs)
</dt> <dt>

[Registro de servidores COM](registering-com-servers.md)
</dt> <dt>

[Registro propio](self-registration.md)
</dt> </dl>

 

 
