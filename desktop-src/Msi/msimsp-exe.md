---
description: El método recomendado para generar un paquete de revisión es usar herramientas de creación de revisiones como Msimsp.exe y Patchwiz.dll. La herramienta Msimsp.exe solo está disponible en los componentes del SDK de Windows para Windows instaladores.
ms.assetid: fa8e9d68-3db1-4d17-aa99-2ca0ed421c7a
title: Msimsp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1810fd0c544695742273bbb0e63b22138529c129
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074375"
---
# <a name="msimspexe"></a>Msimsp.exe

El método recomendado para generar un paquete de revisión es usar herramientas de creación de revisiones como Msimsp.exe y [Patchwiz.dll](patchwiz-dll.md). La herramienta Msimsp.exe solo está disponible en los componentes del SDK de Windows [para Windows programadores del instalador](platform-sdk-components-for-windows-installer-developers.md).

Msimsp.exe es un archivo ejecutable que llama a [Patchwiz.dll](patchwiz-dll.md). La herramienta se puede usar para crear un paquete de revisión pasando la ruta de acceso a un archivo de propiedades de creación de revisiones (archivo .csv) y la ruta de acceso al paquete de revisión que se está creando. Msimsp.ex también se puede usar para crear un archivo de registro y para especificar una carpeta temporal en la que se guardan las transformaciones, los archivadores y los archivos que se usan para crear el paquete de revisión.

La sintaxis de línea de comandos Msimsp.exe es:

**Msimsp.exe -s** ruta de *\[ acceso \] al archivo .msp*  *\[ \]* -p ruta de acceso al archivo .msp **{options}**

Las opciones de la línea de comandos no distinguen mayúsculas de minúsculas y se pueden usar delimitadores de barra diagonal en lugar de un guión. Si no se especifica ninguna opción, Msimsp.exe muestra los valores actuales de las propiedades de información de resumen.

<dl> <dt>

<span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[ ruta de \] acceso al archivo .csv_
</dt> <dd>

Esto es necesario y debe ir seguido de la ruta de acceso al archivo de propiedades de creación de revisiones (extensión .csv). Para obtener más información, [ veaPatchWiz.dll](patchwiz-dll.md).

</dd> <dt>

<span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_ruta de acceso al archivo .msp_
</dt> <dd>

Esto es necesario y seguido de la ruta de acceso al paquete de revisión que se está creando (extensión .msp).

</dd> <dt>

<span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f ruta de**_acceso a la carpeta temporal_
</dt> <dd>

Opcional. Seguido de la ruta de acceso a la carpeta temporal. La ubicación predeterminada es %TMP% \\ ~pcw \_ tmp.tmp \\ .

</dd> <dt>

<span id="-k"></span><span id="-K"></span>**-k**
</dt> <dd>

Opcional. Se producirá un error si la carpeta temporal ya existe.

</dd> <dt>

<span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l ruta**_de acceso al archivo de registro_
</dt> <dd>

Opcional. Seguido de la ruta de acceso al archivo de registro que describe el proceso de creación de revisiones y los errores. Para obtener más información, vea [Valores devueltos para UiCreatePatchPackage.](return-values-for-uicreatepatchpackage.md)

</dd> <dt>

<span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-lp ruta de**_acceso al archivo de registro con datos de rendimiento_
</dt> <dd>

Opcional. Seguido de la ruta de acceso al archivo de registro que describe el proceso de creación de revisiones y los errores. Esta opción escribe datos de rendimiento en el archivo de registro. Esta opción requiere la versión 4.0 de Patchwiz.dll.

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
> Msimsp.exe puede producir un error cuando llama a Makecab.exe si hay [](file-table.md) valores en la columna Archivo de la tabla Archivo del paquete de instalación que solo difieren por mayúsculas y minúsculas. Windows El instalador distingue mayúsculas de minúsculas y permite un paquete de instalación, como en la tabla siguiente, solo cuando Comp1 y Comp2 se instalan en directorios diferentes. Sin [ embargo, ](patchwiz-dll.md) en este escenario no puede usar Msimsp.exe oPatchwiz.dllpara generar una revisión para el paquete, ya que Msimsp.exe y Patchwiz.dll llaman Makecab.exe, que no tiene en cuenta las mayúsculas y minúsculas.
> 
> Evite crear un paquete de instalación como la siguiente tabla [de archivos parcial.](file-table.md)
> 
> | Archivo       | Componente\_ | FileName   |
> |------------|-------------|------------|
> | readme.txt | Comp1       | readme.txt |
> | ReadMe.txt | Comp2       | readme.txt |


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear un paquete de revisión](creating-a-patch-package.md)
</dt> <dt>

[Ejemplo pequeño de aplicación de revisiones de actualizaciones](a-small-update-patching-example.md)
</dt> <dt>

[Windows Herramientas de desarrollo del instalador](windows-installer-development-tools.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



