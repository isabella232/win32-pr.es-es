---
title: Self-Registration
description: El registro automático es el medio estándar a través del cual un módulo de servidor puede empaquetar sus propias operaciones del registro, tanto el registro como la anulación del registro, en el propio módulo.
ms.assetid: fb5dcb2b-b0e3-4f37-a8e7-b84b9a265227
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c95d422213b8e33ac89b89408ed95724f0769b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488339"
---
# <a name="self-registration"></a>Self-Registration

A medida que el software de componentes sigue creciendo como un mercado, habrá más instancias en las que un usuario obtiene un nuevo componente de software como un solo módulo DLL o EXE, como cuando se descarga un componente nuevo desde un servicio en línea o se recibe uno de un amigo en un disquete. En estos casos, no es práctico requerir al usuario que realice un procedimiento de instalación o un programa de instalación largo. Además de los problemas de licencia, que se administran a través de [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), un procedimiento de instalación crea normalmente las entradas del registro necesarias para que un componente se ejecute correctamente en el contexto com y OLE.

El registro automático es el medio estándar a través del cual un módulo de servidor puede empaquetar sus propias operaciones del registro, tanto el registro como la anulación del registro, en el propio módulo. Cuando se usa con licencias que se administran a través de [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), un servidor puede convertirse en un módulo totalmente independiente sin necesidad de programas de instalación externos o archivos. reg.

Cualquier módulo de registro automático, DLL o EXE, debe incluir primero una cadena "OleSelfRegister" en la sección [StringFileInfo](/windows/desktop/menurc/stringfileinfo-block) de su recurso de información de versión, como se muestra aquí.

``` syntax
VS_VERSION_INFO VERSIONINFO 
 
 ... 
 
 BEGIN 
   BLOCK "StringFileInfo" 
    BEGIN 
#ifdef UNICODE 
     BLOCK "040904B0" // Lang=US English, CharSet=Unicode 
#else 
     BLOCK "040904E4" // Lang=US English, CharSet=Windows Multilingual 
#endif 
      BEGIN 
       ... 
       VALUE "OLESelfRegister", "\0" 
      END 
 
   ... 
 
   END 
 
 ... 
 
 END 
 
```

La existencia de estos datos permite que cualquier parte interesada, como una aplicación que desee integrar este nuevo componente, determine si el servidor admite el registro automático sin tener que cargar primero el archivo DLL o EXE.

Si el servidor está empaquetado en un módulo DLL, el archivo DLL debe exportar las funciones [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver). Cualquier aplicación que desee indicar al servidor que se registre (es decir, todos sus CLSID e identificadores de biblioteca de tipos) puede obtener un puntero a **DllRegisterServer** a través de la función [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) . En **DllRegisterServer**, el archivo dll crea todas las entradas del registro necesarias, almacenando la ruta de acceso correcta a la dll para todas las entradas [InProcServer32](inprocserver32.md) o [InprocHandler32](inprochandler32.md) .

Cuando una aplicación desea quitar el componente del sistema, debe anular el registro de ese componente llamando a [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver). Dentro de esta llamada, el servidor quita exactamente las entradas creadas anteriormente en [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver). El servidor no debe quitar ciegamente todas las entradas de sus clases porque es posible que otro software haya almacenado entradas adicionales, como una clave [treatAs](treatas.md) .

Si el servidor está empaquetado en un módulo EXE, la aplicación que desea registrar el servidor inicia el servidor EXE con el argumento de línea de comandos **/regserver** o **-regserver** (no distingue mayúsculas de minúsculas). Si la aplicación desea anular el registro del servidor, inicia el archivo EXE con el argumento de línea de comandos **modificador/unregserver** o **-UnregServer**. El archivo EXE de registro automático detecta estos argumentos de línea de comandos e invoca las mismas operaciones que una DLL en [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)y [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver), respectivamente, registrando la ruta de acceso del módulo en [LocalServer32](localserver32.md) en lugar de **InProcServer32** o **InprocHandler32**.

El servidor debe registrar la ruta de acceso completa a la ubicación de instalación del módulo DLL o EXE para sus correspondientes claves **InProcServer32**, **InprocHandler32** y **LocalServer32** en el registro. La ruta de acceso del módulo se obtiene fácilmente a través de la función [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instalar como una aplicación de servicio](installing-as-a-service-application.md)
</dt> <dt>

[Registrar una clase durante la instalación](registering-a-class-at-installation.md)
</dt> <dt>

[Registrar un servidor EXE en ejecución](registering-a-running-exe-server.md)
</dt> <dt>

[Registrar objetos en la tabla ROT](registering-objects-in-the-rot.md)
</dt> </dl>

 

 