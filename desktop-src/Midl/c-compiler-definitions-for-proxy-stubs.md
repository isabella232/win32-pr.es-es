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
# <a name="c-compiler-definitions-for-proxystubs"></a>Definiciones de compilador de C para proxy/códigos auxiliares

El archivo de encabezado rpcproxy. h incluye las siguientes definiciones de macro, cada una de las cuales puede ser útil al compilar una aplicación COM distribuida. Estas macros se invocan con el modificador de preprocesador [**/d**](-d.md) (o-D) en el tiempo de compilación de C.



| MACRO                                                                                                                                                                                           | Descripción                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| REGISTRAR \_ dll de proxy \_                                                                                                                                                                            | Genera funciones **DllMain**, **DllRegisterServer** y **DllUnregisterServer** para registrar automáticamente un archivo dll de proxy.                                                                                       |
| CLSID de PROXY \_ =<clsid>                                                                                                                                                                      | Especifica un identificador de clase para el servidor. Si no se define esta macro, el CLSID predeterminado es el primer identificador de interfaz que encuentra el compilador MIDL en la especificación IDL para el servidor proxy/código auxiliar. |
| El \_ CLSID del proxy \_ es = {0x *8hexdigits*, 0x *4hexdigits*, 0x *4hexdigits*, {0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*,}} | Especifica el valor del identificador de clase del servidor en formato hexadecimal binario.                                                                                                                                           |



 

Al definir la **macro Register \_ proxy \_ dll** al compilar dlldata. c, el archivo dll de serialización de proxy/stub incluirá automáticamente las definiciones predeterminadas para las funciones **DllMain**, **DllRegisterServer** y **DllUnregisterServer** . Puede usar estas funciones para registrar automáticamente el archivo DLL del proxy en el registro del sistema.

Este código de registro predeterminado usa el GUID de la primera interfaz que se encuentra como CLSID para registrar todo el servidor DLL de proxy/código auxiliar. COM más adelante utiliza este CLSID para buscar y cargar el servidor proxy/stub compilado para el cálculo de referencias de cualquiera de las interfaces que el servidor está registrado para controlar. Cuando una aplicación realiza una llamada a un método de interfaz que cruza los límites de subprocesos, procesos o equipos, COM usa la entrada del registro del identificador de interfaz para buscar la entrada del registro CLSID para el servidor de serialización de proxy/código auxiliar. A continuación, usa este CLSID para cargar el servidor (si aún no está cargado), de modo que se pueda calcular la llamada a la interfaz.

Use la **macro \_ CLSID** = <clsid> de proxy si desea especificar explícitamente el CLSID del servidor proxy/código auxiliar en lugar de confiar en el CLSID predeterminado. Por ejemplo, si va a compilar un archivo DLL de serialización estándar como su propio servidor COM en proceso, o si necesita definir su propio **DllMain** para controlar la Asociación del proceso de dll \_ \_ .

Usar **CLSID de proxy \_ \_ es**= macro en lugar **de \_ CLSID del proxy** para definir el valor del CLSID en el formato hexadecimal binario que utiliza la macro de **definición de \_ GUID** .

Tenga en cuenta también que cuando se ejecuta la función predeterminada **DllRegisterServer** , se registra el servidor con ThreadingModel = both.

En el siguiente ejemplo de archivo make se usa la **\_ \_ dll del proxy de registro** y el **proxy \_ CLSID**= macros:

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

Para obtener más información sobre la opción de preprocesador [**/d**](-d.md) , consulte la documentación del compilador de C.

 

 




