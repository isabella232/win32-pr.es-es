---
description: Siga las instrucciones que se indican a continuación para crear un paquete de Windows Installer de 64 bits.
ms.assetid: e7dfd188-fd4d-49d6-8cf5-c17182b697ca
title: Usar paquetes de Windows Installer de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b46ab8a9668d816ea99bd92c2575e9ea6367352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652848"
---
# <a name="using-64-bit-windows-installer-packages"></a>Usar paquetes de Windows Installer de 64 bits

Cuando cree [paquetes de Windows Installer de 64 bits](64-bit-windows-installer-packages.md) o aplicaciones que llamen a Windows Installer para instalar paquetes de 64 bits, haga lo siguiente:

-   Use un esquema de base de datos Windows Installer de 200 o superior. Especifique que la versión 2,0 es la versión mínima del instalador necesaria para instalar el paquete. para ello, establezca la propiedad [**Resumen de recuento de páginas**](page-count-summary.md) en el entero 200. Windows Installer versiones anteriores rechazan los intentos de instalar paquetes de 64 bits. En el caso de los paquetes de 64 bits en la plataforma Arm64, el esquema de la base de datos Windows Installer debe ser 500 o superior.
-   Indique en la propiedad Resumen de la [**plantilla**](template-summary.md) el flujo de información de Resumen de paquetes que se trata de un paquete de 64 bits. Escriba "Intel64" en el campo plataforma de la propiedad de Resumen de la **plantilla** si el paquete se va a ejecutar en un procesador Intel64. Escriba "x64" si el paquete se va a ejecutar en un procesador extendido de 64 bits. Escriba "Arm64" si el paquete se va a ejecutar en un procesador de Arm64. No se puede marcar un paquete como compatible con plataformas Intel64 y x64, un valor de propiedad de **Resumen de plantilla** de "Intel64, x64" no es válido. No se puede marcar un paquete como compatible con las plataformas de 32 bits y 64 bits, los valores de propiedad de Resumen de la **plantilla** "Intel, x64" o "Intel, Intel64" no son válidos.
-   Identifique cada componente de 64 bits estableciendo **msidbComponentAttributes64bit** en la columna Attributes de la tabla de [componentes](component-table.md) .
-   Use instrucciones condicionales opcionales que comprueben la versión del sistema operativo de 64 bits haciendo referencia a la propiedad [**VersionNT64**](versionnt64.md) . Windows Installer establece esta propiedad en la versión de Windows de 64 bits y deja VersionNT64 sin definir si el sistema operativo no es Windows de 64 bits. Para obtener más información, vea [usar propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md).
-   Use instrucciones condicionales opcionales que comprueben el nivel de procesador numérico del equipo mediante una referencia a la propiedad [**Intel64**](intel64.md) o [**Msix64**](msix64.md) . El Windows Installer establece estas propiedades en el nivel de procesador numérico actual del equipo y deja la propiedad **Intel64** sin definir si no se trata de un procesador Basado en Itanium. Para obtener más información, vea [usar propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md).
-   Use la [tabla AppSearch](appsearch-table.md) y la [acción AppSearch](appsearch-action.md) para realizar búsquedas opcionales del registro para los componentes de 64 bits existentes. Para buscar componentes de 64 bits existentes, incluya el bit **msidbLocatorType64bit** en la columna Type de la [tabla RegLocator](reglocator-table.md). Para obtener más información, vea [Buscar aplicaciones, archivos, entradas del registro o propiedades de entradas del archivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
-   Obtenga las rutas de acceso a las carpetas del sistema mediante una referencia a la propiedad [**System64Folder**](system64folder.md), la propiedad [**ProgramFiles64Folder**](programfiles64folder.md) y la propiedad [**CommonFiles64Folder**](commonfiles64folder.md) para las carpetas de 64 bits y la propiedad [**carpetadelsistema**](systemfolder.md) , la propiedad [**ProgramFilesFolder**](programfilesfolder.md) y la propiedad [**CommonFilesFolder**](commonfilesfolder.md) para las carpetas de 32 bits.
-   Compruebe que la aplicación utiliza el GUID correcto al hacer referencia a un componente de 64 bits. Si hay versiones de 32 bits y de 64 bits de un componente específico, deben tener distintos GUID de identificador de componente.
-   Determine si es necesario definir una nueva variable de entorno al instalar aplicaciones de 64 bits.
-   Si se va a instalar el administrador de controladores ODBC de 64 bits, el componente que lo lleva debe denominarse ODBCDriverManager64. El administrador de controladores ODBC debe estar creado en el paquete del instalador y debe incluirse un componente denominado ODBCDriverManager64. Si es necesario, el administrador se instalará.
-   Compruebe que la aplicación solo llama a los servicios de 32 bits que se ejecutan como ejecutables. Las aplicaciones no deben llamar a los servicios de 32 bits que se ejecutan en archivos dll.
-   Si la aplicación instala versiones coexistentes de 32 bits y de 64 bits de un componente, compruebe que la aplicación comparte correctamente la información del archivo. ini.
-   Compruebe que la aplicación solo aplica revisiones de 32 bits a archivos binarios de 32 bits y revisiones de 64 bits a archivos binarios de 64 bits.
-   Tenga en cuenta los escenarios de actualización futuros para las versiones de 32 bits y 64 bits y para mantener los códigos de actualización. Para obtener más información, consulte [revisiones y actualizaciones](patching-and-upgrades.md).
-   Cuando use una aplicación de [arranque](bootstrapping.md) para instalar un [paquete de Windows Installer de 64 bits](64-bit-windows-installer-packages.md), compile la aplicación de arranque como una aplicación de 64 bits.
-   Para deshabilitar la [reflexión del registro](../winprog64/registry-reflection.md) para las claves del registro que se ven afectadas por un componente determinado, establezca el bit **msidbComponentAttributesDisableRegistryReflection** en el campo atributos de la tabla [componente](component-table.md) . Esto puede ser necesario para que coexistan copias de 32 y 64 bits de la misma aplicación. Si se establece este bit, el Windows Installer llama a la función [**RegDisableReflectionKey**](/windows/win32/api/winreg/nf-winreg-regdisablereflectionkey) en cada clave a la que tiene acceso el componente. Este bit está disponible con Windows Installer versión 4,0. Este bit se omite en los sistemas de 32 bits. Este bit se omite en las versiones de 64 bits de Windows XP y Windows 2000.

> [!Note]  
> El valor de la raíz numérica del registro devuelto por el parámetro *lpPathBuf* de la función [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) distingue entre los componentes de los sistemas operativos de 32 y 64 bits. Para obtener más información, consulte función **MsiGetComponentPath** .

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acciones personalizadas de 64 bits](64-bit-custom-actions.md)
</dt> </dl>

 

 
