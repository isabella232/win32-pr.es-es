---
description: En este tema se de abordan las instrucciones de programación para buscar cadenas del Registro redirigidas. Para obtener más información, vea Uso del redireccionamiento de cadenas del Registro.
ms.assetid: 03d1512f-35a6-4b3a-9a0e-97e17bd9b126
title: Buscar cadenas redirigidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f11600ad57c04de54d914c2c876b67967dfa1467
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274191"
---
# <a name="locating-redirected-strings"></a>Buscar cadenas redirigidas

En este tema se de abordan las instrucciones de programación para buscar cadenas del Registro redirigidas. Para obtener más información, vea [Using Registry String Redirection](using-registry-string-redirection.md).

## <a name="load-a-language-neutral-registry-value"></a>Carga de un Language-Neutral del Registro

En Windows Vista y versiones posteriores, la aplicación DEA usa un valor del Registro neutro en el idioma para permitir el acceso a cadenas específicas del idioma almacenadas en una tabla de recursos de cadena. Para obtener más información, vea Crear un recurso de Language-Neutral en [Uso del redireccionamiento de cadenas del Registro.](using-registry-string-redirection.md)

El código de aplicación que lee el valor neutro del idioma del Registro debe cargar las cadenas en el lenguaje de interfaz de usuario correcto mediante una llamada [**a RegLoadMUIStringW**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa). Si usa esta función, la aplicación no tiene que tratar explícitamente con la carga de recursos.

Si va a actualizar una aplicación existente al uso neutro del idioma del registro, normalmente mantendrá los valores de cadena existentes, localizados en inglés o en algún otro idioma único del Registro, como reserva y por compatibilidad con versiones anteriores. Mantener una cadena literal en el Registro permite a la aplicación volver a la cadena literal si se produce un error en una llamada a [**RegLoadMUIStringW.**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa) Debe decidir cómo implementar este tipo de reserva, ya que LAN no proporciona compatibilidad con dicha implementación.

## <a name="use-shell-api-to-set-shortcut-strings-from-the-registry"></a>Uso de shell API para establecer cadenas de acceso directo desde el Registro

La aplicación puede usar la API de shell para crear cadenas para accesos directos que vinculan archivos o carpetas en el **menú** Inicio o en el escritorio. Para obtener más información, vea Crear recursos para cadenas de acceso directo en [Using Registry String Redirection](using-registry-string-redirection.md).

La aplicación puede usar [**SHSetLocalizedName para**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) cargar el nombre para mostrar compatible con MUI para un acceso directo. Debe usar [**IShellLink::SetDescription para**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) establecer la información sobre información asociada. Las llamadas registran las cadenas en el registro. Tenga en cuenta los ejemplos siguientes, para los que "HKCR" representa la clave raíz del Registro HKEY \_ \_ CLASSES:


```C++
HKCR,"CLSID\%CLSID_AntiSpyware%",,,"Windows AntiSpyware"

HKCR,"CLSID\%CLSID_AntiSpyware%","LocalizedString",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-104"

HKCR,"CLSID\%CLSID_AntiSpyware%","InfoTip",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-208"
```



La primera línea proporciona una cadena literal sin localizar para la compatibilidad con versiones anteriores y de reserva. La segunda línea muestra la manera compatible con MUI de registrar el nombre para mostrar. Esta línea indica el identificador de cadena 104 almacenado en Msascui.exe (para Windows XP) o en su archivo específico del idioma asociado (para Windows Vista). Este identificador de cadena corresponde a "Mis lugares de red". La tercera línea del ejemplo controla el registro de información sobre información. %CLSID AntiSpyware% especifica una variable de entorno que representa el GUID que coincide con \_ el identificador de clase de este componente.

