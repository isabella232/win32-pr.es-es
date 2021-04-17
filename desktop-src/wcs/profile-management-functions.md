---
title: Funciones de administración de perfiles
description: Funciones de administración de perfiles
ms.assetid: 185863b7-0b74-4c65-97c3-3c60b86d37fd
keywords:
- Sistema de color de Windows (WCS), funciones
- WCS (sistema de colores de Windows), funciones
- Administración del color de imagen, funciones
- Administración del color, funciones
- colores, funciones
- Referencia WCS, funciones
- referencia de las funciones WCS,
- Sistema de color de Windows (WCS), perfiles
- WCS (sistema de colores de Windows), perfiles
- Administración del color de imagen, perfiles
- Administración del color, perfiles
- colores, perfiles
- Referencia WCS, perfiles
- referencia de WCS, perfiles
- Administración de perfiles
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0e80e300532b20148eef6d9dc362438b6714a3
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "105721172"
---
# <a name="profile-management-functions"></a>Funciones de administración de perfiles

## <a name="profile-management-functions"></a>Funciones de administración de perfiles

Las siguientes funciones de API son útiles en la administración de perfiles.



| Función                                                                               | Descripción                                                                                                                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssociateColorProfileWithDeviceW**](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | Asocia un perfil de color especificado a un dispositivo especificado.                                                              |
| [**CreateProfileFromLogColorSpaceW**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew) | Convierte un espacio de [colores](c.md) lógico en un [Perfil de dispositivo](d.md). |
| [**DisassociateColorProfileFromDeviceW**](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | Desasocia un perfil de color especificado con un dispositivo especificado en un equipo especificado. |
| [**EnumColorProfilesW**](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | Enumera todos los perfiles que cumplen los criterios de enumeración especificados. |
| [**GetColorDirectoryW**](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | Recupera la ruta de acceso del directorio de COLOR de Windows en un equipo especificado. |
| [**GetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | Obtiene la rampa gamma de los paneles de presentación de colores directos.                                                                                                |
| [**GetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | Recupera el perfil de color registrado para el espacio de [colores](c.md)estándar especificado. |
| [**InstallColorProfileW**](/windows/win32/api/icm/nf-icm-installcolorprofilew) | Instala un perfil determinado para su uso en un equipo especificado. El perfil también se copia en el directorio de COLOR. |
| [**RegisterCMMW**](/windows/win32/api/icm/nf-icm-registercmmw) | Asocia un valor de identificación especificado a la biblioteca de vínculos dinámicos del módulo de administración de color (CMM DLL) especificada. Cuando este identificador aparece en un perfil de color, Windows puede localizar la CMM correspondiente para crear una transformación. |
| [**SetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | Establece la rampa gamma en los paneles de presentación de color directo.                                                                                                  |
| [**SetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | Registra un perfil especificado para un [espacio de colores](c.md)estándar determinado. El perfil se puede consultar mediante [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew). |
| [**UninstallColorProfileW**](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | Quita un perfil de color especificado de un equipo especificado. Los archivos asociados se eliminan opcionalmente del sistema. |
| [**UnregisterCMMW**](/windows/win32/api/icm/nf-icm-unregistercmmw) | Anula la Asociación de un valor de identificador especificado de una biblioteca de vínculos dinámicos (DLL CMM) determinada del módulo de administración del color. |
| [**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | Asocia un perfil de color WCS especificado a un dispositivo especificado.                                                                                    |
| [**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | Convierte un perfil WCS en un perfil ICC.                                                                                                          |
| [**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | Desasocia un perfil de color WCS especificado con un dispositivo especificado en un equipo especificado.                                                         |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | Enumera todos los perfiles de color que cumplen los criterios de enumeración en el ámbito de administración de perfiles especificado.                                       |
| [**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)                           | Devuelve el tamaño, en bytes, del búfer requerido por la función [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) para enumerar los perfiles de color. |
| [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)                         | Recupera el perfil de color predeterminado para un dispositivo o el valor predeterminado independiente del dispositivo si no se especifica el dispositivo.                                  |
| [**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | Devuelve el tamaño, en bytes, del nombre de Perfil de color predeterminado para un dispositivo, incluido el terminador **null** .                                       |
| [**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Recupera el intento de representación predeterminado en el ámbito de administración de perfiles especificado.                                                                    |
| [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Determina si el usuario ha elegido utilizar una lista de asociaciones de perfil por usuario para el dispositivo especificado.                                          |
| [**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | Crea un identificador para un perfil de color especificado.                                                                                                       |
| [**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | Establece el nombre de Perfil de color predeterminado del tipo de perfil especificado en el ámbito de administración de perfiles especificado.                                         |
| [**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | Establece la intención de representación predeterminada en el ámbito de administración de perfiles especificado.                                                                         |
| [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | Permite al usuario especificar si se va a usar una lista de asociaciones de perfil por usuario para el dispositivo especificado.                                              |



 

## <a name="profile-consumption-functions"></a>Funciones de consumo de perfiles

Las API de consumo de perfiles son las API de ICM2 que usan perfiles XML de ICC o WCS, identificadores de perfil o representación del Intent como parámetros, y un conjunto de nuevas API para la compatibilidad del perfil WCS con el código de administración del color de la aplicación.

 

## <a name="profiles-and-profile-management-functions"></a>Perfiles y funciones de administración de perfiles

El flujo de trabajo de administración de perfiles se basa en las API de ICM2 existentes que se han ampliado para proporcionar funcionalidad adicional para revisar el código de la aplicación.

Los perfiles contienen información que utilizan los algoritmos de procesamiento de color para traducir el color entre diferentes espacios de color. La administración de perfiles proporciona una manera de consultar y especificar qué perfiles se usan en diferentes fases por el modelo de procesamiento de color para administrar la salida de color de varios dispositivos periféricos con distintas características de color.

La administración de perfiles proporciona el siguiente conjunto de funcionalidades:

 

1. Instalar perfiles de color para su uso en el sistema.

 

2. Asociación de uno o varios perfiles de color instalados con un dispositivo determinado.

 

3. Elegir un perfil de color predeterminado de un tipo determinado entre los perfiles disponibles para su uso en una fase determinada de procesamiento de color. Esto podría ser para un dispositivo entre los perfiles asociados a él o entre los perfiles instalados en el sistema y no específicos del dispositivo.

 

4. Enumerar los perfiles de color que cumplen determinados criterios entre los perfiles instalados en el sistema.

Las extensiones de nombre de archivo del perfil WCS son ". CDMP" para DMPs, ". Camp" para los nombres y ". GMMP" para GMMPs.

 

**Administración de perfiles por usuario y habilitación de la ejecución en el contexto LUA**

El objetivo del diseño descrito en el documento actual es el siguiente:

 

1. La implementación de ICM2 heredada no proporciona compatibilidad con la administración de perfiles por usuario. Los distintos usuarios no pueden tener su propia configuración de perfil. En vista, la infraestructura de administración de perfiles WCS permite a los usuarios configurar opciones de perfil individuales para la mayoría de las funcionalidades.

 

2. Todas las API de administración de perfiles de ICM2 heredadas modifican la configuración de todo el sistema y requieren privilegios administrativos. En Windows Vista, todos los usuarios se ejecutan en la configuración de cuenta de usuario con privilegios mínimos (LUA) la mayoría de las veces, y los administradores pueden elevar los privilegios de forma selectiva para ejecutar aplicaciones que modifican la configuración de todo el sistema. En la administración de perfiles WCS, todas las configuraciones de perfil por usuario se pueden configurar en el contexto LUA. Las aplicaciones de administración de perfiles se pueden ejecutar como configuraciones de LUA, lo que aumenta el ámbito de uso y garantiza que la seguridad del sistema no se ve comprometida.

La administración de perfiles en vista proporciona las siguientes mejoras en la infraestructura de ICM2 heredada:

 

1. Habilita la Asociación de perfiles con los dispositivos, la configuración de perfil predeterminada y la enumeración de perfiles en el ámbito por usuario y todo el sistema.

 

2. La instalación de un perfil permanece en todo el sistema y requiere privilegios de administrador. Esto es coherente con la instalación del perfil durante la instalación del dispositivo porque la instalación del dispositivo es todo el sistema y requiere privilegios administrativos.

 

El hecho de que los dispositivos se puedan instalar desde el contexto LUA es específico de lo que se admite para esa clase de dispositivo. Por ejemplo, en vista, es posible realizar la instalación de la impresora desde el contexto de LUA si el usuario tiene derechos para copiar archivos en el almacén de controladores mediante un administrador de dominio mediante directivas de almacén de controladores. La infraestructura de administración de perfiles de color no tiene que hacer nada especial en este sentido, ya que la instalación se produce en el contexto del administrador de trabajos de impresión.

 

3. La modificación de la configuración de perfil en el ámbito por usuario se puede realizar en el contexto LUA; las modificaciones en todo el sistema requieren privilegios administrativos. Las operaciones de administración de perfiles que requieren la lectura de la información de configuración se pueden realizar en el contexto LUA para configuraciones por usuario y para todo el sistema.

Ámbito de administración de perfiles indica el ámbito de las operaciones realizadas; por usuario o en todo el sistema.

Para cada operación, se indica si se puede hacer desde el contexto LUA. Si una operación no se puede realizar en el contexto LUA, la API de administración de perfiles correspondiente devuelve un error con acceso denegado. Las aplicaciones que usan la API, como el panel de control de administración del color, pueden permitir que el usuario eleve el contexto administrativo (mediante OTS o la interfaz de usuario de consentimiento) y, después, llama a la API desde el contexto elevado para que la operación se realice correctamente.



Operación

Ámbito de administración de perfiles

Condición previa

Condición posterior

Ejecutable en contexto LUA

$ {ROWSPAN2} $Install perfil $ {REMOVE} $  

En todo el sistema

Perfil copiado, instalado en el sistema y disponible para su uso. El perfil es Enumerable en el ámbito de todo el sistema y del usuario actual para todos los usuarios.

Durante la instalación del controlador de dispositivo, regido por las directivas de instalación del controlador. De lo contrario, no.

Usuario actual

No compatible

$ {ROWSPAN2} $Uninstall perfil $ {REMOVE} $  

En todo el sistema

El perfil está instalado en el sistema

Perfil desinstalado del sistema y, opcionalmente, eliminado del almacén de perfiles. El perfil ya no está disponible para su uso y no se puede enumerar en ningún ámbito.

No

Usuario actual

No compatible

$ {ROWSPAN2} $Associate perfil con el dispositivo $ {REMOVE} $  

En todo el sistema

El perfil está instalado y es de tipo ICC o CDMP

El perfil está disponible para su uso con el dispositivo por parte de todos los usuarios. Es Enumerable, en el ámbito de todo el sistema y también en el ámbito de usuario actual para todos los usuarios, como está asociado con el dispositivo.

No

Usuario actual

El perfil está instalado. No importa si el perfil ya está asociado al dispositivo en el ámbito de todo el sistema y es de tipo ICC o CDMP.

El perfil está disponible para su uso con el dispositivo por el usuario actual. Solo se Enumerable en el ámbito del usuario actual (a menos que también haya una asociación de todo el sistema) como está asociado con el dispositivo.

Sí

$ {ROWSPAN2} $Disassociate perfil del dispositivo $ {REMOVE} $  

En todo el sistema

El perfil está asociado con el dispositivo en el ámbito de todo el sistema y es de tipo ICC o CDMP

El perfil ya no está disponible para su uso (excepto para los usuarios que tienen esta asociación en su ámbito de usuario actual). No es Enumerable en el ámbito de todo el sistema. Sin embargo, podría ser Enumerable en el ámbito del usuario actual para un usuario que tenga esta asociación en su ámbito.

No

Usuario actual

El perfil está asociado con el dispositivo en el ámbito del usuario actual (independientemente de si está asociado en el ámbito de todo el sistema) y es de tipo ICC o CDMP.

El perfil ya no está disponible para su uso, o Enumerable como asociado al dispositivo, por parte del usuario actual (a menos que también esté asociado en el ámbito de todo el sistema al dispositivo).

Sí

$ {ROWSPAN2} $Set perfil para un tipo (DMP o ICC) como valor predeterminado para un dispositivo $ {REMOVE} $  

En todo el sistema

El perfil es de tipo ICC o CDMP

De forma predeterminada, el perfil se usa para el tipo determinado con el dispositivo, para todos los usuarios excepto para aquellos que han invalidado esta configuración en su ámbito de usuario actual. (El perfil se instala y se asocia al sistema del dispositivo de ancho, si aún no es el caso).

No

Usuario actual

El perfil es de tipo ICC o CDMP

De forma predeterminada, el perfil se usa para el tipo determinado con el dispositivo en caso de usuario actual, con independencia del valor predeterminado para todo el sistema. (El perfil se instala y se asocia al dispositivo para el usuario actual, si aún no es el caso).

Sí, si el perfil ya está instalado

$ {ROWSPAN2} $Set perfil para un tipo (ICC, DMP, CAMP, GMMP) y combinación de subtipo como valor predeterminado global $ {REMOVE} $  

En todo el sistema

Solo los perfiles ICC y CDMP se pueden asociar a los dispositivos.

El perfil se utiliza de forma predeterminada para el tipo determinado. Los usuarios pueden invalidar esta configuración en el ámbito del usuario actual. (El perfil está instalado, si aún no es el caso).

No

Usuario actual

Solo los perfiles ICC y CDMP se pueden asociar a los dispositivos.

El perfil se utiliza de forma predeterminada para el tipo concreto para el usuario actual. (El perfil está instalado, si aún no es el caso).

Sí, si el perfil ya está instalado.

$ {ROWSPAN2} $Erase la invalidación del usuario actual para una configuración de perfil predeterminada determinada, de modo que el valor predeterminado del sistema se usa siempre (como reserva), incluso para el ámbito del usuario actual. $ {REMOVE} $  

En todo el sistema

No aplicable

Usuario actual

Incluso en el caso de las consultas de usuario actual en la configuración de perfil predeterminada, se devuelve la configuración de todo el sistema para su uso.

Sí

$ {ROWSPAN2} $Enumerate perfiles instalados que satisfacen criterios determinados (como clase de dispositivo, clase de perfil, etc.) $ {REMOVE} $  

En todo el sistema

Solo los perfiles ICC y CDMP se pueden asociar y enumerar para dispositivos.

Los perfiles que se instalan y cumplen los criterios especificados en el ámbito de todo el sistema se enumeran.

Sí

Usuario actual

Solo los perfiles ICC y CDMP se pueden asociar con dispositivos y, por tanto, se enumeran para dispositivos.

Los perfiles que se instalan y cumplen los criterios especificados en el ámbito de todo el sistema se enumeran.

Sí

$ {ROWSPAN2} $Enumerate perfiles asociados a un dispositivo determinado que satisfacen determinados criterios, como la clase de dispositivo y la clase de perfil $ {REMOVE} $  

En todo el sistema

Solo los perfiles ICC y CDMP se pueden asociar y enumerar para dispositivos.

Los perfiles que están asociados al dispositivo en el ámbito de todo el sistema y cumplen los criterios especificados en el ámbito de todo el sistema se enumeran.

Sí

Usuario actual

Solo los perfiles ICC y CDMP se pueden asociar y enumerar para dispositivos.

Los perfiles que están disponibles como asociados al dispositivo en el ámbito del usuario actual, que incluye las asociaciones de todo el sistema y cumplen los criterios especificados en el ámbito del usuario actual, se enumeran.

Sí



 

Los tipos de Perfil de color válidos los proporciona la enumeración COLORPROFILETYPE.

Los subtipos de Perfil de color válidos los proporciona la enumeración COLORPROFILESUBTYPE.

En la tabla siguiente se muestran las combinaciones válidas de tipo de perfil/subtipo.



COLORPROFILETYPE 

COLORPROFILESUBTYPE válido

Notas

Valor predeterminado del dispositivo

Valor predeterminado global

Uso previsto

Uso previsto

ICC de CPT \_

CPST \_ ninguno

Obtiene o establece el perfil ICC predeterminado asociado a un dispositivo.

CPST \_ RGBWorkingSpace o CPST \_ CustomWorkingSpace

Obtiene o establece el perfil de ICC como perfil de espacio de trabajo global RGB o personalizado. Vea la Nota.

COLORPROFILETYPE CPT \_ ICC y CPT \_ DMP son mutuamente excluyentes. El perfil de color predeterminado que establezca para un espacio de trabajo determinado (RGB o personalizado) puede ser un perfil ICC o un perfil DMP, pero no ambos.

DMP de CPT \_

CPST \_ ninguno

Obtiene o establece el perfil de DMP predeterminado asociado a un dispositivo.

CPST \_ RGBWorkingSpace o CPST \_ CustomWorkingSpace

Obtiene o establece el perfil de DMP como perfil de espacio de trabajo global RGB o personalizado. Vea la Nota.

COLORPROFILETYPE CPT \_ ICC y CPT \_ DMP son mutuamente excluyentes. El perfil de color predeterminado que establezca para un espacio de trabajo determinado (RGB o personalizado) puede ser un perfil ICC o un perfil DMP, pero no ambos.



 

> [!Note]  
> Cuando se llama a WcsSetDefaultColorProfile para establecer un perfil de DMP como perfil predeterminado para el espacio de trabajo de RGB o un espacio de trabajo personalizado, solo es válido un perfil DMP de tipo RGBVirtualDevice, LCD o CRT.
>
>  
>
> Cuando se llama a WcsSetDefaultColorProfile para establecer un perfil de ICC como perfil predeterminado para el espacio de trabajo RGB o un espacio de trabajo personalizado, solo un perfil de ICC cuya clase es "Space" o "DISP" y cuyo espacio de colores es "RGB" es válido.

 

La arquitectura está diseñada según los requisitos de las operaciones que se mencionan en las enumeraciones y las tablas anteriores.

### <a name="profile-management-public-api-layer"></a>Nivel de API pública de administración de perfiles

Dado que el ámbito de administración de perfiles no es compatible con las API de ICM2 heredadas, se requiere un nuevo conjunto de API de administración de perfiles WCS que defina el ámbito de administración de perfiles como usuario amplio o del sistema actual. ? Las API de ICM2 heredadas siguen siendo compatibles con la compatibilidad con versiones anteriores y funcionan en el ámbito de administración de perfiles que está implícito para la llamada. ¿o ICM2 API que funcionan en el ámbito del usuario actual? Esto es para las operaciones que son compatibles con el ámbito de usuario actual y del sistema en la administración de perfiles WCS. Las API de ICM2 heredadas llaman a las nuevas API WCS con el ámbito de administración de perfiles como usuario actual. Esto tiene sentido desde la perspectiva del usuario, ya que permite la configuración por usuario de las aplicaciones heredadas y también la ejecución de la mayoría de las operaciones en el contexto LUA. ¿o ICM2 API que funcionan en el ámbito de todo el sistema? Esto es para las operaciones (instalar perfiles y desinstalar perfiles) que solo admiten el ámbito de todo el sistema. No se crean nuevas API de administración de perfiles WCS y se pueden modificar las API existentes.

Las implementaciones subyacentes de las operaciones de administración de perfiles funcionan en las entidades de datos de configuración siguientes para crear el contexto de los algoritmos de procesamiento de colores con el fin de proporcionar funcionalidades de administración del color. Son valores específicos del dispositivo o globales (independientes del dispositivo). o datos de configuración específicos del dispositivo:? Lista de perfiles asociados a un dispositivo determinado. ? Perfil predeterminado para distintos tipos de perfiles asociados con un dispositivo. ? Modo de coincidencia de perfiles que se usa para la enumeración. o datos de configuración global:? Lista de perfiles instalados en el sistema. ? Perfil predeterminado global para distintos tipos de perfiles. ? Las implementaciones subyacentes del almacenamiento de datos de configuración se aplican en el ámbito de almacenamiento para los datos de configuración (ya sean independientes del dispositivo o específicos del dispositivo), que puede ser todo el sistema o el usuario actual. Esto es diferente del ámbito de administración de perfiles. Una operación con el ámbito de administración de perfiles de usuario actual puede producir una lectura desde un ámbito de almacenamiento de todo el sistema si la configuración de usuario actual para esa operación no está presente. ? El nivel de API ICM2/WCS llama a esta capa de almacenamiento para obtener y establecer datos con el ámbito de almacenamiento adecuado. La capa de almacenamiento es transparente para el ámbito de administración de perfiles. La lógica para combinar datos de ámbitos de almacenamiento de usuario actual y de todo el sistema para crear o actualizar una configuración de acuerdo con el ámbito de administración de perfiles especificado por el llamador de la API. Esta lógica está presente en el nivel de API ICM2/WCS.

### <a name="device-specific-storage-layer"></a>Capa de almacenamiento específica del dispositivo

El almacenamiento de diferentes clases de dispositivos como imprimir, capturar o mostrar puede ser diferente entre sí. Por ejemplo, los datos de configuración de un dispositivo de impresión deben almacenarse mediante las API de impresión estándar, como SetPrinterDataEx y GetPrinterDataEx, para permitir la copia de perfiles y la configuración que se va a transferir a un equipo cliente durante la conexión de punto e impresión. ? Esta capa exporta la funcionalidad para abrir el almacén, obtener datos, establecer datos y cerrar el almacén mediante interfaces predefinidas comunes para que la capa de almacenamiento de la configuración de la administración de perfiles pueda llamarlos a la vez que se almacenan los datos para ese dispositivo.

El diagrama siguiente muestra esta arquitectura.



Nivel de API pública de administración de perfiles

$ {ROWSPAN2} $Legacy API de ICM2 para las operaciones que solo admiten el ámbito de administración de perfiles de todo el sistema en vista (instalar, desinstalar y obtener directorio de color). Llaman a la capa de almacenamiento de configuración con el ámbito de almacenamiento adecuado. $ {REMOVE} $  

Legacy ICM2 API para las operaciones que admiten el ámbito de administración de perfiles de usuario actual y todo el sistema en vista (todas las operaciones distintas de install, uninstall y Get color Directory). Funcionan implícitamente en el ámbito del usuario actual y llaman a la nueva API WCS con el ámbito de administración de perfiles como usuario actual.

Nueva API WCS con compatibilidad con el ámbito de administración de perfiles de usuario actual y en todo el sistema. Llaman a la capa de almacenamiento de configuración con el ámbito de almacenamiento adecuado.



 



Capa de almacenamiento de configuración de administración de perfiles

Rutinas de configuración global independientes del dispositivo

Rutinas de configuración específicas del dispositivo

$ {ROWSPAN3} $Profile la instalación y la administración de configuración de perfil predeterminada independiente del dispositivo, que se admite en el ámbito de almacenamiento de usuario actual y en todo el sistema. $ {REMOVE} $  

Asociación de dispositivos y administración de configuración de perfil predeterminada específica del dispositivo, que se admite en el ámbito de almacenamiento de usuario actual y en todo el sistema.

Device-Specific capa de almacenamiento

Imprimir almacenamiento específico

Mostrar almacenamiento específico

Capturar almacenamiento específico



 

Las API de ICM2 heredadas para las operaciones que solo admiten el ámbito de administración de perfiles de todo el sistema en vista no tienen ningún cambio de comportamiento. Las operaciones de instalación y desinstalación se encuentran en esta categoría.

Las API de ICM2 heredadas para las operaciones que admiten el ámbito de administración de perfiles de usuario actual y todo el sistema tienen su comportamiento cambiado para consultar y configurar las opciones de usuario actual. Todas las operaciones que no sean instalar y desinstalar se encuentran en esta categoría.

 

 




