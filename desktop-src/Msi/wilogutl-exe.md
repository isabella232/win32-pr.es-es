---
description: Wilogutl.exe ayuda al análisis de archivos de registro desde una instalación del instalador de Windows y muestra soluciones sugeridas a los errores que se encuentran en un archivo de registro.
ms.assetid: 09aa03ba-992f-47ab-999b-ebdfe85c1ea7
title: Wilogutl.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9958b91513dccc32f3bfc82ff781f65f166c208
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883856"
---
# <a name="wilogutlexe"></a>Wilogutl.exe

Wilogutl.exe ayuda al análisis de archivos de registro desde una instalación del instalador de Windows y muestra soluciones sugeridas a los errores que se encuentran en un archivo de registro.

No se muestran errores no críticos. Wilogutl.exe se puede ejecutar en modo silencioso o con una interfaz de usuario (UI). La herramienta genera informes como archivos de texto tanto en la interfaz de usuario como en los modos silenciosos. Funciona mejor con archivos de registro Windows instalador detallado, pero también funciona con registros no detallados. Para obtener más información, vea [Registro](logging.md).

Esta herramienta solo está disponible en los componentes del [SDK Windows para los Windows instaladores de .](platform-sdk-components-for-windows-installer-developers.md)

## <a name="syntax"></a>Syntax

**wilogutl.exe** *\[ &lt; opciones de &gt; \] \[ <source file> \] \[ &lt; configuración &gt; \] \[ <report file directory> \]*

Puede usar las siguientes líneas de comandos para ejecutarse en modo silencioso.

**wilogutl /q /l** *c: \\ mymsilog.log* **/o** *c \\ outputdir \\*

**wilogutl /q /l** *c: \\ mymsilog.log*

## <a name="command-line-options"></a>Opciones de la línea de comandos

Wilogutl.exe usa las siguientes opciones de línea de comandos que no tienen en cuenta mayúsculas de minúsculas. Se puede usar un delimitador de guiones en lugar de una barra diagonal.



| Opción | Descripción                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ninguno   | Se ejecuta en modo de interfaz de usuario, sin opciones de línea de comandos.                                                                                                                                                   |
| /q     | Especifica el modo silencioso. Wilogutl.exe genera archivos de informe y no muestra una interfaz de usuario.                                                                                            |
| /l     | Especifica el nombre del archivo de registro que se va a analizar. Esta opción es necesaria cuando se usa el modo silencioso.                                                                                           |
| /o     | Especifica el directorio de salida para los archivos de informe. Esta ruta de acceso de salida solo se usa cuando se ejecuta en modo silencioso. Si la opción no está presente, los informes se colocarán en el directorio C: \\ WiLogResults. |



 

Cuando se ejecuta en modo de interfaz de usuario, Wilogutl.exe muestra los cuadros de diálogo siguientes.




