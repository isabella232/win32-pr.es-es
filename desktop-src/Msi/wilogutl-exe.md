---
description: Wilogutl.exe ayuda a analizar los archivos de registro desde una instalación de Windows Installer y muestra soluciones sugeridas a los errores que se encuentran en un archivo de registro.
ms.assetid: 09aa03ba-992f-47ab-999b-ebdfe85c1ea7
title: Wilogutl.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec81c3c82299a08fd947fbbecc7afd8a373252b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678586"
---
# <a name="wilogutlexe"></a>Wilogutl.exe

Wilogutl.exe ayuda a analizar los archivos de registro desde una instalación de Windows Installer y muestra soluciones sugeridas a los errores que se encuentran en un archivo de registro.

No se muestran los errores no críticos. Wilogutl.exe puede ejecutarse en modo silencioso o con una interfaz de usuario (UI). La herramienta genera informes como archivos de texto en los modos de interfaz de usuario y de modo silencioso. Funciona mejor con los archivos de registro detallados de Windows Installer, pero también funciona con registros no detallados. Para obtener más información, vea [Registro](logging.md).

Esta herramienta solo está disponible en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="syntax"></a>Sintaxis

**wilogutl.exe***\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*

Puede usar las siguientes líneas de comandos para ejecutarse en modo silencioso.

**wilogutl/q/l** *c: \\ mymsilog. log* **/o** *c \\ outputDir \\*

**wilogutl/q/l** *c: \\ mymsilog. log*

## <a name="command-line-options"></a>Opciones de la línea de comandos

Wilogutl.exe usa las siguientes opciones de línea de comandos que no distinguen mayúsculas de minúsculas. Se puede usar un delimitador de guiones en lugar de una barra diagonal.



| Opción | Descripción                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ninguno   | Se ejecuta en modo de interfaz de usuario, sin opciones de línea de comandos.                                                                                                                                                   |
| /q     | Especifica el modo silencioso. Wilogutl.exe genera archivos de informe y no muestra ninguna interfaz de usuario.                                                                                            |
| /l     | Especifica el nombre del archivo de registro que se va a analizar. Esta opción es necesaria cuando se usa el modo silencioso.                                                                                           |
| /o     | Especifica el directorio de salida para los archivos de informe. Esta ruta de acceso de salida solo se usa cuando se ejecuta en modo silencioso. Si la opción no está presente, los informes se colocan en el \\ directorio C: WiLogResults |



 

