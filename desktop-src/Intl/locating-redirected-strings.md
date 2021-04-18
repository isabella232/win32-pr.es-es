---
description: En este tema se describen las instrucciones de programación para buscar cadenas de registro redirigidas. Para obtener más información, vea usar el redireccionamiento de cadenas del registro.
ms.assetid: 03d1512f-35a6-4b3a-9a0e-97e17bd9b126
title: Localizar cadenas redirigidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f11600ad57c04de54d914c2c876b67967dfa1467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687094"
---
# <a name="locating-redirected-strings"></a>Localizar cadenas redirigidas

En este tema se describen las instrucciones de programación para buscar cadenas de registro redirigidas. Para obtener más información, vea [usar el redireccionamiento de cadenas del registro](using-registry-string-redirection.md).

## <a name="load-a-language-neutral-registry-value"></a>Carga de un valor del registro de Language-Neutral

En Windows Vista y versiones posteriores, la aplicación MUI usa un valor del registro independiente del lenguaje para permitir el acceso a cadenas específicas del idioma almacenadas en una tabla de recursos de cadena. Para obtener más información, vea crear un recurso de Language-Neutral en [con el redireccionamiento de cadenas del registro](using-registry-string-redirection.md).

El código de aplicación que lee el valor independiente del lenguaje del registro debe cargar las cadenas en el idioma de la interfaz de usuario correcto mediante una llamada a [**RegLoadMUIStringW**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa). Si usa esta función, la aplicación no tiene que tratar explícitamente con la carga de recursos.

Si está actualizando una aplicación existente al uso independiente del lenguaje del registro, normalmente mantendrá los valores de cadena existentes, localizados en inglés o en algún otro idioma del registro, como reserva y por compatibilidad con versiones anteriores. Mantener una cadena literal en el registro permite a la aplicación revertir a la cadena literal si se produce un error en una llamada a [**RegLoadMUIStringW**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa) . Debe decidir cómo implementar este tipo de reserva, ya que MUI no proporciona compatibilidad con dicha implementación.

## <a name="use-shell-api-to-set-shortcut-strings-from-the-registry"></a>Usar la API de Shell para establecer cadenas de acceso directo del registro

La aplicación puede usar la API de Shell para crear cadenas para los accesos directos que vinculan archivos o carpetas en el menú **Inicio** o en el escritorio. Para obtener más información, vea crear recursos para cadenas de acceso directo en [usar redirección de cadenas del registro](using-registry-string-redirection.md).

La aplicación puede utilizar [**SHSetLocalizedName**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) para cargar el nombre para mostrar conforme a MUI para un acceso directo. Debe usar [**IShellLink:: SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) para establecer el recuadro informativo asociado. Las llamadas registran las cadenas con el registro. Considere los ejemplos siguientes, para los que "HKCR" representa la \_ \_ clave del Registro raíz de las clases HKEY:


```C++
HKCR,"CLSID\%CLSID_AntiSpyware%",,,"Windows AntiSpyware"

HKCR,"CLSID\%CLSID_AntiSpyware%","LocalizedString",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-104"

HKCR,"CLSID\%CLSID_AntiSpyware%","InfoTip",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-208"
```



La primera línea proporciona una cadena literal no localizada para la reserva y la compatibilidad con versiones anteriores. La segunda línea muestra la manera compatible con MUI de registrar el nombre para mostrar. Esta línea indica el identificador de cadena 104 almacenado en Msascui.exe (para Windows XP) o en su archivo específico de idioma asociado (para Windows Vista). Este identificador de cadena corresponde a "mis sitios de red". La tercera línea del ejemplo controla el registro de recuadro informativo. % CLSID \_ anti spyware% especifica una variable de entorno que representa el GUID que coincide con el identificador de clase de este componente.