| Nombre | Descripción | 
|------|-------------|
| Windows Analizador de registro detallado del instalador | El Windows de diálogo Analizador de registro detallado del instalador de registros permite a los usuarios seleccionar un archivo de registro para su análisis:<ul><li>El <strong>botón</strong> Abrir abre el archivo en Bloc de notas. El área de vista previa se puede usar para comprobar que se ha seleccionado el archivo de registro correcto.</li><li>El <strong>botón Analizar</strong> comienza el análisis de archivos de registro y muestra el cuadro de diálogo Vista detallada del archivo de registro.</li></ul> | 
| Vista detallada del archivo de registro | El cuadro de diálogo Vista detallada del archivo de registro muestra información de error registrada. Use los <strong>botones Atrás</strong> <strong>y</strong> Siguiente para navegar por varios errores. Para mostrar errores no críticos, active <strong>la casilla Mostrar errores de depuración omitido.</strong> Se muestra la versión del instalador en el equipo que se usa para ejecutar la instalación registrada. Si la instalación registrada se ha <strong></strong> ejecutado con permisos elevados, la <strong></strong> casilla Instalación con privilegios elevados está activada y se proporciona información en los cuadros de texto Detalles de privilegios del lado cliente y Detalles de <strong>privilegios</strong> del lado servidor. El cuadro de diálogo Vista detallada del archivo de registro contiene los siguientes botones:<br /><ul><li><strong>Estados:</strong> muestra el cuadro de diálogo Estados de características y componentes .</li><li><strong>Propiedades:</strong> muestra el cuadro de diálogo Propiedades.</li><li><strong>Directivas:</strong> muestra el cuadro de diálogo Directivas.</li><li><strong>Registro anotado en HTML:</strong> muestra el registro como archivo HTML anotado.</li><li><strong>Guardar resultados:</strong> guarde los archivos de informe en el directorio especificado.</li><li><strong>Ayuda del mensaje de error:</strong> mostrar la ayuda del mensaje de error del instalador.</li><li><strong>Ayuda:</strong> muestra ayuda para el analizador de registro Windows instalación del instalador.</li><li><strong>Cómo leer un archivo de registro:</strong> mostrar el documento de ayuda del archivo de registro.</li></ul> | 
| Estados de características y componentes | El <strong>cuadro de diálogo Estados de características</strong> y componentes muestra los estados de características y componentes:<ul><li>La <strong>columna</strong> Característica muestra el nombre de la característica en el paquete de instalación.</li><li>La <strong>columna</strong> Componente muestra el nombre del componente en el paquete de instalación.</li><li>La <strong>columna Instalado</strong> muestra el estado de la característica o componente al final de la instalación.</li><li>La <strong>columna</strong> Solicitud muestra la selección del usuario durante la instalación para el estado de la característica o componente.</li><li>La <strong>columna</strong> Acción muestra la acción realizada por el instalador para la característica o componente.</li></ul>Para obtener más información, <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>vea MsiGetComponentState</strong></a> y <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState.</strong></a><br /> | 
| Propiedades | El cuadro de diálogo Propiedades Windows Propiedades <a href="properties.md">del instalador</a> y sus valores al final de la instalación. Puede ordenar las propiedades por nombre o por valor:<ul><li>La <strong>pestaña</strong> Cliente muestra las propiedades y los valores durante la parte del lado cliente de la instalación.</li><li>La <strong>pestaña</strong> Servidor muestra las propiedades y los valores durante la parte del servidor de la instalación.</li><li>La <strong>pestaña Nested</strong> (Anidado) muestra las propiedades y los valores de cualquier instalación <a href="concurrent-installations.md">simultánea.</a></li></ul> | 
| Directivas | El cuadro de diálogo Directivas muestra el <a href="system-policy.md">conjunto de directivas del</a> sistema después de la instalación:<ul><li>Un valor de 0 (cero) establecido para la directiva significa que la directiva no está habilitada.</li><li>Un valor de 1 (uno) significa que la directiva está habilitada.</li><li>Un valor de ? (signo de interrogación) significa que el valor de la directiva no se registra en el registro.</li></ul>Si necesita un valor de directiva que no esté en el registro, pruebe a usar Regedit.exe para comprobar las claves del Registro en el equipo que no se puede instalar.<br /> | 




 

## <a name="report-files"></a>Archivos de informe

Al realizar un análisis en  modo silencioso o hacer clic en el botón Guardar resultados del cuadro de diálogo **Vista** detallada del archivo de registro, la herramienta Analizador de instalación del instalador de Windows genera tres archivos de texto y un archivo de registro anotado HTML.

En la tabla siguiente se identifican los nombres y el contenido de los archivos de informe.



| Nombre                      | Descripción                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| logfilename \_summary.txt  | Resume el archivo de registro. Muestra la información que muestra el cuadro de diálogo Vista detallada del archivo de registro y el primer error.         |
| logfilename \_errors.txt   | Identifica el número de errores, los errores y las soluciones recomendadas. En este archivo se enumeran los errores críticos y no críticos. |
| logfilename \_policies.txt | Identifica los nombres y valores de directiva establecidos al final de la instalación como en el cuadro de diálogo Directivas .                       |
| detalles \_logfilename.htm  | Un registro anotado en HTML con una leyenda para la codificación de colores.                                                                      |



 

## <a name="return-values"></a>Valores devueltos

Si se pasan argumentos de línea de comandos no válidos para las operaciones en modo silencioso, Wilogutl.exe no hace nada y el proceso devuelve uno de los valores de la tabla siguiente.



| Valor | Significado                                                                 |
|-------|-------------------------------------------------------------------------|
| 1     | Se especifica el directorio de salida no indicado.                                      |
| 2     | Se especifica un nombre de archivo de registro no bueno.                                         |
| 3     | Se ha pasado /q, pero falta el modificador /l necesario para el nombre del archivo de registro. |
| 4     | Se ha pasado /l, pero falta el modificador /q necesario para el modo silencioso.        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Versiones, herramientas y redistribuibles publicados](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Windows Herramientas de desarrollo del instalador](windows-installer-development-tools.md)
</dt> </dl>

 

 