Cuando se ejecuta en modo de interfaz de usuario, Wilogutl.exe muestra los siguientes cuadros de diálogo.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nombre</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Analizador de registros detallado Windows Installer</td>
<td>El cuadro de diálogo Windows Installer analizador de registros detallado permite a los usuarios seleccionar un archivo de registro para su análisis:
<ul>
<li>El botón <strong>abrir</strong> abre el archivo en el Bloc de notas. El área de vista previa se puede usar para comprobar que se ha seleccionado el archivo de registro correcto.</li>
<li>El botón <strong>analizar</strong> inicia el análisis del archivo de registro y muestra el cuadro de diálogo vista de archivo de registro detallada.</li>
</ul></td>
</tr>
<tr class="even">
<td>Vista detallada del archivo de registro</td>
<td>En el cuadro de diálogo vista de archivo de registro detallada se muestra la información de error registrada. Use los botones <strong>atrás</strong> y <strong>siguiente</strong> para navegar por varios errores. Para mostrar los errores no críticos, active la casilla <strong>Mostrar errores de depuración omitidos</strong> . Se muestra la versión del instalador en el equipo que se usa para ejecutar la instalación registrada. Si la instalación registrada se ejecutó con permisos elevados, la casilla de <strong>instalación</strong> con privilegios elevados está activada y se proporciona información en los cuadros de texto <strong>detalles de privilegios</strong> del lado del cliente y detalles de los <strong>privilegios del servidor</strong> . El cuadro de diálogo vista de archivo de registro detallado contiene los siguientes botones:<br/>
<ul>
<li><strong>Estados</strong> - de Muestra el cuadro de diálogo Estados de características y componentes.</li>
<li><strong>Propiedades</strong> - de Mostrar el cuadro de diálogo Propiedades.</li>
<li><strong>Directivas</strong> - de Muestra el cuadro de diálogo directivas.</li>
<li>Registro anotado <strong>HTML</strong> - Muestra el registro como archivo HTML anotado.</li>
<li><strong>Guardar resultados</strong> - Guardar archivos de informe en el directorio especificado.</li>
<li>Ayuda del mensaje de <strong>error</strong> - Muestra la ayuda del mensaje de error del instalador.</li>
<li><strong>Ayuda</strong> - de Mostrar ayuda para Windows Installer el analizador de registros de instalación.</li>
<li><strong>Cómo leer un archivo</strong> - de registro Muestra el documento de ayuda del archivo de registro.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Estados de características y componentes</td>
<td>El cuadro de diálogo Estados de características <strong>y</strong> componentes muestra los Estados de características y componentes:
<ul>
<li>La columna <strong>característica</strong> muestra el nombre de la característica en el paquete de instalación.</li>
<li>La columna <strong>componente</strong> muestra el nombre del componente en el paquete de instalación.</li>
<li>La columna <strong>instalado</strong> muestra la característica o el estado del componente al final de la instalación.</li>
<li>La columna <strong>solicitud</strong> muestra la selección del usuario durante la instalación del estado de la característica o del componente.</li>
<li>La columna <strong>acción</strong> muestra la acción realizada por el instalador para la característica o componente.</li>
</ul>
Para obtener más información, vea <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> y <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>.<br/></td>
</tr>
<tr class="even">
<td>Propiedades</td>
<td>El cuadro de diálogo Propiedades muestra Windows Installer <a href="properties.md">propiedades</a> y sus valores al final de la instalación. Puede ordenar las propiedades por nombre o por valor:
<ul>
<li>La pestaña <strong>cliente</strong> muestra propiedades y valores durante la parte del cliente de la instalación.</li>
<li>En la pestaña <strong>servidor</strong> se muestran las propiedades y los valores durante la parte de servidor de la instalación.</li>
<li>En la pestaña <strong>anidado</strong> se muestran las propiedades y los valores de las <a href="concurrent-installations.md">instalaciones simultáneas</a>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Directivas</td>
<td>En el cuadro de diálogo directivas se muestra el conjunto de <a href="system-policy.md">directivas del sistema</a> después de la instalación:
<ul>
<li>Un valor de 0 (cero) establecido para la directiva significa que la Directiva no está habilitada.</li>
<li>Un valor de 1 (uno) significa que la Directiva está habilitada.</li>
<li>Un valor de? (signo de interrogación) significa que el valor de la Directiva no se registra en el registro.</li>
</ul>
Si necesita un valor de directiva que no esté en el registro, pruebe a usar Regedit.exe para comprobar las claves del registro en el equipo que no se puede realizar la instalación.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="report-files"></a>Archivos de informe

Al realizar un análisis de modo silencioso o al hacer clic en el botón **Guardar resultados** en el cuadro de diálogo **vista detallada del archivo de registro** , la herramienta analizador de instalación de Windows Installer genera tres archivos de texto y un archivo de registro anotado en HTML.

En la tabla siguiente se identifican los nombres y el contenido de los archivos de informe.



| Nombre                      | Descripción                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| nombreDeArchivoDeRegistro \_summary.txt  | Resume el archivo de registro. Muestra la información que se muestra en el cuadro de diálogo vista de archivo de registro detallada y el primer error.         |
| nombreDeArchivoDeRegistro \_errors.txt   | Identifica el número de errores, los errores y las soluciones recomendadas. En este archivo se enumeran los errores críticos y no críticos. |
| nombreDeArchivoDeRegistro \_policies.txt | Identifica los nombres de directiva y los valores establecidos al final de la instalación, como en el cuadro de diálogo directivas.                       |
| detalles \_logfilename.htm  | Un registro anotado en HTML con una leyenda para la codificación de colores.                                                                      |



 

## <a name="return-values"></a>Valores devueltos

Si se pasan argumentos de línea de comandos no válidos para las operaciones de modo silencioso, Wilogutl.exe no hace nada y el proceso devuelve uno de los valores de la tabla siguiente.



| Value | Significado                                                                 |
|-------|-------------------------------------------------------------------------|
| 1     | Se ha especificado un directorio de salida incorrecto.                                      |
| 2     | Se ha especificado un nombre de archivo de registro incorrecto.                                         |
| 3     | Se pasó/q, pero falta el modificador/l necesario para el nombre del archivo de registro. |
| 4     | Se pasó/l, pero falta el modificador "/q" necesario para el modo silencioso.        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Herramientas de desarrollo de Windows Installer](windows-installer-development-tools.md)
</dt> </dl>

 

 




