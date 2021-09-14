---
description: Cumpla las siguientes directrices al crear un paquete de 64 bits Windows Installer.
ms.assetid: e7dfd188-fd4d-49d6-8cf5-c17182b697ca
title: Uso de paquetes de instalador de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b46ab8a9668d816ea99bd92c2575e9ea6367352
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069595"
---
# <a name="using-64-bit-windows-installer-packages"></a>Uso de paquetes de instalador de Windows de 64 bits

Al crear aplicaciones o paquetes del instalador de Windows de [64](64-bit-windows-installer-packages.md) bits que llaman a Windows Installer para instalar paquetes de 64 bits, haga lo siguiente:

-   Use un esquema Windows base de datos del instalador de 200 o superior. Especifique que la versión 2.0 es la versión mínima del instalador necesaria para instalar el paquete estableciendo la propiedad [**Resumen**](page-count-summary.md) de recuento de páginas en el entero 200. Las versiones Windows installer anteriores rechazan los intentos de instalar paquetes de 64 bits. Para los paquetes de 64 bits en la plataforma Arm64, el esquema de base de datos Windows Installer debe ser 500 o superior.
-   Indique en la [**propiedad Resumen de**](template-summary.md) plantilla del flujo de información de resumen del paquete que se trata de un paquete de 64 bits. Escriba "Intel64" en el campo de plataforma de la propiedad **Resumen** de plantilla si el paquete se va a ejecutar en un procesador Intel64. Escriba "x64" si el paquete se va a ejecutar en un procesador extendido de 64 bits. Escriba "Arm64" si el paquete se va a ejecutar en un procesador Arm64. Un paquete no se puede marcar como compatible con las  plataformas Intel64 y x64; un valor de propiedad Resumen de plantilla de "Intel64,x64" no es válido. Un paquete no se puede marcar como compatible con plataformas de  32 y 64 bits, los valores de propiedad Resumen de plantilla de "Intel,x64" o "Intel,Intel64" no son válidos.
-   Identifique cada componente de 64 bits estableciendo **msidbComponentAttributes64bit en** la columna Atributos de la [tabla Component.](component-table.md)
-   Use instrucciones condicionales opcionales que comprueben la versión del sistema operativo de 64 bits haciendo referencia a la [**propiedad VersionNT64.**](versionnt64.md) Windows El instalador establece esta propiedad en la versión de Windows de 64 bits y deja VersionNT64 sin definir si el sistema operativo no es de 64 Windows. Para obtener más información, [vea Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).
-   Use instrucciones condicionales opcionales que comprueben el nivel de procesador numérico del equipo haciendo referencia a la [**propiedad Intel64**](intel64.md) [**o Msix64.**](msix64.md) El Windows establece estas propiedades en el nivel de procesador numérico actual del equipo y deja la propiedad **Intel64** sin definir si no se trata de un procesador basado en Itanium. Para obtener más información, [vea Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).
-   Use la [tabla AppSearch y](appsearch-table.md) la [acción de AppSearch](appsearch-action.md) para realizar búsquedas opcionales del registro para los componentes de 64 bits existentes. Para buscar componentes de 64 bits existentes, incluya el bit **msidbLocatorType64bit** en la columna Type de la [tabla RegLocator](reglocator-table.md). Para obtener más información, vea Buscar aplicaciones, archivos, entradas del Registro o [.ini de entrada de archivo existentes.](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
-   Obtenga las rutas de acceso a las carpetas del sistema haciendo referencia a las propiedades [**System64Folder,**](system64folder.md) [**ProgramFiles64Folder**](programfiles64folder.md) y [**CommonFiles64Folder**](commonfiles64folder.md) para las carpetas de 64 bits y la propiedad [**SystemFolder,**](systemfolder.md) [**ProgramFilesFolder**](programfilesfolder.md) y [**CommonFilesFolder**](commonfilesfolder.md) para las carpetas de 32 bits.
-   Compruebe que la aplicación usa el GUID correcto al hacer referencia a un componente de 64 bits. Si hay versiones de 32 y 64 bits de un componente específico, deben tener GUID de identificador de componente diferentes.
-   Determine si es necesario definir nuevas variables de entorno al instalar aplicaciones de 64 bits.
-   Si se va a instalar un Administrador de controladores ODBC de 64 bits, el componente que lo lleva debe denominarse ODBCDriverManager64. El Administrador de controladores ODBC debe crearse en el paquete del instalador y se debe incluir un componente denominado ODBCDriverManager64. El administrador se instalará si es necesario.
-   Compruebe que la aplicación solo llama a servicios de 32 bits que se ejecutan como ejecutables. Las aplicaciones no deben llamar a servicios de 32 bits que se ejecutan en archivos DLL.
-   Si la aplicación instala versiones coexistntes de 32 y 64 bits de un componente, compruebe que la aplicación comparte .ini información de archivo correctamente.
-   Compruebe que la aplicación solo aplica revisiones de 32 bits a archivos binarios de 32 bits y revisiones de 64 bits a archivos binarios de 64 bits.
-   Considere escenarios de actualización futuros para las versiones de 32 y 64 bits y mantenga los códigos de actualización. Para obtener más información, vea [Aplicación de revisiones y actualizaciones.](patching-and-upgrades.md)
-   Cuando se usa [una aplicación](bootstrapping.md) de arranque para instalar un paquete de instalador de Windows de [64](64-bit-windows-installer-packages.md)bits, compile la aplicación de arranque como una aplicación de 64 bits.
-   Para deshabilitar [la](../winprog64/registry-reflection.md) reflexión del Registro para las claves del Registro afectadas por un componente determinado, establezca el bit **msidbComponentAttributesDisableRegistryReflection** en el campo Atributos de la tabla [Component.](component-table.md) Esto puede ser necesario para que coexistan copias de 32 y 64 bits de la misma aplicación. Si se establece este bit, Windows Installer llama a la función [**RegDisableReflectionKey**](/windows/win32/api/winreg/nf-winreg-regdisablereflectionkey) en cada clave a la que tiene acceso el componente. Este bit está disponible con Windows Installer versión 4.0. Este bit se omite en sistemas de 32 bits. Este bit se omite en las versiones de 64 bits de Windows XP y Windows 2000.

> [!Note]  
> El valor de la raíz numérica del Registro devuelta por el parámetro *lpPathBuf* de la función [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) distingue entre los componentes de los sistemas operativos de 32 y 64 bits. Para obtener más información, **vea Función MsiGetComponentPath.**

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acciones personalizadas de 64 bits](64-bit-custom-actions.md)
</dt> </dl>

 

 
