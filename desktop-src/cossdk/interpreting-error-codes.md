---
description: Interpretación de códigos de error
ms.assetid: df2fe03b-2f5f-4958-926f-17e3a025a9b5
title: Interpretación de códigos de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b15dfbfd183178132e6917aac04aab46c5ce90fac0fb59cdbb52cc30143159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990886"
---
# <a name="interpreting-error-codes"></a>Interpretación de códigos de error

Después de determinar qué aplicación es el origen de un problema, debe averiguar qué error se ha producido. Los errores se producen y notifican en diferentes formatos, en función del lenguaje que use la aplicación.

En Microsoft Visual C++, los valores correctos, de advertencia y de error se devuelven mediante un número de 32 bits conocido como **HRESULT**. Para obtener una lista de valores **HRESULT** definidos por el sistema, consulte el archivo de encabezado Winerror.h incluido con el SDK Windows. Este archivo incluye todos los códigos de error y descripciones de COM+. Para obtener más información sobre **los valores HRESULT,** vea [Control de errores.](/windows/desktop/com/error-handling-in-com)

En el lenguaje Java, se produce una instancia de com.ms.com.ComFailException para indicar un error, donde el objeto ComFailException especifica un **HRESULT**. Una instancia de com.ms.com.ComSuccessException indica que se ha hecho correctamente con un valor devuelto de False. Para obtener información sobre cómo interpretar estas excepciones, vea la documentación de Microsoft Visual J++.

> [!Note]  
> Los procesos del servidor de aplicaciones COM+ que hospedan objetos de Visual J++ no se inactivarán (incluso con cero objetos activos) a menos que desactive la depuración JIT en el IDE de VJ6. Para obtener información sobre cómo hacerlo, vea la documentación de Visual J++.

 

En Visual Basic, puede recuperar valores **HRESULT** examinando la propiedad Err.Number. Se puede recuperar una descripción del error con la propiedad Err.Description.

También puede usar la utilidad ERRLOOK en Microsoft Visual Studio para recuperar un mensaje de error del sistema o un mensaje de error de módulo. ERRLOOK recupera automáticamente el texto del mensaje de error si arrastra y coloca un valor hexadecimal o decimal desde el depurador de Visual Studio u otra aplicación habilitada para Automation. También puede escribir un valor si lo escribe o lo pega desde el Portapapeles del IDE y hace clic en **la opción Buscar.**

El siguiente método de C++ imprime una descripción del error, basándose en el **HRESULT de entrada.**


```C++
#include <stdio.h>
#include <windows.h>
#include <tchar.h>

void ErrorDescription(HRESULT hr) 
{ 
     if(FACILITY_WINDOWS == HRESULT_FACILITY(hr)) 
         hr = HRESULT_CODE(hr); 
     TCHAR* szErrMsg; 

     if(FormatMessage( 
       FORMAT_MESSAGE_ALLOCATE_BUFFER|FORMAT_MESSAGE_FROM_SYSTEM, 
       NULL, hr, MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), 
       (LPTSTR)&szErrMsg, 0, NULL) != 0) 
     { 
         _tprintf(TEXT("%s"), szErrMsg); 
         LocalFree(szErrMsg); 
     } else 
         _tprintf( TEXT("[Could not find a description for error # %#x.]\n"), hr); 
}
```



En la tabla siguiente se proporcionan descripciones de códigos de error comunes en COM+.



