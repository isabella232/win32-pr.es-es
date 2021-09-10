---
title: Self-Registration
description: El registro propio es el medio estándar a través del cual un módulo de servidor puede empaquetar sus propias operaciones de registro, tanto de registro como de anulación de registro, en el propio módulo.
ms.assetid: fb5dcb2b-b0e3-4f37-a8e7-b84b9a265227
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c95d422213b8e33ac89b89408ed95724f0769b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369704"
---
# <a name="self-registration"></a>Self-Registration

A medida que el software de componentes siga creciendo como mercado, habrá cada vez más instancias en las que un usuario obtenga un nuevo componente de software como un único módulo DLL o EXE, como al descargar un nuevo componente desde un servicio en línea o recibir uno de un amigo en un disquete. En estos casos, no es práctico exigir al usuario que pase por un largo procedimiento de instalación o programa de instalación. Además de los problemas de licencia, que se controlan a través de [**IClassFactory2,**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)un procedimiento de instalación normalmente crea las entradas del Registro necesarias para que un componente se ejecute correctamente en el contexto COM y OLE.

El registro propio es el medio estándar a través del cual un módulo de servidor puede empaquetar sus propias operaciones de registro, tanto de registro como de anulación de registro, en el propio módulo. Cuando se usa con licencias que se administran a través de [**IClassFactory2,**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)un servidor puede convertirse en un módulo completamente independiente sin necesidad de programas de instalación externos o archivos .reg.

Cualquier módulo de registro propio, DLL o EXE, debe incluir primero una cadena "OleSelfRegister" en la sección [StringFileInfo](/windows/desktop/menurc/stringfileinfo-block) de su recurso de información de versión, como se muestra aquí.

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

La existencia de estos datos permite a cualquier parte interesada, como una aplicación que desee integrar este nuevo componente, determinar si el servidor admite el registro propio sin tener que cargar primero el archivo DLL o EXE.

Si el servidor está empaquetado en un módulo DLL, el archivo DLL debe exportar las funciones [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) [**y DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver). Cualquier aplicación que desee indicar al servidor que se registre a sí mismo (es decir, todos sus CLSID e IDs de biblioteca de tipos) puede obtener un puntero a **DllRegisterServer** a través de la [**función GetProcAddress.**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) En **DllRegisterServer**, el archivo DLL crea todas sus entradas del Registro necesarias, almacenando la ruta de acceso correcta al archivo DLL para todas las [entradas InprocServer32](inprocserver32.md) o [InprocHandler32.](inprochandler32.md)

Cuando una aplicación desea quitar el componente del sistema, debe anular el registro de ese componente llamando [**a DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver). Dentro de esta llamada, el servidor quita exactamente las entradas que creó anteriormente en [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver). El servidor no debe quitar todas las entradas de sus clases porque es posible que otro software haya almacenado entradas adicionales, como una [clave TreatAs.](treatas.md)

Si el servidor está empaquetado en un módulo EXE, la aplicación que desea registrar el servidor inicia el servidor EXE con el argumento de línea de comandos **/RegServer** o **-RegServer** (sin que se tenga en cuenta mayúsculas de minúsculas). Si la aplicación desea anular el registro del servidor, inicia el archivo EXE con el argumento de línea de comandos **/UnregServer** o **-UnregServer**. El archivo EXE de registro propio detecta estos argumentos de línea de comandos e invoca las mismas operaciones que un archivo DLL en [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)y [**DllUnregisterServer,**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)respectivamente, registrando su ruta de acceso del módulo en [LocalServer32](localserver32.md) en lugar de **InprocServer32** **o InprocHandler32.**

El servidor debe registrar la ruta de acceso completa a la ubicación de instalación del módulo DLL o EXE para sus claves **InprocServer32**, **InprocHandler32** y **LocalServer32** respectivas en el Registro. La ruta de acceso del módulo se obtiene fácilmente a través [**de la función GetModuleFileName.**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instalación como una aplicación de servicio](installing-as-a-service-application.md)
</dt> <dt>

[Registro de una clase durante la instalación](registering-a-class-at-installation.md)
</dt> <dt>

[Registro de un servidor EXE en ejecución](registering-a-running-exe-server.md)
</dt> <dt>

[Registrar objetos en ROT](registering-objects-in-the-rot.md)
</dt> </dl>

 

 