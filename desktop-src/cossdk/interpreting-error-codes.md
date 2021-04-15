---
description: Interpretar códigos de error
ms.assetid: df2fe03b-2f5f-4958-926f-17e3a025a9b5
title: Interpretar códigos de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659ee7def9feff50d375a07ab201e1cca25bffd7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677223"
---
# <a name="interpreting-error-codes"></a>Interpretar códigos de error

Después de determinar qué aplicación es el origen de un problema, debe averiguar qué error se ha producido. Los errores se generan y se muestran en diferentes formatos, en función del lenguaje que use la aplicación.

En Microsoft Visual C++, se devuelven valores correctos, de advertencia y de error mediante un número de 32 bits conocido como **HRESULT**. Para obtener una lista de valores **HRESULT** definidos por el sistema, vea el archivo de encabezado Winerror. h incluido con el Windows SDK. Este archivo incluye todos los códigos de error y descripciones de COM+. Para obtener más información sobre los valores **HRESULT** , vea [control de errores](/windows/desktop/com/error-handling-in-com).

En el lenguaje Java, se inicia una instancia de com. ms. com. ComFailException para indicar un error, donde el objeto ComFailException especifica un **valor HRESULT**. Una instancia de com. ms. com. ComSuccessException indica Success con un valor devuelto de false. Para obtener información sobre cómo interpretar estas excepciones, vea la documentación de Microsoft Visual J++.

> [!Note]  
> Los procesos del servidor de aplicaciones COM+ que hospedan objetos de Visual J++ no estarán inactivos (incluso con cero objetos activos) a menos que desactive la depuración JIT en el IDE de VJ6. Para obtener información sobre cómo hacerlo, consulte la documentación de Visual J++.

 

En Visual Basic, puede recuperar los valores **HRESULT** mediante el examen de la propiedad Err. Number. Se puede recuperar una descripción del error con la propiedad Err. Description.

También puede usar la utilidad ERRLOOK en Microsoft Visual Studio para recuperar un mensaje de error del sistema o un mensaje de error del módulo. ERRLOOK recupera automáticamente el texto del mensaje de error si arrastra y coloca un valor hexadecimal o decimal desde el depurador de Visual Studio u otra aplicación habilitada para automatización. También puede escribir un valor escribiéndolo o pegándolo desde el Portapapeles del IDE y haciendo clic en la opción **Buscar** .

El siguiente método de C++ imprime una descripción del error, en función del **HRESULT** de entrada.


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



En la tabla siguiente se proporcionan descripciones de los códigos de error comunes en COM+.



