---
title: Definiciones de C-Compiler para proxy/código auxiliar
description: El archivo de encabezado Rpcproxy.h incluye las siguientes definiciones de macro, cada una de las cuales puede resultar cómoda al compilar una aplicación COM distribuida. Estas macros se invocan con el modificador de preprocesador /D (o -D) en tiempo de compilación de C.
ms.assetid: 697f0b63-76ae-410d-8bbf-bb95295ffba9
keywords:
- MIDL del compilador MIDL, compilador de C, definiciones de proxy/stubs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f12b9fd1e2688545137dba870816c1765102ce3593d09ea3cb062bd8250c7c28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807847"
---
# <a name="c-compiler-definitions-for-proxystubs"></a>Definiciones de C-Compiler para proxy/código auxiliar

El archivo de encabezado Rpcproxy.h incluye las siguientes definiciones de macro, cada una de las cuales puede resultar cómoda al compilar una aplicación COM distribuida. Estas macros se invocan con el modificador de preprocesador [**/D**](-d.md) (o -D) en tiempo de compilación de C.



| MACRO                                                                                                                                                                                           | Descripción                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| REGISTRAR \_ DLL DE \_ PROXY                                                                                                                                                                            | Genera las **funciones DllMain,** **DllRegisterServer** y **DllUnregisterServer** para registrar automáticamente un archivo DLL de proxy.                                                                                       |
| PROXY \_ CLSID=<clsid>                                                                                                                                                                      | Especifica un identificador de clase para el servidor. Si no se define esta macro, el CLSID predeterminado es el primer identificador de interfaz que el compilador MIDL encuentra en la especificación de IDL para el servidor Proxy/Stub. |
| PROXY \_ CLSID \_ IS={0x *8hexdigits*, 0x *4hexdigits*,0x *4hexdigits*, {0x *2hexdigits,0x**2hexdigits*, 0x *2hexdigits*,0x *2hexdigits,**0x 2hexdigits,0x**2hexdigits,* 0x *2hexdigits,0x**2hexdigits*,}} | Especifica el valor del identificador de clase del servidor en formato hexadecimal binario.                                                                                                                                           |



 

Al definir la macro **REGISTER \_ PROXY \_ DLL** al compilar Dlldata.c, el archivo DLL de serialización de proxy/stub incluirá automáticamente definiciones predeterminadas para las funciones **DllMain,** **DllRegisterServer** y **DllUnregisterServer.** Puede usar estas funciones para registrar de forma automática el archivo DLL de proxy en el registro del sistema.

Este código de registro predeterminado usa el GUID de la primera interfaz encontrada como CLSID para registrar todo el servidor DLL de proxy o código auxiliar. COM usa más adelante este CLSID para buscar y cargar el servidor proxy/stub compilado para la serialización de cualquiera de las interfaces que el servidor está registrado para controlar. Cuando una aplicación realiza una llamada al método de interfaz que cruza los límites de subprocesos, procesos o equipos, COM usa la entrada del Registro del identificador de interfaz para buscar la entrada del Registro CLSID para el servidor de serialización de proxy o código auxiliar. A continuación, usa este CLSID para cargar el servidor (si aún no está cargado) para que la llamada a la interfaz se pueda serializar.

Use la **macro \_ CLSID de PROXY** cuando desee especificar explícitamente el CLSID del servidor proxy/stub en lugar de basarse en el = <clsid> CLSID predeterminado. Por ejemplo, si está creando un archivo DLL de serialización estándar como su propio servidor COM en proceso, o si necesita definir su propio **archivo DllMain** para controlar DLL \_ PROCESS \_ ATTACH.

Use **PROXY \_ CLSID \_ IS**= macro en lugar de **\_ CLSID** de PROXY para definir el valor del CLSID en el formato hexadecimal binario que usa la macro **DEFINE \_ GUID.**

Tenga en cuenta también que cuando se ejecuta la función **DllRegisterServer** predeterminada, registra el servidor con ThreadingModel=Both.

En el siguiente ejemplo de archivo Make se usan las macros **REGISTER \_ PROXY \_ DLL** y **PROXY \_ CLSID**= :

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

Para obtener más información sobre la opción de preprocesador [**/D,**](-d.md) consulte la documentación del compilador de C.

 

 




