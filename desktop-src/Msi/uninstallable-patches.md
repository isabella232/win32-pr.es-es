---
description: El hecho de que una revisión se pueda desinstalar depende de cómo se haya creado la revisión, la versión de Windows Installer utilizada para instalar la revisión y los cambios realizados por la revisión en la aplicación.
ms.assetid: 95a5365c-e2ae-4e35-9aeb-67d04e67c7df
title: Revisiones desinstalables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad46d85318378ed81d2278d3ea1290152723704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539875"
---
# <a name="uninstallable-patches"></a>Revisiones desinstalables

El hecho de que una revisión se pueda desinstalar depende de cómo se haya creado la revisión, la versión de Windows Installer utilizada para instalar la revisión y los cambios realizados por la revisión en la aplicación. Si no se instala una revisión, la única manera de quitar la revisión es desinstalar toda la aplicación y reinstalar sin aplicar la revisión que se va a quitar.

Puede llamar a para la desinstalación de revisiones aplicadas con Windows Installer versión 3,0 mediante [las opciones](command-line-options.md)de la línea de comandos, la función [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) o el [**método RemovePatches**](installer-removepatches.md) como se describe en la sección [desinstalación de revisiones](uninstalling-patches.md) . El Windows Installer comprueba que cada una de las revisiones enumeradas para su eliminación en la propiedad [**MSIPATCHREMOVE**](msipatchremove.md) es desinstalable. Si el usuario no tiene privilegios para quitar la revisión, la revisión es desconocida para el producto, la Directiva de revisión impide la eliminación o la revisión se marcó como no desinstalable, el instalador devuelve un error que indica que se ha producido un error en la transacción de instalación.

**Windows Installer 2,0:** No compatible. Las revisiones aplicadas mediante una versión de Windows Installer anterior a Windows Installer 3,0 no se pueden desinstalar.

## <a name="patches-that-are-not-uninstallable"></a>Revisiones que no se pueden instalar

Las revisiones (archivos. msp) aplicadas a una aplicación instalada no se desinstalan en los casos siguientes. El único método para quitar una revisión que no se pueda desinstalar es desinstalar la aplicación con revisión y, a continuación, volver a instalar la aplicación sin volver a aplicar la revisión. En este caso, debe volver a aplicar las revisiones que no desea que se quiten de la aplicación.

-   Las revisiones aplicadas mediante una versión de Windows Installer inferior a Windows Installer 3,0 no se pueden desinstalar.
-   Las revisiones que se aplican a las aplicaciones instaladas en un equipo que tiene la directiva [DisablePatchUninstall](disablepatchuninstall.md) establecida por un administrador no se pueden desinstalar. Cuando se establece esta [Directiva de equipo](machine-policies.md), no se puede desinstalar ninguna revisión en el equipo, ni siquiera un administrador.
-   No se pueden desinstalar las revisiones que no tienen una tabla [MsiPatchMetadata](msipatchmetadata-table.md) en su base de datos.
-   No se pueden desinstalar las revisiones que no incluyen la siguiente fila en la tabla [MsiPatchMetadata](msipatchmetadata-table.md) . La revisión no se instala para otros valores de Company, Property y Value.

    | Compañía | Propiedad     | Value |
    |---------|--------------|-------|
    | Acepta  | AllowRemoval | 1     |

    

     

-   La revisión se ha aplicado a una aplicación instalada en un contexto para el que el usuario no tiene privilegios suficientes para desinstalar las revisiones. Las palabras "no permitidas" de la tabla siguiente indican que un administrador o un usuario que no es administrador no puede desinstalar revisiones de aplicaciones con revisión instaladas en este contexto. La palabra "permitido" de esta tabla significa que los privilegios no impiden que un administrador o un usuario que no sea administrador desinstale revisiones; sin embargo, por alguna de las demás razones descritas en esta sección, es posible que aún no sea posible desinstalar la revisión.

    | Contexto de instalación de la aplicación        | Desinstalación del administrador de revisiones | Desinstalación de revisión que no es de administrador                                                                                                                                                                                                                                                                             |
    |-----------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Per-Machine                             | Permitido                          | Por lo general, no se permite la única excepción si se aplicó la revisión mediante la aplicación de revisiones (LUA). Un parche marcado como una revisión de LUA es desinstalable por administradores o usuarios que no son administradores. La revisión de LUA solo está disponible para los paquetes instalados por equipo desde el medio y requieren una creación especial.<br/> |
    | Per-User no administrado para el usuario actual   | Permitida                          | Permitida                                                                                                                                                                                                                                                                                                          |
    | Per-User no administrado para diferentes usuarios | No permitida                      | No permitida                                                                                                                                                                                                                                                                                                      |
    | Per-User administrado para el usuario actual       | Permitido                          | No permitida                                                                                                                                                                                                                                                                                                      |
    | Per-User administrado para diferentes usuarios     | No permitida                      | No permitida                                                                                                                                                                                                                                                                                                      |

    

     

