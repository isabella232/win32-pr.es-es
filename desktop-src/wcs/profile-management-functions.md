---
title: Funciones de administración de perfiles
description: Funciones de administración de perfiles
ms.assetid: 185863b7-0b74-4c65-97c3-3c60b86d37fd
keywords:
- Windows Sistema de colores (WCS), funciones
- WCS (Windows Color System),functions
- administración de colores de imagen, funciones
- administración de colores, funciones
- colors,functions
- Referencia de WCS, funciones
- referencia de WCS,functions
- Windows Sistema de colores (WCS),perfiles
- WCS (Windows Color System),profiles
- administración de colores de imagen, perfiles
- administración de colores, perfiles
- colors,profiles
- Referencia de WCS, perfiles
- referencia de WCS,profiles
- administración de perfiles
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f047c2dee199800fad976dd7b959fbbb54d585fd252fb8b5390c3223415db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587775"
---
# <a name="profile-management-functions"></a>Funciones de administración de perfiles

## <a name="profile-management-functions"></a>Funciones de administración de perfiles

Las siguientes funciones de API son útiles en la administración de perfiles.



| Función                                                                               | Descripción                                                                                                                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssociateColorProfileWithDeviceW**](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | Asocia un perfil de color especificado a un dispositivo especificado.                                                              |
| [**CreateProfileFromLogColorSpaceW**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew) | Convierte un espacio [de color lógico en](c.md) un perfil de [dispositivo](d.md). |
| [**DisassociateColorProfileFromDeviceW**](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | Desasocia un perfil de color especificado con un dispositivo especificado en un equipo especificado. |
| [**EnumColorProfilesW**](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | Enumera todos los perfiles que cumplen los criterios de enumeración especificados. |
| [**GetColorDirectoryW**](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | Recupera la ruta de acceso del Windows COLOR en un equipo especificado. |
| [**GetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | Obtiene la rampa gamma de los paneles de visualización de color directo.                                                                                                |
| [**GetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | Recupera el perfil de color registrado para el espacio de [colores estándar especificado.](c.md) |
| [**InstallColorProfileW**](/windows/win32/api/icm/nf-icm-installcolorprofilew) | Instala un perfil determinado para su uso en un equipo especificado. El perfil también se copia en el directorio COLOR. |
| [**RegisterCMMW**](/windows/win32/api/icm/nf-icm-registercmmw) | Asocia un valor de identificación especificado a la biblioteca de vínculos dinámicos (DLL de CMM) del módulo de administración de colores especificado. Cuando este identificador aparece en un perfil de color, Windows buscar la CMM correspondiente para crear una transformación. |
| [**SetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | Establece la rampa gamma en los paneles de presentación de color directo.                                                                                                  |
| [**SetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | Registra un perfil especificado para un espacio [de color estándar determinado.](c.md) El perfil se puede consultar mediante [GetStandardColorSpaceProfileW.](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) |
| [**UninstallColorProfileW**](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | Quita un perfil de color especificado de un equipo especificado. Opcionalmente, los archivos asociados se eliminan del sistema. |
| [**Anulación del registro DECMMW**](/windows/win32/api/icm/nf-icm-unregistercmmw) | Desasocia un valor de identificador especificado de una biblioteca de vínculos dinámicos (DLL de CMM) de un módulo de administración de colores determinado. |
| [**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | Asocia un perfil de color WCS especificado a un dispositivo especificado.                                                                                    |
| [**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | Convierte un perfil WCS en un perfil DE CIA.                                                                                                          |
| [**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | Desasocia un perfil de color WCS especificado con un dispositivo especificado en un equipo especificado.                                                         |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | Enumera todos los perfiles de color que cumplen los criterios de enumeración en el ámbito de administración de perfiles especificado.                                       |
| [**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)                           | Devuelve el tamaño, en bytes, del búfer requerido por la función [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) para enumerar los perfiles de color. |
| [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)                         | Recupera el perfil de color predeterminado para un dispositivo o el valor predeterminado independiente del dispositivo si no se especifica el dispositivo.                                  |
| [**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | Devuelve el tamaño, en bytes, del nombre del perfil de color predeterminado para un dispositivo, incluido el terminador **NULL.**                                       |
| [**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Recupera la intención de representación predeterminada en el ámbito de administración de perfiles especificado.                                                                    |
| [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Determina si el usuario ha elegido usar una lista de asociaciones de perfil por usuario para el dispositivo especificado.                                          |
| [**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | Crea un identificador para un perfil de color especificado.                                                                                                       |
| [**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | Establece el nombre del perfil de color predeterminado del tipo de perfil especificado en el ámbito de administración de perfiles especificado.                                         |
| [**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | Establece la intención de representación predeterminada en el ámbito de administración de perfiles especificado.                                                                         |
| [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | Permite al usuario especificar si se debe usar una lista de asociaciones de perfil por usuario para el dispositivo especificado.                                              |



 

## <a name="profile-consumption-functions"></a>Funciones de consumo de perfiles

Las API de consumo de perfiles son aquellas API de ICM2 que toman perfiles XML DE WCS o DE ÍNDICE, identificadores de perfil o intenciones de representación como parámetros, y un conjunto de nuevas API para la compatibilidad de perfiles WCS con el código de administración del color de la aplicación.

 

## <a name="profiles-and-profile-management-functions"></a>Perfiles y funciones de administración de perfiles

El flujo de trabajo de administración de perfiles se basa en las API ICM2 existentes que se aumentan para proporcionar funcionalidad adicional para revisar el código de la aplicación.

Los perfiles contienen información que usan los algoritmos de procesamiento de colores para traducir el color entre distintos espacios de color. La administración de perfiles proporciona una manera de consultar y especificar qué perfiles se usan en diferentes fases por el modelo de procesamiento de colores para administrar la salida de color de varios dispositivos periféricos con diversas características de color.

La administración de perfiles proporciona el siguiente conjunto de funcionalidades:

 

1. Instalación de perfiles de color para su uso en el sistema.

 

2. Asociación de uno o varios perfiles de color instalados con cualquier dispositivo determinado.

 

3. Elegir un perfil de color predeterminado de un tipo determinado entre los perfiles disponibles para su uso en una fase determinada del procesamiento de colores. Esto podría ser para un dispositivo entre los perfiles asociados a él o entre los perfiles instalados en el sistema y no específicos del dispositivo.

 

4. Enumeración de perfiles de color que cumplen determinados criterios entre los perfiles instalados en el sistema.

Las extensiones de nombre de archivo del perfil de WCS son ".cdmp" para DMP, ".camp" para LOS MMP y ".gmmp" para GMMP.

 

**Administración de perfiles por usuario y habilitación de la ejecución en el contexto de LUA**

El objetivo del diseño descrito en el documento actual es el siguiente:

 

1. La implementación heredada de ICM2 no proporciona compatibilidad con la administración de perfiles por usuario. Los distintos usuarios no pueden tener su propia configuración de perfil. En Vista, la infraestructura de administración de perfiles de WCS permite a los usuarios configurar opciones de perfil individuales para la mayoría de las funcionalidades.

 

2. Todas las API de administración de perfiles ICM2 heredadas modifican la configuración en todo el sistema y requieren privilegios administrativos. En Windows Vista, todos los usuarios se ejecutan en la configuración de cuentas de usuario con privilegios mínimos (LUA) la mayoría del tiempo y los administradores pueden elevar los privilegios de forma selectiva para ejecutar aplicaciones que modifican la configuración de todo el sistema. En la administración de perfiles de WCS, todas las configuraciones de perfil por usuario se pueden configurar en el contexto lua. Las aplicaciones de administración de perfiles se pueden ejecutar como configuración de LUA, lo que aumenta su ámbito de uso y garantiza que la seguridad del sistema no esté en peligro.

La administración de perfiles en Vista proporciona las siguientes mejoras en la infraestructura ICM2 heredada:

 

1. Permite la asociación de perfiles con dispositivos, la configuración de perfil predeterminada y la enumeración de perfiles tanto en el ámbito por usuario como en todo el sistema.

 

2. La instalación de un perfil permanece en todo el sistema y requiere privilegios de administrador. Esto es coherente con la instalación de perfiles durante la instalación del dispositivo porque la instalación de dispositivos es de todo el sistema y requiere privilegios administrativos.

 

El hecho de que los dispositivos se puedan instalar desde el contexto lua es particular de lo que se admite para esa clase de dispositivo. Por ejemplo, en Vista, es posible realizar la instalación de impresoras desde el contexto lua si un administrador de dominio ha concedido al usuario derechos para copiar archivos en el almacén de controladores mediante directivas de almacén de controladores. La infraestructura de administración de perfiles de color no necesita hacer nada especial en este sentido, ya que la instalación se produce en el contexto del administrador de trabajos de cola.

 

3. La modificación de la configuración del perfil en el ámbito por usuario se puede realizar en el contexto de LUA; Las modificaciones de todo el sistema requerían privilegios administrativos. Las operaciones de administración de perfiles que requieren leer información de configuración se pueden realizar en el contexto lua para la configuración por usuario y para todo el sistema.

El ámbito de administración de perfiles indica el ámbito de las operaciones realizadas; por usuario o en todo el sistema.

Para cada operación, se indica si se puede realizar desde el contexto lua. Si no se puede realizar una operación en el contexto de LUA, la API de administración de perfiles correspondiente devuelve un error con acceso denegado. Las aplicaciones que usan la API, como Color Management Panel de control, pueden permitir que el usuario eleve al contexto administrativo (mediante OTS o la interfaz de usuario de consentimiento) y, a continuación, llamar a la API desde el contexto con privilegios elevados para que la operación se realizará correctamente.



Operación

Ámbito de administración de perfiles

Condición previa

Condición posterior

Ejecutable en contexto lua

${ROWSPAN2}$Install profile${REMOVE}$  

Todo el sistema

Perfil copiado, instalado en el sistema y disponible para su uso. El perfil se puede enumerar en el ámbito de usuario actual y en todo el sistema para todos los usuarios.

Durante la instalación del controlador de dispositivo, regido por directivas de instalación de controladores. De lo contrario, no.

Usuario actual

No compatible

${ROWSPAN2}$Uninstall profile${REMOVE}$  

Todo el sistema

El perfil está instalado en el sistema

Perfil desinstalado del sistema y eliminado opcionalmente del almacén de perfiles. El perfil ya no está disponible para su uso y no se puede enumerar en ningún ámbito.

No

Usuario actual

No compatible

${ROWSPAN2}$Associate perfil con device${REMOVE}$  

Todo el sistema

El perfil está instalado y es de tipo ICC o CDMP.

El perfil está disponible para su uso con el dispositivo por parte de todos los usuarios. Es enumerable, en el ámbito de todo el sistema y también en el ámbito del usuario actual para todos los usuarios, como se asocia con el dispositivo.

No

Usuario actual

El perfil está instalado. No importa si el perfil ya está asociado al dispositivo en el ámbito de todo el sistema y es de tipo DHCP o CDMP.

El perfil está disponible para su uso con el dispositivo por parte del usuario actual. Solo se puede enumerar en el ámbito del usuario actual (a menos que también haya una asociación de todo el sistema) asociada al dispositivo.

Sí

${ROWSPAN2}$Disassociate perfil del dispositivo${REMOVE}$  

Todo el sistema

El perfil está asociado al dispositivo en el ámbito de todo el sistema y es de tipo DHCP o CDMP.

El perfil ya no está disponible para su uso (excepto para los usuarios que también tienen esta asociación en su ámbito de usuario actual). No se puede enumerar en el ámbito de todo el sistema. Sin embargo, podría enumerarse en el ámbito del usuario actual para un usuario que tenga esta asociación en su ámbito.

No

Usuario actual

El perfil está asociado al dispositivo en el ámbito del usuario actual (independientemente de si está asociado en el ámbito de todo el sistema) y es de tipo DHCP o CDMP.

El perfil ya no está disponible para su uso, o enumerable como asociado al dispositivo, por parte del usuario actual (a menos que también esté asociado en el ámbito del sistema al dispositivo).

Sí

${ROWSPAN2}$Set perfil para un tipo (DMP o ICC) como valor predeterminado para un dispositivo${REMOVE}$  

Todo el sistema

El perfil es de tipo ICC o CDMP

El perfil se usa de forma predeterminada, para el tipo concreto con el dispositivo, para todos los usuarios, excepto para aquellos que han invalidado esta configuración en su ámbito de usuario actual. (El perfil está instalado y asociado al sistema del dispositivo en todo el sistema, si aún no es así).

No

Usuario actual

El perfil es de tipo ICC o CDMP

El perfil se usa de forma predeterminada para el tipo determinado con el dispositivo en el caso del usuario actual, independientemente del valor predeterminado de todo el sistema para esto. (El perfil está instalado y asociado al dispositivo para el usuario actual, si aún no es así).

Sí, si el perfil ya está instalado

${ROWSPAN2}$Set perfil para un tipo (ICC, DMP,CAMP, GMMP) y una combinación de subtipo como valor predeterminado global${REMOVE}$  

Todo el sistema

Solo se pueden asociar perfiles DE ACUERDO y CDMP con dispositivos.

El perfil se usa de forma predeterminada para el tipo determinado. Los usuarios pueden invalidar esta configuración en el ámbito de usuario actual. (El perfil está instalado, si aún no es así).

No

Usuario actual

Solo se pueden asociar perfiles DE ACUERDO y CDMP con dispositivos.

El perfil se usa de forma predeterminada para el tipo concreto para el usuario actual. (El perfil está instalado, si aún no es así).

Sí, si el perfil ya está instalado.

${ROWSPAN2}$Erase la invalidación del usuario actual para una configuración de perfil predeterminada determinada, de modo que el valor predeterminado del sistema siempre se utilice (como reserva) incluso para el ámbito del usuario actual.${REMOVE}$  

Todo el sistema

No aplicable

Usuario actual

Incluso para las consultas de usuario actuales en la configuración predeterminada del perfil, se devuelve la configuración de todo el sistema para su uso.

Sí

${ROWSPAN2}$Enumerate perfiles instalados que cumplen determinados criterios (como la clase de dispositivo, la clase de perfil, etc.) ${REMOVE}$  

Todo el sistema

Solo se pueden asociar y enumerar perfiles DE CMP y CDMP para dispositivos.

Se enumeran los perfiles instalados y que cumplen los criterios especificados en el ámbito de todo el sistema.

Sí

Usuario actual

Solo los perfiles DE ACUERDO y CDMP se pueden asociar a dispositivos y, por tanto, se pueden enumerar para los dispositivos.

Se enumeran los perfiles que se instalan y cumplen los criterios especificados en el ámbito de todo el sistema.

Sí

${ROWSPAN2}$Enumerate asociados a un dispositivo determinado que cumplen determinados criterios, como la clase de dispositivo y la clase de perfil${REMOVE}$  

Todo el sistema

Solo se pueden asociar y enumerar perfiles DE CMP y CDMP para dispositivos.

Se enumeran los perfiles asociados al dispositivo en el ámbito de todo el sistema y que cumplen los criterios especificados en el ámbito de todo el sistema.

Sí

Usuario actual

Solo se pueden asociar y enumerar perfiles DE TOM y CDMP para dispositivos.

Se enumeran los perfiles que están disponibles como asociados al dispositivo en el ámbito de usuario actual, que incluye las asociaciones de todo el sistema y cumple los criterios especificados en el ámbito del usuario actual.

Sí



 

La enumeración COLORPROFILETYPE proporciona los tipos de perfil de color válidos.

La enumeración COLORPROFILESUBTYPE proporciona los subtipos de perfil de color válidos.

Las combinaciones válidas de tipo de perfil y subtipo se muestran en la tabla siguiente.



COLORPROFILETYPE 

COLORPROFILESUBTYPE válido

Notas

Valor predeterminado del dispositivo

Valor predeterminado global

Uso previsto

Uso previsto

CPT \_ ICC

CPST \_ NONE

Obtener o establecer el perfil PREDETERMINADO de ASSOCIATED asociado a un dispositivo

CPST \_ RGBWorkingSpace o CPST \_ CustomWorkingSpace

Obtiene o establece el perfil DEER COMO PERFIL RGB global o perfil de espacio de trabajo personalizado. Vea la Nota.

ColorPROFILETYPE CPT \_ ICC y CPT \_ DMP son mutuamente excluyentes. El perfil de color predeterminado que establezca para un espacio de trabajo determinado (RGB o Personalizado) puede ser un perfil DE COLOR O DMP, pero no ambos.

CPT \_ DMP

CPST \_ NONE

Obtener o establecer el perfil de DMP predeterminado asociado a un dispositivo

CPST \_ RGBWorkingSpace o CPST \_ CustomWorkingSpace

Obtiene o establece el perfil de DMP como perfil RGB global o de espacio de trabajo personalizado. Vea la Nota.

ColorPROFILETYPE CPT \_ ICC y CPT \_ DMP son mutuamente excluyentes. El perfil de color predeterminado que establezca para un espacio de trabajo determinado (RGB o Personalizado) puede ser un perfil DE COLOR O DMP, pero no ambos.



 

> [!Note]  
> Cuando se llama a WcsSetDefaultColorProfile para establecer un perfil DMP como perfil predeterminado para el espacio de trabajo RGB o un espacio de trabajo personalizado, solo es válido un perfil DMP de tipo RGBVirtualDevice, RGB o CRT.
>
>  
>
> Cuando se llama a WcsSetDefaultColorProfile para establecer un perfil DEER COMO perfil predeterminado para el espacio de trabajo RGB o un espacio de trabajo personalizado, solo es válido un perfil DE COLOR CUYA clase sea "spac" o "disp" y cuyo espacio de color sea "RGB".

 

La arquitectura está diseñada según los requisitos de las operaciones, como se mencionó en las enumeraciones y tablas anteriores.

### <a name="profile-management-public-api-layer"></a>Capa de API pública de administración de perfiles

Dado que el ámbito de administración de perfiles no es compatible con las API ICM2 heredadas, se requiere un nuevo conjunto de API de administración de perfiles de WCS que defina el ámbito de administración de perfiles como usuario actual o de todo el sistema. ? Las API ICM2 heredadas siguen siendo compatibles con versiones anteriores y funcionan en el ámbito de administración de perfiles implícito para la llamada. o API de ICM2 que funcionan en el ámbito de usuario actual ? Esto es para las operaciones que se admiten para el ámbito de usuario actual y de todo el sistema en la administración de perfiles de WCS. Las API ICM2 heredadas llaman a en nuevas API de WCS con ámbito de administración de perfiles como usuario actual. Esto tiene sentido desde la perspectiva del usuario, ya que permite la configuración por usuario desde aplicaciones heredadas y también la ejecución de la mayoría de las operaciones en el contexto lua. o API de ICM2 que funcionan en el ámbito de todo el sistema ? Esto es para las operaciones (instalar perfiles y desinstalar perfiles) que solo admiten el ámbito de todo el sistema. No se crean nuevas API de administración de perfiles de WCS y se pueden modificar las API existentes.

Las implementaciones subyacentes de las operaciones de administración de perfiles funcionan en las siguientes entidades de datos de configuración para crear el contexto para que los algoritmos de procesamiento de colores proporcionen funcionalidades de administración de colores. Son configuraciones específicas del dispositivo o globales (independientes del dispositivo). o Datos de configuración específicos del dispositivo: ? Lista de perfiles asociados a un dispositivo determinado. ? Perfil predeterminado para los distintos tipos de perfil asociados a un dispositivo. ? Modo de coincidencia de perfiles usados para la enumeración. o Datos de configuración global: ? Lista de perfiles instalados en el sistema. ? Perfil predeterminado global para diferentes tipos de perfil. ? Las implementaciones subyacentes del almacenamiento de datos de configuración toman el ámbito de almacenamiento para los datos de configuración (independiente del dispositivo o específico del dispositivo), que puede ser un usuario actual o de todo el sistema. Esto es diferente del ámbito de administración de perfiles. Una operación con el ámbito de administración de perfiles de usuario actual puede provocar una lectura desde un ámbito de almacenamiento de todo el sistema si la configuración de usuario actual para esa operación no está presente. ? La capa de API de ICM2/WCS llama a en esta capa de almacenamiento para obtener y establecer datos con el ámbito de almacenamiento adecuado. La capa de almacenamiento es transparente para el ámbito de administración de perfiles. Lógica para combinar datos de los ámbitos de almacenamiento del usuario actual y de todo el sistema para crear o actualizar una configuración según el ámbito de administración de perfiles especificado por el autor de la llamada a la API. Esta lógica está presente en la capa de API de ICM2/WCS.

### <a name="device-specific-storage-layer"></a>Capa de almacenamiento específica del dispositivo

El almacenamiento de diferentes clases de dispositivos, como la impresión, la captura o la presentación, podría ser diferente entre sí. Por ejemplo, los datos de configuración de un dispositivo de impresión deben almacenarse mediante las API de impresión estándar, como SetPrinterDataEx y GetPrinterDataEx, para permitir que los perfiles se copien y la configuración se transfiera a un equipo cliente durante la conexión de punto e impresión. ? Esta capa exporta funcionalidad para abrir el almacén, obtener datos, establecer datos y cerrar el almacén mediante interfaces predefinidas comunes para que la capa de almacenamiento de configuración de administración de perfiles pueda llamar a ellos a la vez que es transparente para la forma en que se almacenan los datos para ese dispositivo.

El diagrama siguiente muestra esta arquitectura.



Capa de API pública de Administración de perfiles

${ROWSPAN2}$Legacy API de ICM2 para operaciones que solo admiten el ámbito de administración de perfiles de todo el sistema en Vista (instalar, desinstalar y obtener el directorio de color). Llaman a la capa de almacenamiento de configuración con el ámbito de almacenamiento adecuado.${REMOVE}$  

API ICM2 heredada para operaciones que admiten el ámbito de administración de perfiles de usuario actual y de todo el sistema en Vista (todas las operaciones que no son instalar, desinstalar y obtener el directorio de color). Funcionan implícitamente en el ámbito del usuario actual y llaman a la nueva API de WCS con el ámbito de administración de perfiles como usuario actual.

Nueva API de WCS con compatibilidad con el ámbito de administración de perfiles de usuario actual y de todo el sistema. Llaman a la capa de almacenamiento de configuración con el ámbito de almacenamiento adecuado.



 



Capa de configuración Storage administración de perfiles

Rutinas de configuración global independientes del dispositivo

Rutinas de configuración específicas del dispositivo

${ROWSPAN3}$Profile la instalación y la administración de la configuración de perfil predeterminada independiente del dispositivo, admitida en el ámbito de almacenamiento del usuario actual y en todo el sistema.${REMOVE}$  

Asociación de dispositivos y administración de la configuración de perfil predeterminada específica del dispositivo, admitida en el ámbito de almacenamiento de usuarios actuales y de todo el sistema.

Device-Specific Storage capa

Impresión de almacenamiento específico

Mostrar almacenamiento específico

Captura de almacenamiento específico



 

Las API ICM2 heredadas para las operaciones que solo admiten el ámbito de administración de perfiles de todo el sistema en Vista no tienen ningún cambio de comportamiento. Las operaciones de instalación y desinstalación están en esta categoría.

Las API ICM2 heredadas para las operaciones que admiten el ámbito de administración de perfiles de usuario actual y de todo el sistema han cambiado su comportamiento para consultar y configurar las opciones de usuario actual. Todas las operaciones que no son de instalación y desinstalación están en esta categoría.

 

 




