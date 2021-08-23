---
description: Si se puede desinstalar una revisión depende de cómo se haya creado la revisión, de la versión de Windows Installer usada para instalar la revisión y de los cambios realizados por la revisión en la aplicación.
ms.assetid: 95a5365c-e2ae-4e35-9aeb-67d04e67c7df
title: Revisiones que se pueden desinstalar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a3abea369a09dd51e995ba28dcab1463032bb6e5dec9648d3eae39be4cbf21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527645"
---
# <a name="uninstallable-patches"></a>Revisiones que se pueden desinstalar

Si se puede desinstalar una revisión depende de cómo se haya creado la revisión, de la versión de Windows Installer usada para instalar la revisión y de los cambios realizados por la revisión en la aplicación. Si una revisión no se puede desinstalar, la única manera de quitar la revisión es desinstalar toda la aplicación y volver a instalarla sin aplicar la revisión que se va a quitar.

Puede llamar a para la desinstalación de las revisiones aplicadas con la versión 3.0 del instalador de Windows mediante opciones de [](uninstalling-patches.md) línea de [comandos,](command-line-options.md)la función [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) o el método [**RemovePatches,**](installer-removepatches.md) tal y como se describe en la sección Desinstalación de revisiones. El Windows de aplicaciones comprueba que se puede desinstalar cada una de las revisiones enumeradas para su eliminación en la propiedad [**MSIPATCHREMOVE.**](msipatchremove.md) Si el usuario no tiene privilegios para quitar la revisión, la revisión es desconocida para el producto, la directiva de revisión impide la eliminación o la revisión se ha marcado como no desinstalable, el instalador devuelve un error que indica una transacción de instalación con errores.

**Windows Installer 2.0:** No se admite. Las revisiones aplicadas mediante una versión de Windows Installer anterior a Windows Installer 3.0 no se pueden desinstalar.

## <a name="patches-that-are-not-uninstallable"></a>Revisiones que no se pueden desinstalar

Una revisión (archivo .msp) aplicada a una aplicación instalada no se puede desinstalar en los casos siguientes. El único método para quitar una revisión que no se puede desinstalar es desinstalar la aplicación con revisión y, a continuación, volver a instalar la aplicación sin volver a aplicar la revisión. En este caso, debe volver a aplicar las revisiones que no desee quitar de la aplicación.

-   Las revisiones aplicadas mediante una versión de Windows Installer que sea inferior a Windows Installer 3.0 no se pueden desinstalar.
-   Las revisiones aplicadas a las aplicaciones instaladas en un equipo que tiene la directiva [DisablePatchUninstall](disablepatchuninstall.md) establecida por un administrador no se pueden desinstalar. Cuando se [ha establecido](machine-policies.md)esta directiva de equipo, un administrador no puede desinstalar ninguna revisión en el equipo.
-   Las revisiones que no tienen una [tabla MsiPatchMetadata](msipatchmetadata-table.md) en su base de datos no se pueden desinstalar.
-   Las revisiones que no incluyen la fila siguiente en su [tabla MsiPatchMetadata](msipatchmetadata-table.md) no se pueden desinstalar. La revisión no se puede desinstalar para otros valores de Company, Property y Value.

    | Compañía | Propiedad     | Valor |
    |---------|--------------|-------|
    | {Null}  | AllowRemoval | 1     |

    

     

-   La revisión se ha aplicado a una aplicación instalada en un contexto para el que el usuario no tiene privilegios suficientes para desinstalar revisiones. Las palabras "No permitido" de la tabla siguiente indican que un administrador o un usuario que no es administrador no puede desinstalar revisiones de las aplicaciones con revisión instaladas en este contexto. La palabra "Permitido" en esta tabla significa que los privilegios no impiden que un administrador o un usuario que no sea administrador desinstale las revisiones; sin embargo, por cualquiera de las otras razones que se deban tratar en esta sección, es posible que no sea posible desinstalar la revisión.

    | contexto de instalación de la aplicación        | Desinstalación de revisión por parte del administrador | Desinstalación de revisión que no es de administrador                                                                                                                                                                                                                                                                             |
    |-----------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Per-Machine                             | Permitido                          | Generalmente no permitido La única excepción es si la revisión se aplicó mediante la aplicación de revisiones (LUA). Los administradores o no administradores pueden desinstalar una revisión marcada como revisión de LUA. La aplicación de revisiones de LUA solo está disponible para los paquetes instalados por equipo desde medios y requieren una creación especial.<br/> |
    | Per-User no administrado para el usuario actual   | Permitida                          | Permitida                                                                                                                                                                                                                                                                                                          |
    | Per-User no administrado para distintos usuarios | No permitida                      | No permitida                                                                                                                                                                                                                                                                                                      |
    | Per-User administrado para el usuario actual       | Permitido                          | No permitida                                                                                                                                                                                                                                                                                                      |
    | Per-User administrado para distintos usuarios     | No permitida                      | No permitida                                                                                                                                                                                                                                                                                                      |

    

     