-   Una [actualización importante](major-upgrades.md) aplicada por una revisión no se instala. Las actualizaciones principales de una aplicación deben realizarse mediante la instalación de la aplicación actualizada (archivo. msi) en lugar de una revisión.
-   Las revisiones que se aplican a una instalación administrativa no se pueden desinstalar. No se recomienda aplicar revisiones a las instalaciones administrativas. El conjunto actual de revisiones debe aplicarse en el equipo del usuario después de que el usuario instala la aplicación desde la imagen administrativa. Esto puede impedir que el [código de paquete](package-codes.md) almacenado en caché en el equipo del usuario sea diferente del código del paquete en la instalación administrativa. Si el código de paquete almacenado en memoria caché en el equipo del usuario se diferencia de los de la instalación administrativa, vuelva a instalar la aplicación desde la instalación administrativa y, a continuación, aplique una revisión al equipo cliente.
-   Cuando una revisión agrega contenido nuevo a cualquiera de las tablas de la lista siguiente, Windows Installer marca la revisión como no desinstalable. Una revisión que no se puede instalar puede agregar nuevos archivos, ensamblados, entradas del registro, componentes o características a una instalación agregando nuevas filas a las tablas de base de datos que no están incluidas en esta lista.

    -   [AppId](appid-table.md)
    -   [BindImage](bindimage-table.md)
    -   [Clase](class-table.md)
    -   [ComPlus](complus-table.md)
    -   [CreateFolder](createfolder-table.md)
    -   [DuplicateFile](duplicatefile-table.md)
    -   [Entorno](environment-table.md)
    -   [Extensión](extension-table.md)
    -   [Fuente](font-table.md)
    -   [IniFile](inifile-table.md)
    -   [IsolatedComponent](isolatedcomponent-table.md)
    -   [LockPermissions](lockpermissions-table.md)
    -   [MsiLockPermissionsEx](msilockpermissionsex-table.md)
    -   [Mine](mime-table.md)
    -   [MoveFile](movefile-table.md)
    -   [MsiServiceConfig](msiserviceconfig-table.md)
    -   [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md)
    -   [ODBCAttribute](odbcattribute-table.md)
    -   [ODBCDataSource](odbcdatasource-table.md)
    -   [ODBCDriver](odbcdriver-table.md)
    -   [ODBCSourceAttribute](odbcsourceattribute-table.md)
    -   [ODBCTranslator](odbctranslator-table.md)
    -   [Programa](progid-table.md)
    -   [PublishComponent](publishcomponent-table.md)
    -   [RemoveIniFile](removeinifile-table.md)
    -   [SelfReg](selfreg-table.md)
    -   [ServiceControl](servicecontrol-table.md)
    -   [ServiceInstall](serviceinstall-table.md)
    -   [TypeLib](typelib-table.md)
    -   [Verbo](verb-table.md)
    -   [!Note]  
        > Si una revisión agrega contenido nuevo a las tablas [RemoveFile](removefile-table.md) o [RemoveRegistry](removeregistry-table.md) , Windows Installer no marca la revisión como no desinstalable. Sin embargo, la revisión no se instalará a menos que el recurso para quitar el nuevo contenido no exista en el paquete de instalación original. Por ejemplo, si la revisión agrega una nueva fila a la tabla RemoveFile, el archivo quitado no se puede restaurar desinstalando la revisión si el archivo es externo a la [tabla de archivos](file-table.md). El archivo se debe haber creado en la tabla de archivos del paquete original más las revisiones aplicadas de la revisión que se va a desinstalar.

         

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Secuenciación de revisiones](sequencing-patches.md)
</dt> <dt>

[Quitar revisiones](removing-patches.md)
</dt> <dt>

[Desinstalación de revisiones](uninstalling-patches.md)
</dt> <dt>

[Revisión de desinstalación de acciones personalizadas](patch-uninstall-custom-actions.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 