| Códigos de error                                                   | Definiciones                                                                                                                                                                                                      |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| COMAdmin \_ E \_ ALREADYINSTALLED<br/>                      | El objeto ya está registrado.<br/>                                                                                                                                                                     |
| COMAdmin \_ E \_ archivo de aplicación \_ \_ READFAIL<br/>                   | Error al leer el archivo de aplicación.<br/>                                                                                                                                                          |
| versión del \_ \_ archivo de \_ aplicación \_ de COMAdmin<br/>                    | Número de versión no válido en el archivo de aplicación.<br/>                                                                                                                                                           |
| COMAdmin \_ E \_ archivo de aplicación \_ \_ WRITEFAIL<br/>                  | Error al escribir en el archivo de aplicación.<br/>                                                                                                                                                       |
| COMAdmin \_ E \_ APPDIRNOTFOUND<br/>                        | No se encontró el directorio de instalación de la aplicación.<br/>                                                                                                                                                          |
| \_aplicación COMQC \_ E \_ no \_ en cola<br/>                 | Solo las aplicaciones COM+ marcadas como "en cola" se pueden crear mediante el moniker "cola".<br/>                                                                                                                      |
| COMAdmin \_ E \_ APPLICATIONEXISTS<br/>                     | La aplicación ya está instalada.<br/>                                                                                                                                                                 |
| la E/s de comadministración \_ \_ \_ coincide con \_ CLSID<br/>                | Ya hay instalado en este equipo un CLSID con el mismo GUID que el nuevo identificador de aplicación.<br/>                                                                                                            |
| aplicación COMAdmin \_ E \_ no se \_ \_ está ejecutando<br/>                     | La aplicación especificada no se está ejecutando actualmente.<br/>                                                                                                                                                   |
| COMAdmin \_ E \_ AUTHENTICATIONLEVEL<br/>                   | No se puede establecer el nivel de autenticación necesario para la solicitud de actualización.<br/>                                                                                                                                       |
| COMAdmin \_ E \_ BADPATH<br/>                               | La ruta de acceso del archivo no es válida.<br/>                                                                                                                                                                             |
| COMAdmin \_ E \_ BADREGISTRYLIBID<br/>                      | El ID. de la biblioteca de tipos registrados no es válido.<br/>                                                                                                                                                            |
| COMAdmin \_ E \_ BADREGISTRYPROGID<br/>                     | Falta el ProgID del componente o está dañado.<br/>                                                                                                                                                         |
| COMAdmin \_ E \_ \_ no puede \_ exportar \_ el \_ proxy de aplicación<br/>          | El proxy de aplicación no es exportable.<br/>                                                                                                                                                              |
| COMAdmin \_ E \_ \_ no puede \_ iniciar la \_ aplicación<br/>                  | No se pudo iniciar la aplicación porque es una aplicación de biblioteca o un proxy de aplicación.<br/>                                                                                                       |
| COMAdmin \_ E \_ \_ no puede \_ exportar \_ la \_ aplicación sys<br/>            | La aplicación del sistema no es exportable.<br/>                                                                                                                                                             |
| COMAdmin \_ E \_ no \_ se pudo suscribir \_ al \_ componente<br/>        | El usuario no puede suscribirse a este componente porque es posible que se haya importado.<br/>                                                                                                             |
| COMAdmin \_ E \_ CANTCOPYFILE<br/>                          | Error al copiar el archivo.<br/>                                                                                                                                                                   |
| COMAdmin \_ E \_ CLSIDORIIDMISMATCH<br/>                    | Los CLSID de archivo de aplicación o IID no coinciden con los archivos dll correspondientes.<br/>                                                                                                                                      |
| la comp. de COMAdmin \_ E \_ \_ mueve el \_ \_ destino incorrecto<br/>                 | No se pudo realizar el movimiento del componente porque la aplicación de destino ya no existe.<br/>                                                                                                                       |
| movimiento de \_ \_ comp. \_ de COMAdmin \_<br/>                    | No se ha permitido el traslado del componente porque la aplicación de origen o de destino es una aplicación del sistema o está bloqueada actualmente contra cambios.<br/>                                                |
| COMAdmin \_ E \_ COMPFILE \_ BADTLB<br/>                      | No se pudo cargar la biblioteca de tipos.<br/>                                                                                                                                                                 |
| COMAdmin \_ E \_ COMPFILE \_ CLASSNOTAVAIL<br/>               | El archivo DLL no admite los componentes enumerados en la biblioteca de tipos.<br/>                                                                                                                                   |
| COMAdmin \_ E \_ COMPFILE \_ DOESNOTEXIST<br/>                | Este archivo no existe.<br/>                                                                                                                                                                             |
| COMAdmin \_ E \_ COMPFILE \_ GETCLASSOBJ<br/>                 | Error del método [**getclassobject (**](/windows/desktop/api/objidl/nf-objidl-iclassactivator-getclassobject) en el archivo dll.<br/>                                                                                                                |
| COMAdmin \_ E \_ COMPFILE \_ LOADDLLFAIL<br/>                 | No se pudo cargar la DLL.<br/>                                                                                                                                                                          |
| COMAdmin \_ E \_ COMPFILE \_ noregistrar<br/>                 | El registrador de componentes al que se hace referencia en este archivo no está disponible.<br/>                                                                                                                                     |
| COMAdmin \_ E \_ COMPFILE \_ NOTINSTALLABLE<br/>              | El archivo no contiene componentes o información de componentes.<br/>                                                                                                                                        |
| COMAdmin \_ E \_ COREQCOMPINSTALLED<br/>                    | Ya hay instalado un componente en el mismo archivo DLL.<br/>                                                                                                                                                     |
| COMAdmin \_ E \_ DLLLOADFAILED<br/>                         | No se pudo cargar la DLL.<br/>                                                                                                                                                                          |
| COMAdmin \_ E \_ DLLREGISTERSERVER<br/>                     | Se produjo un error en la función [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) al instalar el componente.<br/>                                                                                                  |
| COMAdmin \_ E \_ EVENTCLASS \_ peralte \_ es \_ suscriptor<br/>      | Una clase de eventos no se puede configurar como un componente de suscriptor. Cuando se realiza un intento de crear una suscripción con una clase de eventos como suscriptor, se devuelve este error.<br/>                          |
| COMAdmin \_ E \_ INVALIDUSERIDS<br/>                        | Uno o varios usuarios del archivo de aplicación no son válidos.<br/>                                                                                                                                              |
| COMAdmin \_ E \_ KEYMISSING<br/>                            | No se encontró el objeto en el catálogo.<br/>                                                                                                                                                              |
| PROXY de aplicación de COMAdmin \_ E \_ lib \_ \_ \_ incompatible<br/>         | Las aplicaciones de biblioteca y los proxies de aplicación no son compatibles. Este error se devuelve cuando se intenta exportar un proxy de aplicación y la propiedad de activación de la aplicación es una biblioteca. <br/> |
| COMAdmin \_ E \_ NOREGISTRYCLSID<br/>                       | Falta el CLSID del componente o está dañado.<br/>                                                                                                                                                          |
| COMAdmin \_ E \_ NOSERVERSHARE<br/>                         | No hay ningún recurso compartido de archivos de servidor disponible.<br/>                                                                                                                                                                    |
| COMAdmin \_ E \_ NOTCHANGEABLE<br/>                         | Se han deshabilitado los cambios realizados en este objeto y sus subobjetos.<br/>                                                                                                                                        |
| COMAdmin \_ E \_ NOTDELETEABLE<br/>                         | La función de eliminación se ha deshabilitado para este objeto.<br/>                                                                                                                                                |
| COMAdmin \_ E \_ NOTINREGISTRY<br/>                         | No se encontró el objeto en el registro.<br/>                                                                                                                                                                     |
| COMAdmin \_ & \_ nousuario<br/>                                | Uno o más usuarios no son válidos.<br/>                                                                                                                                                                      |
| el objeto COMAdmin \_ E no \_ \_ \_ \_ existe<br/>              | No se encuentra uno de los objetos especificados.<br/>                                                                                                                                                         |
| falta el \_ \_ \_ elemento primario del \_ objeto COMAdmin E<br/>               | Uno de los objetos que se van a insertar o actualizar no pertenece a una colección primaria válida.<br/>                                                                                                            |
| COMAdmin \_ E \_ OBJECTERRORS<br/>                          | Se produjeron errores al obtener acceso a uno o más objetos. Para obtener más información, consulte la colección [**errorInfo**](errorinfo.md) .<br/>                                                                               |
| COMAdmin \_ E \_ OBJECTEXISTS<br/>                          | El objeto que está intentando agregar o cambiar de nombre ya existe.<br/>                                                                                                                                        |
| COMAdmin \_ E \_ OBJECTINVALID<br/>                         | Faltan una o varias propiedades del objeto o no son válidas.<br/>                                                                                                                                        |
| COMAdmin \_ E \_ OBJECTNOTPOOLABLE<br/>                     | Este objeto no se puede agrupar.<br/>                                                                                                                                                                      |
| COMAdmin \_ E \_ PROPERTYSAVEFAILED<br/>                    | Uno o varios valores de propiedad no son válidos o están en conflicto entre sí.<br/>                                                                                                                      |
| desbordamiento de la propiedad COMAdmin \_ E \_ \_<br/>                    | El valor de la propiedad es demasiado grande.<br/>                                                                                                                                                                      |
| COMAdmin \_ E \_ REGFILE \_ dañado<br/>                      | El archivo de registro está dañado.<br/>                                                                                                                                                                     |
| COMAdmin \_ E \_ REGISTERTLB<br/>                           | El sistema no pudo registrar la biblioteca de tipos.<br/>                                                                                                                                                   |
| COMAdmin \_ E \_ REGISTRARFAILED<br/>                       | Se produjeron errores en el registrador de componentes.<br/>                                                                                                                                                     |
| COMAdmin \_ E \_ REMOTEINTERFACE<br/>                       | Falta o se ha cambiado la información de la interfaz.<br/>                                                                                                                                                   |
| COMAdmin \_ E \_ requiere \_ una \_ plataforma diferente<br/>         | Esta operación no está habilitada en esta plataforma.<br/>                                                                                                                                                       |
| el rol COMAdmin \_ E no \_ \_ \_ \_ existe<br/>                | Un rol asignado a un componente, interfaz o método no existe en la aplicación.<br/>                                                                                                               |
| COMAdmin \_ E \_ ROLEEXISTS<br/>                            | El rol ya existe.<br/>                                                                                                                                                                              |
| COMAdmin \_ E \_ SERVICENOTINSTALLED<br/>                   | El servicio no está instalado.<br/>                                                                                                                                                                         |
| sesión de COMAdmin \_ E \_<br/>                               | No se admite la versión del catálogo del servidor.<br/>                                                                                                                                                          |
| COMAdmin \_ S \_ SOMEALREADYPAUSED<br/>                     | Uno o varios de los procesos de aplicación especificados ya estaban en pausa.<br/>                                                                                                                               |
| COMAdmin \_ S \_ SOMEALREADYRUNNING<br/>                    | Uno o varios de los procesos de aplicación especificados ya estaban en ejecución.<br/>                                                                                                                              |
| COMAdmin \_ E \_ iniciar la \_ aplicación \_ necesita \_ componentes<br/>         | Para iniciar la aplicación, debe tener componentes en una aplicación.<br/>                                                                                                                                 |
| COMAdmin \_ E \_ SVCAPP \_ no \_ agrupables \_ o \_ reciclables<br/> | Las aplicaciones COM+ que se ejecutan como un servicio NT no se pueden marcar como agrupadas ni recicladas.<br/>                                                                                                               |
| COMAdmin \_ E \_ SYSTEMAPP<br/>                             | Esta operación no se puede realizar en la aplicación del sistema.<br/>                                                                                                                                         |
| COMAdmin \_ E \_ usuario \_ en \_ conjunto<br/>                         | Uno o más usuarios ya están asignados a un conjunto de particiones local.<br/>                                                                                                                                      |
| COMAdmin \_ E \_ USERPASSWDNOTVALID<br/>                    | La identidad o la contraseña establecida en la aplicación no es válida.<br/>                                                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aislamiento de errores y Directiva FailFast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Buscar el origen de un error](finding-the-source-of-an-error.md)
</dt> <dt>

[Cómo modifica COM+ los valores devueltos](how-com--modifies-return-values.md)
</dt> <dt>

[Estrategias para controlar errores en COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Solución de problemas](troubleshooting-the-com--crm.md)
</dt> </dl>

 