| Códigos de error                                                   | Definiciones                                                                                                                                                                                                      |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| COMADMIN \_ E \_ ALREADYINSTALLED<br/>                      | El objeto ya está registrado.<br/>                                                                                                                                                                     |
| ARCHIVO DE \_ APLICACIÓN COMADMIN E \_ \_ \_ READFAIL<br/>                   | Error al leer el archivo de aplicación.<br/>                                                                                                                                                          |
| VERSIÓN DEL \_ ARCHIVO \_ DE \_ APLICACIÓN COMADMIN E \_<br/>                    | Número de versión no válido en el archivo de aplicación.<br/>                                                                                                                                                           |
| COMADMIN \_ E \_ APP \_ FILE \_ WRITEFAIL<br/>                  | Error al escribir en el archivo de aplicación.<br/>                                                                                                                                                       |
| COMADMIN \_ E \_ APPDIRNOTFOUND<br/>                        | No se encontró el directorio de instalación de la aplicación.<br/>                                                                                                                                                          |
| APLICACIÓN COMQC \_ E \_ NO EN \_ \_ COLA<br/>                 | Solo se pueden crear aplicaciones COM+ marcadas como "en cola" mediante el moniker "queue".<br/>                                                                                                                      |
| COMADMIN \_ E \_ APPLICATIONEXISTS<br/>                     | La aplicación ya está instalada.<br/>                                                                                                                                                                 |
| COMADMIN \_ E \_ APPLID COINCIDE CON \_ \_ CLSID<br/>                | Un CLSID con el mismo GUID que el nuevo identificador de aplicación ya está instalado en esta máquina.<br/>                                                                                                            |
| LA APLICACIÓN \_ COMADMIN E \_ NO SE \_ ESTÁ \_ EJECUTANDO<br/>                     | La aplicación especificada no se está ejecutando actualmente.<br/>                                                                                                                                                   |
| COMADMIN \_ E \_ AUTHENTICATIONLEVEL<br/>                   | No se puede establecer el nivel de autenticación necesario para la solicitud de actualización.<br/>                                                                                                                                       |
| COMADMIN \_ E \_ BADPATH<br/>                               | La ruta de acceso del archivo no es válida.<br/>                                                                                                                                                                             |
| COMADMIN \_ E \_ BADREGISTRYLIBID<br/>                      | El identificador de la biblioteca de tipos registrado no es válido.<br/>                                                                                                                                                            |
| COMADMIN \_ E \_ BADREGISTRYPROGID<br/>                     | Falta el ProgID del componente o está dañado.<br/>                                                                                                                                                         |
| COMADMIN \_ E NO PUEDE EXPORTAR EL PROXY DE \_ \_ \_ \_ \_ APLICACIÓN<br/>          | El proxy de aplicación no se puede exportar.<br/>                                                                                                                                                              |
| COMADMIN \_ E NO PUEDE INICIAR LA \_ \_ \_ \_ APLICACIÓN<br/>                  | No se pudo iniciar la aplicación porque es una aplicación de biblioteca o un proxy de aplicación.<br/>                                                                                                       |
| COMADMIN \_ E NO PUEDE EXPORTAR LA APLICACIÓN \_ \_ \_ \_ SYS \_<br/>            | La aplicación del sistema no se puede exportar.<br/>                                                                                                                                                             |
| COMADMIN \_ E \_ CANT \_ SUBSCRIBE \_ TO \_ COMPONENT<br/>        | El usuario no puede suscribirse a este componente porque es posible que se haya importado el componente.<br/>                                                                                                             |
| COMADMIN \_ E \_ CANTCOPYFILE<br/>                          | Error al copiar el archivo.<br/>                                                                                                                                                                   |
| COMADMIN \_ E \_ CLSIDORIIDMISMATCH<br/>                    | Los CLID o IID del archivo de aplicación no coinciden con los archivos DLL correspondientes.<br/>                                                                                                                                      |
| COMADMIN \_ E \_ COMP \_ MOVE \_ BAD \_ DEST<br/>                 | Error al mover el componente porque la aplicación de destino ya no existe.<br/>                                                                                                                       |
| COMADMIN \_ E \_ COMP \_ MOVE \_ LOCKED<br/>                    | No se ha permitido el traslado del componente porque la aplicación de origen o de destino es una aplicación del sistema o está bloqueada actualmente contra los cambios.<br/>                                                |
| COMADMIN \_ E \_ COMPFILE \_ BADTLB<br/>                      | No se pudo cargar la biblioteca de tipos.<br/>                                                                                                                                                                 |
| COMADMIN \_ E \_ COMPFILE \_ CLASSNOTAVAIL<br/>               | El archivo DLL no admite los componentes enumerados en la biblioteca de tipos.<br/>                                                                                                                                   |
| COMADMIN \_ E \_ COMPFILE \_ DOESNOTEXIST<br/>                | Este archivo no existe.<br/>                                                                                                                                                                             |
| COMADMIN \_ E \_ COMPFILE \_ GETCLASSOBJ<br/>                 | Error [**del método GetClassObject**](/windows/desktop/api/objidl/nf-objidl-iclassactivator-getclassobject) en el archivo DLL.<br/>                                                                                                                |
| COMADMIN \_ E \_ COMPFILE \_ LOADDLDLDLIL<br/>                 | No se pudo cargar el archivo DLL.<br/>                                                                                                                                                                          |
| COMADMIN \_ E \_ COMPFILE \_ NOREGISTRAR<br/>                 | El registrador de componentes al que se hace referencia en este archivo no está disponible.<br/>                                                                                                                                     |
| COMADMIN \_ E \_ COMPFILE \_ NOTINSTALLABLE<br/>              | El archivo no contiene información de componentes o componentes.<br/>                                                                                                                                        |
| COMADMIN \_ E \_ COREQCOMPINSTALLED<br/>                    | Ya hay instalado un componente en el mismo archivo DLL.<br/>                                                                                                                                                     |
| COMADMIN \_ E \_ DLLLOADFAILED<br/>                         | No se pudo cargar el archivo DLL.<br/>                                                                                                                                                                          |
| COMADMIN \_ E \_ DLLREGISTERSERVER<br/>                     | Error [**en la función DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) cuando se instaló el componente.<br/>                                                                                                  |
| COMADMIN \_ E \_ EVENTCLASS NO PUEDE SER \_ \_ \_ SUSCRIPTOR<br/>      | Una clase de eventos no se puede configurar como un componente de suscriptor. Cuando se intenta crear una suscripción con una clase de eventos como suscriptor, se devuelve este error.<br/>                          |
| COMADMIN \_ E \_ INVALIDUSERIDS<br/>                        | Uno o varios usuarios del archivo de aplicación no son válidos.<br/>                                                                                                                                              |
| COMADMIN \_ E \_ KEYMISSING<br/>                            | El objeto no se encontró en el catálogo.<br/>                                                                                                                                                              |
| COMADMIN \_ E \_ LIB \_ APP \_ PROXY \_ INCOMPATIBLE<br/>         | Las aplicaciones de biblioteca y los servidores proxy de aplicación son incompatibles. Este error se devuelve cuando se intenta exportar un proxy de aplicación y la propiedad de activación de la aplicación es una biblioteca. <br/> |
| COMADMIN \_ E \_ NOREGISTRYCLSID<br/>                       | Falta el CLSID del componente o está dañado.<br/>                                                                                                                                                          |
| COMADMIN \_ E \_ NOSERVERSHARE<br/>                         | No hay ningún recurso compartido de archivos de servidor disponible.<br/>                                                                                                                                                                    |
| COMADMIN \_ E \_ NOTCHANGEABLE<br/>                         | Se han deshabilitado los cambios realizados en este objeto y sus subelementos.<br/>                                                                                                                                        |
| COMADMIN \_ E \_ NOTDELETEABLE<br/>                         | La función delete se ha deshabilitado para este objeto.<br/>                                                                                                                                                |
| COMADMIN \_ E \_ NOTINREGISTRY<br/>                         | No se encontró el objeto en el Registro.<br/>                                                                                                                                                                     |
| COMADMIN \_ E \_ NOUSER<br/>                                | Uno o varios usuarios no son válidos.<br/>                                                                                                                                                                      |
| EL OBJETO \_ COMADMIN E \_ NO \_ \_ \_ EXISTE<br/>              | No se encuentra uno de los objetos especificados.<br/>                                                                                                                                                         |
| FALTA EL ELEMENTO \_ PRIMARIO \_ DEL \_ OBJETO COMADMIN E \_<br/>               | Uno de los objetos que se insertan o actualizan no pertenece a una colección primaria válida.<br/>                                                                                                            |
| COMADMIN \_ E \_ OBJECTERRORS<br/>                          | Se produjeron errores al acceder a uno o varios objetos. Para obtener más información, vea la [**colección ErrorInfo.**](errorinfo.md)<br/>                                                                               |
| COMADMIN \_ E \_ OBJECTEXISTS<br/>                          | El objeto que está intentando agregar o cambiar de nombre ya existe.<br/>                                                                                                                                        |
| COMADMIN \_ E \_ OBJECTINVALID<br/>                         | Faltan una o varias de las propiedades del objeto o no son válidas.<br/>                                                                                                                                        |
| COMADMIN \_ E \_ OBJECTNOTPOOLABLE<br/>                     | Este objeto no se puede agrupar.<br/>                                                                                                                                                                      |
| COMADMIN \_ E \_ PROPERTYSAVEFAILED<br/>                    | Una o varias configuraciones de propiedad no son válidas o están en conflicto entre sí.<br/>                                                                                                                      |
| COMADMIN \_ E \_ PROPERTY \_ OVERFLOW<br/>                    | El valor de propiedad es demasiado grande.<br/>                                                                                                                                                                      |
| COMADMIN \_ E \_ REGFILE \_ DAÑADO<br/>                      | El archivo de registro está dañado.<br/>                                                                                                                                                                     |
| COMADMIN \_ E \_ REGISTERTLB<br/>                           | El sistema no pudo registrar la biblioteca de tipos.<br/>                                                                                                                                                   |
| COMADMIN \_ E \_ REGISTRARFAILED<br/>                       | Se produjeron errores en el registrador de componentes.<br/>                                                                                                                                                     |
| COMADMIN \_ E \_ REMOTEINTERFACE<br/>                       | Falta información de interfaz o se ha cambiado.<br/>                                                                                                                                                   |
| COMADMIN \_ E REQUIERE UNA PLATAFORMA \_ \_ \_ DIFERENTE<br/>         | Esta operación no está habilitada en esta plataforma.<br/>                                                                                                                                                       |
| EL ROL E DE COMADMIN \_ \_ NO \_ \_ \_ EXISTE<br/>                | Un rol asignado a un componente, interfaz o método no existe en la aplicación.<br/>                                                                                                               |
| COMADMIN \_ E \_ ROLEEXISTS<br/>                            | El rol ya existe.<br/>                                                                                                                                                                              |
| COMADMIN \_ E \_ SERVICENOTINSTALLED<br/>                   | El servicio no está instalado.<br/>                                                                                                                                                                         |
| SESIÓN \_ E DE \_ COMADMIN<br/>                               | No se admite la versión del catálogo de servidores.<br/>                                                                                                                                                          |
| COMADMIN \_ S \_ SOMEALREADYPAUSED<br/>                     | Uno o varios de los procesos de aplicación especificados ya estaban en pausa.<br/>                                                                                                                               |
| COMADMIN \_ S \_ SOMEALREADYRUNNING<br/>                    | Uno o varios de los procesos de aplicación especificados ya se estaban ejecutando.<br/>                                                                                                                              |
| COMADMIN \_ E \_ START \_ APP \_ NEEDS \_ COMPONENTS<br/>         | Para iniciar la aplicación, debe tener componentes en una aplicación.<br/>                                                                                                                                 |
| COMADMIN \_ E \_ SVCAPP NO ES \_ \_ AGRUPABLE NI \_ \_ RECICLABLE<br/> | Es posible que las aplicaciones COM+ que se ejecutan como un servicio NT no se marquen como agrupadas o recicladas.<br/>                                                                                                               |
| COMADMIN \_ E \_ SYSTEMAPP<br/>                             | Esta operación no se puede realizar en la aplicación del sistema.<br/>                                                                                                                                         |
| USUARIO COMADMIN \_ E \_ EN \_ \_ SET<br/>                         | Uno o varios usuarios ya están asignados a un conjunto de particiones local.<br/>                                                                                                                                      |
| COMADMIN \_ E \_ USERPASSWDNOTVALID<br/>                    | La identidad o contraseña establecida en la aplicación no es válida.<br/>                                                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aislamiento de errores y directiva de conmutación por error](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Buscar el origen de un error](finding-the-source-of-an-error.md)
</dt> <dt>

[Cómo modifica COM+ los valores devueltos](how-com--modifies-return-values.md)
</dt> <dt>

[Estrategias para controlar errores en COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Solución de problemas](troubleshooting-the-com--crm.md)
</dt> </dl>

 