-   Una [actualización principal](major-upgrades.md) aplicada por una revisión no se puede desinstalar. Las actualizaciones principales de una aplicación deben realizarse instalando la aplicación actualizada (.msi archivo) en lugar de una revisión.
-   Las revisiones aplicadas a una instalación administrativa no se pueden desinstalar. No se recomienda aplicar revisiones a las instalaciones administrativas. El conjunto actual de revisiones debe aplicarse en el equipo del usuario después de que el usuario instale la aplicación desde la imagen administrativa. Esto puede impedir que el [código del paquete](package-codes.md) almacenado en caché en el equipo del usuario sea diferente del código del paquete en la instalación administrativa. Si el código del paquete almacenado en caché en el equipo del usuario es diferente del de la instalación administrativa, vuelva a instalar la aplicación desde la instalación administrativa y, a continuación, vuelva a aplicar revisiones al equipo cliente.
-   Cuando una revisión agrega contenido nuevo a cualquiera de las tablas de la lista siguiente, Windows Instalador marca la revisión como no desinstalable. Una revisión que se puede desinstalar puede agregar nuevos archivos, ensamblados, entradas del Registro, componentes o características a una instalación agregando nuevas filas a las tablas de base de datos que no están incluidas en esta lista.

    -   [Appid](appid-table.md)
    -   [BindImage](bindimage-table.md)
    -   [Clase](class-table.md)
    -   [Complus](complus-table.md)
    -   [CreateFolder](createfolder-table.md)
    -   [DuplicateFile](duplicatefile-table.md)
    -   [Entorno](environment-table.md)
    -   [Extensión](extension-table.md)
    -   [Fuente](font-table.md)
    -   [IniFile](inifile-table.md)
    -   [IsolatedComponent](isolatedcomponent-table.md)
    -   [LockPermissions](lockpermissions-table.md)
    -   [MsiLockPermissionsEx](msilockpermissionsex-table.md)
    -   [Mime](mime-table.md)
    -   [MoveFile](movefile-table.md)
    -   [MsiServiceConfig](msiserviceconfig-table.md)
    -   [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md)
    -   [ODBCAttribute](odbcattribute-table.md)
    -   [ODBCDataSource](odbcdatasource-table.md)
    -   [ODBCDriver](odbcdriver-table.md)
    -   [ODBCSourceAttribute](odbcsourceattribute-table.md)
    -   [ODBCTranslator](odbctranslator-table.md)
    -   [Progid](progid-table.md)
    -   [PublishComponent](publishcomponent-table.md)
    -   [RemoveIniFile](removeinifile-table.md)
    -   [SelfReg](selfreg-table.md)
    -   [ServiceControl](servicecontrol-table.md)
    -   [ServiceInstall](serviceinstall-table.md)
    -   [Typelib](typelib-table.md)
    -   [Verbo](verb-table.md)
    -   [!Note]  
        > Si una revisión agrega contenido nuevo a las tablas [RemoveFile](removefile-table.md) o [RemoveRegistry,](removeregistry-table.md) Windows Installer no marca la revisión como no desinstalable. Sin embargo, la revisión no se puede desinstalar a menos que el recurso para quitar el nuevo contenido no exista en el paquete de instalación original. Por ejemplo, si la revisión agrega una nueva fila a la tabla RemoveFile, el archivo quitado no se puede restaurar desinstalando la revisión si el archivo es externo a la [tabla File](file-table.md). El archivo debe haber sido creado en la tabla Archivo del paquete original más las revisiones aplicadas para que la revisión se pueda desinstalar.

         

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Secuenciación de revisiones](sequencing-patches.md)
</dt> <dt>

[Eliminación de revisiones](removing-patches.md)
</dt> <dt>

[Desinstalación de revisiones](uninstalling-patches.md)
</dt> <dt>

[Acciones personalizadas de desinstalación de revisiones](patch-uninstall-custom-actions.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 