En el ejemplo anterior, la aplicación llama a [**SHSetLocalizedName**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) para especificar la ruta de acceso del ejecutable para los dos primeros parámetros y especificar *idsRes* como "@%ProgramFiles% \\ Windows AntiSpyware \\MSASCui.exe,104". Una llamada a [**IShellLink::SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription)especifica la ruta de acceso de InfoTip como "@%ProgramFiles% \\ Windows AntiSpyware \\MSASCui.exe,208".

## <a name="query-friendly-document-type-names-in-the-registry"></a>Nombres de tipos de documento descriptivos de consulta en el Registro

La creación de recursos para nombres de tipo de documento descriptivos se describe en Crear recursos para nombres de tipo de documento descriptivos en Uso del redireccionamiento [de cadenas del Registro](using-registry-string-redirection.md). Para consultar un nombre de documento descriptivo, la aplicación debe usar [**IQueryAssociations::Init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init), seguido de una llamada a [**IQueryAssociations::GetString**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-getstring). La llamada a **IQueryAssociations::Init** especifica el tipo de documento, por ejemplo, ".txt". La llamada a **IQueryAssociations::GetString** debe especificar ASSOCSTR \_ FRIENDLYDOCNAME como identificador de cadena.

## <a name="register-microsoft-management-console-snap-in-strings-not-read-from-the-registry"></a>Registrar Microsoft Management Console cadenas de complemento no leídas del Registro

La aplicación puede usar un complemento Microsoft Management Console (MMC) para hospedar sus tareas de administración. La mayoría de las cadenas se administran como recursos mediante la configuración del Registro descrita en Crear recursos de cadena para Microsoft Management Console Snap-Ins en Uso del redireccionamiento de [cadenas del Registro.](using-registry-string-redirection.md) Sin embargo, algunos complementos registran valores de cadena del Registro que MMC no puede leer del registro. En este caso, el complemento debe obtener los valores mediante la interfaz [**ISnapinAbout,**](/windows/win32/api/mmc/nn-mmc-isnapinabout) que es compatible con MUI.

## <a name="set-the-display-name-and-description-for-a-windows-service-from-the-registry"></a>Establecer el nombre para mostrar y la descripción de un servicio Windows desde el Registro

Si la aplicación DEA usa un Windows, debe mostrar el nombre para mostrar y la descripción del servicio. Los recursos asociados se de abordan en "Crear recursos de cadena para un Windows service" en [Using Registry String Redirection](using-registry-string-redirection.md).

Para establecer el nombre para mostrar del servicio, la aplicación DEA llama a [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) o [**ChangeServiceConfig.**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga) El nombre es una cadena con el formato " `@<PE-path>,-<stringID>[;<comment>]` ". Por ejemplo, si el servicio se implementa mediante un archivo .dll con la ruta de acceso %ProgramFiles% %MyPath%MyDll.dll y el identificador de cadena del nombre para mostrar específico del idioma es \\ 347, el parámetro se especifica \\ como " `@%ProgramFiles%\\%MyPath%\\MyDll.dll,-347` ". Las barras diagonales inversas dobles ( ) son necesarias porque C/C++ usa la barra diagonal inversa como carácter \\ \\ de escape en las cadenas.

Para establecer la descripción del servicio específica del idioma, la aplicación DEAme debe hacer que el miembro **lpDescription** de una estructura [**SERVICE \_ DESCRIPTION**](/windows/win32/api/winsvc/ns-winsvc-service_descriptiona) indique una cadena de formato " ", haciendo referencia al identificador `@<PE-path>,-<stringID>[;<comment>]` de cadena adecuado. A continuación, la aplicación llama a [**ChangeServiceConfig2**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfig2a) con el parámetro *dwInfoLevel* especificado como SERVICE CONFIG DESCRIPTION y el parámetro lpInfo especificado \_ como estructura SERVICE \_ **\_ DESCRIPTION.** 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búsqueda de recursos de Win32 PE](locating-win32-pe-resources.md)
</dt> <dt>

[Uso del redireccionamiento de cadenas del Registro](using-registry-string-redirection.md)
</dt> </dl>

 

 
