---
description: El método recomendado para generar un paquete de revisión es usar herramientas de creación de revisiones como Msimsp.exe y Patchwiz.dll. La herramienta Msimsp.exe solo está disponible en los componentes de Windows SDK para Windows Installer desarrolladores.
ms.assetid: fa8e9d68-3db1-4d17-aa99-2ca0ed421c7a
title: Msimsp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1810fd0c544695742273bbb0e63b22138529c129
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105678657"
---
# <a name="msimspexe"></a>Msimsp.exe

El método recomendado para generar un paquete de revisión es usar herramientas de creación de revisiones como Msimsp.exe y [Patchwiz.dll](patchwiz-dll.md). La herramienta Msimsp.exe solo está disponible en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).

Msimsp.exe es un archivo ejecutable que llama a [Patchwiz.dll](patchwiz-dll.md). La herramienta se puede usar para crear un paquete de revisión pasando la ruta de acceso a un archivo de propiedades de creación de revisiones (archivo. PCP) y la ruta de acceso al paquete de revisión que se va a crear. Msimsp. ex también puede usarse para crear un archivo de registro y especificar una carpeta temporal en la que se guardan las transformaciones, los archivadores y los archivos que se usan para crear el paquete de revisión.

La sintaxis de línea de comandos para Msimsp.exe es:

Ruta de acceso **Msimsp.exe-s** *\[ al archivo \] . PCP* **-p** *\[ ruta de acceso \] al archivo. MSP* **{Options}**

Las opciones de línea de comandos no distinguen mayúsculas de minúsculas y se pueden usar delimitadores de barras diagonales en lugar de guiones. Si no se especifican opciones, Msimsp.exe muestra los valores actuales de las propiedades de información de resumen.

<dl> <dt>

<span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[ ruta de acceso al archivo \] . PCP_
</dt> <dd>

Esto es necesario y debe ir seguido de la ruta de acceso al archivo de propiedades de creación de revisiones (extensión. PCP). Para obtener más información, vea [PatchWiz.dll](patchwiz-dll.md).

</dd> <dt>

<span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_ruta de acceso al archivo. MSP_
</dt> <dd>

Esto es necesario y va seguido de la ruta de acceso al paquete de revisión que se va a crear (extensión. msp).

</dd> <dt>

<span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_ruta de acceso a la carpeta temporal_
</dt> <dd>

Opcional. Seguido de la ruta de acceso a la carpeta temporal. La ubicación predeterminada es% TMP% \\ ~ PCW \_ tmp. tmp \\ .

</dd> <dt>

<span id="-k"></span><span id="-K"></span>**-k**
</dt> <dd>

Opcional. Se produce un error si la carpeta temporal ya existe.

</dd> <dt>

<span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_ruta de acceso al archivo de registro_
</dt> <dd>

Opcional. Seguido de la ruta de acceso al archivo de registro que describe el proceso de creación de la revisión y los errores. Para obtener más información, vea [valores devueltos para UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).

</dd> <dt>

<span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-la ruta de acceso LP**_al archivo de registro con datos de rendimiento_
</dt> <dd>

Opcional. Seguido de la ruta de acceso al archivo de registro que describe el proceso de creación de la revisión y los errores. Esta opción escribe los datos de rendimiento en el archivo de registro. Esta opción requiere la versión 4,0 de Patchwiz.dll.

</dd> <dt>

<span id="-d"></span><span id="-D"></span>**-d**
</dt> <dd>

Opcional. Muestra un cuadro de diálogo si la creación de la revisión se completa correctamente.

</dd> <dt>

<span id="-_"></span>**-?**
</dt> <dd>

Muestra la ayuda de la línea de comandos.

</dd> </dl>

> [!Note]
> Se puede producir un error en Msimsp.exe cuando llama a Makecab.exe si hay valores en la columna de archivo de la [tabla de archivos](file-table.md) del paquete de instalación que solo difieren en mayúsculas y minúsculas. Windows Installer distingue entre mayúsculas y minúsculas y permite un paquete de instalación como en la tabla siguiente solo cuando Comp1 y Comp2 se instalan en directorios diferentes. Sin embargo, en este escenario no puede usar Msimsp.exe o [Patchwiz.dll](patchwiz-dll.md) para generar una revisión para el paquete, ya que Msimsp.exe y Patchwiz.dll llaman a Makecab.exe, que no distingue entre mayúsculas y minúsculas.
> 
> Evite la creación de un paquete de instalación como la siguiente [tabla de archivos](file-table.md)parciales.
> 
> | Archivo       | Componente\_ | FileName   |
> |------------|-------------|------------|
> | readme.txt | Comp1       | readme.txt |
> | ReadMe.txt | Comp2       | readme.txt |


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear un paquete de revisión](creating-a-patch-package.md)
</dt> <dt>

[Un pequeño ejemplo de revisión de actualización](a-small-update-patching-example.md)
</dt> <dt>

[Herramientas de desarrollo de Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