En el ejemplo mostrado anteriormente, la aplicación llama a [**SHSetLocalizedName**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) para especificar la ruta de acceso del archivo ejecutable para los dos primeros parámetros y especifica *idsRes* como "@% ProgramFiles% \\ Windows AntiSpyware \\MSASCui.exe, 104". Una llamada a [**IShellLink:: SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription)especifica la ruta de acceso del recuadro informativo como "@% ProgramFiles% \\ Windows AntiSpyware \\MSASCui.exe, 208".

## <a name="query-friendly-document-type-names-in-the-registry"></a>Consultar los nombres de tipo de documento descriptivos en el registro

La creación de recursos para los nombres de tipo de documento descriptivos se describe en creación de recursos para nombres de tipos de documentos descriptivos en [con el redireccionamiento de cadenas del registro](using-registry-string-redirection.md). Para consultar un nombre descriptivo del documento, la aplicación debe usar [**IQueryAssociations:: init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init), seguida de una llamada a [**IQueryAssociations:: GetString**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-getstring). La llamada a **IQueryAssociations:: init** especifica el tipo de documento, por ejemplo, ". txt". La llamada a **IQueryAssociations:: GetString** debe especificar ASSOCSTR \_ FRIENDLYDOCNAME como identificador de cadena.

## <a name="register-microsoft-management-console-snap-in-strings-not-read-from-the-registry"></a>Registrar cadenas de complementos de Microsoft Management Console no leídas del registro

La aplicación puede usar un complemento de Microsoft Management Console (MMC) para hospedar sus tareas de administración. La mayoría de las cadenas se administran como recursos mediante la configuración del registro descrita en creación de recursos de cadena para Microsoft Management Console Snap-Ins en uso de la [redirección de cadenas del registro](using-registry-string-redirection.md). Sin embargo, algunos complementos registran valores de cadena del registro que MMC no puede leer del registro. En este caso, el complemento debe obtener los valores mediante la interfaz [**ISnapinAbout**](/windows/win32/api/mmc/nn-mmc-isnapinabout) , que es compatible con MUI.

## <a name="set-the-display-name-and-description-for-a-windows-service-from-the-registry"></a>Establecer el nombre para mostrar y la descripción de un servicio de Windows desde el registro

Si la aplicación MUI usa un servicio de Windows, debe mostrar el nombre para mostrar y la descripción del servicio. Los recursos asociados se describen en "crear recursos de cadena para un servicio de Windows" en [mediante el redireccionamiento de cadenas del registro](using-registry-string-redirection.md).

Para establecer el nombre para mostrar del servicio, la aplicación MUI llama a [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) o a [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga). El nombre es una cadena con el formato " `@<PE-path>,-<stringID>[;<comment>]` ". Por ejemplo, si el servicio se implementa mediante un archivo. dll con la ruta de acceso% ProgramFiles% \\ % myPath% \\MyDll.dll, y el identificador de cadena del nombre para mostrar específico del idioma es 347, el parámetro se especifica como " `@%ProgramFiles%\\%MyPath%\\MyDll.dll,-347` ". Las barras diagonales inversas dobles ( \\ \\ ) son necesarias porque C/C++ usa la barra diagonal inversa como carácter de escape en las cadenas.

Para establecer la descripción del servicio específico del lenguaje, la aplicación MUI debe hacer que el miembro **lpDescription** de una estructura de [**\_ Descripción del servicio**](/windows/win32/api/winsvc/ns-winsvc-service_descriptiona) indique una cadena de la forma " `@<PE-path>,-<stringID>[;<comment>]` ", que hace referencia al identificador de cadena adecuado. A continuación, la aplicación llama a [**ChangeServiceConfig2**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfig2a) con el parámetro *dwInfoLevel* especificado como descripción de configuración del servicio \_ \_ y parámetro *lpInfo* especificado como la estructura de **\_ Descripción del servicio** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ubicar recursos PE de Win32](locating-win32-pe-resources.md)
</dt> <dt>

[Usar el redireccionamiento de cadenas del registro](using-registry-string-redirection.md)
</dt> </dl>

 

 
