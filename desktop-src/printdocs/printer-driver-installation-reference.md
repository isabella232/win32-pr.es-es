---
description: Las funciones de esta sección instalan y configuran controladores de impresora en un equipo.
ms.assetid: e6aa8963-aa1a-4313-bc24-2aeb4f4b93c4
title: Referencia de instalación del controlador de impresora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1613725ec5c7e2dbb06710bff706ec5aa7e32dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716337"
---
# <a name="printer-driver-installation-reference"></a>Referencia de instalación del controlador de impresora

Las funciones de esta sección instalan y configuran controladores de impresora en un equipo.

## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Función</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="addmonitor.md"><strong>AddMonitor</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/addmonitor"><strong>AddMonitor</strong></a> instala un monitor de puerto local y vincula los archivos de configuración, datos y supervisión.<br/></td>
</tr>
<tr class="even">
<td><a href="addport.md"><strong>AddPort</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/addport"><strong>AddPort</strong></a> agrega el nombre de un puerto a la lista de puertos admitidos. El monitor de Puerto exporta la función <strong>AddPort</strong> .<br/></td>
</tr>
<tr class="odd">
<td><a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/addprinterdriver"><strong>AddPrinterDriver</strong></a> instala un controlador de impresora local o remoto y asocia los archivos de configuración, datos y controlador.<br/> Para obtener más flexibilidad a la hora de instalar o actualizar controladores de impresora, use la función <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a> porque permite una actualización estricta, una degradación estricta, la copia de archivos más recientes solamente y la copia de todos los archivos (independientemente de las marcas de tiempo de archivo).<br/>
<blockquote>
[!Note]<br />
Ya no se recomienda instalar un controlador de impresora sin un paquete de controladores. Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> en su lugar.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>AddPrinterDriverEx</strong></a> instala un controlador de impresora local o remota y vincula los archivos de configuración, datos y controlador. Además de tener las funcionalidades de <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a>, también tiene opciones que permiten una actualización estricta, una degradación estricta, la copia de archivos más recientes solamente y la copia de todos los archivos (independientemente de las marcas de tiempo de archivo).<br/>
<blockquote>
[!Note]<br />
Ya no se recomienda instalar un controlador de impresora sin un paquete de controladores. Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> en su lugar.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/addprintprocessor"><strong>AddPrintProcessor</strong></a> instala un procesador de impresión en el servidor especificado y agrega el nombre del procesador de impresión a la lista de procesadores de impresión admitidos.<br/></td>
</tr>
<tr class="even">
<td><a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/addprintprovidor"><strong>AddPrintProvidor</strong></a> instala un proveedor de impresión local y vincula los archivos de configuración, datos y proveedor.<br/></td>
</tr>
<tr class="odd">
<td><a href="coreprinterdriverinstalled.md"><strong>CorePrinterDriverInstalled</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>CorePrinterDriverInstalled</strong></a> notifica si está instalado un controlador de impresora principal con un GUID, una fecha y una versión especificados.<br/></td>
</tr>
<tr class="even">
<td><a href="deletemonitor.md"><strong>DeleteMonitor</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/deletemonitor"><strong>DeleteMonitor</strong></a> quita un monitor de Puerto agregado por la función <a href="addmonitor.md"><strong>AddMonitor</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="deleteport.md"><strong>DeletePort</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/deleteport"><strong>DeletePort</strong></a> muestra un cuadro de diálogo que permite al usuario eliminar un nombre de puerto.<br/></td>
</tr>
<tr class="even">
<td><a href="deleteprinterdriver.md"><strong>DeletePrinterDriver</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> quita el nombre del controlador de impresora especificado de la lista de nombres de los controladores admitidos en un servidor.<br/> Para eliminar los archivos asociados al controlador además de quitar el nombre del controlador de impresora especificado de la lista de nombres de los controladores admitidos para un servidor, utilice la función <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> .<br/> <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> elimina un controlador solo si no se está usando ninguna versión del controlador para el entorno especificado. <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> puede eliminar versiones específicas del controlador.<br/></td>
</tr>
<tr class="odd">
<td><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>DeletePrinterDriverEx</strong></a> quita el nombre del controlador de impresora especificado de la lista de nombres de los controladores admitidos en un servidor y elimina los archivos asociados con el controlador. Esta función también puede eliminar versiones específicas del controlador.<br/></td>
</tr>
<tr class="even">
<td><a href="deleteprinterdriverpackage.md"><strong>DeletePrinterDriverPackage</strong></a><br/></td>
<td>Elimina un paquete de controladores de impresora del almacén de controladores.<br/></td>
</tr>
<tr class="odd">
<td><a href="deleteprintprocessor.md"><strong>DeletePrintProcessor</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>DeletePrintProcessor</strong></a> quita un procesador de impresión agregado por la función <a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="deleteprintprovidor.md"><strong>DeletePrintProvidor</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>DeletePrintProvidor</strong></a> quita un proveedor de impresión agregado por la función <a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="enummonitors.md"><strong>EnumMonitors</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/enummonitors"><strong>EnumMonitors</strong></a> recupera información acerca de los monitores de Puerto instalados en el servidor especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="enumports.md"><strong>EnumPorts</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/enumports"><strong>EnumPorts</strong></a> enumera los puertos que están disponibles para imprimir en un servidor especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="enumprinterdrivers.md"><strong>EnumPrinterDrivers</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>EnumPrinterDrivers</strong></a> enumera los controladores de impresora instalados en un servidor de impresión especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="enumprintprocessordatatypes.md"><strong>EnumPrintProcessorDatatypes</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>EnumPrintProcessorDatatypes</strong></a> enumera los tipos de datos que admite un procesador de impresión especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="enumprintprocessors.md"><strong>EnumPrintProcessors</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>EnumPrintProcessors</strong></a> enumera los procesadores de impresión instalados en el servidor especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="getcoreprinterdrivers.md"><strong>GetCorePrinterDrivers</strong></a><br/></td>
<td>Recupera el GUID, la versión y la fecha de los controladores de impresora principales especificados y la ruta de acceso a sus paquetes.<br/></td>
</tr>
<tr class="odd">
<td><a href="getprinterdriver.md"><strong>GetPrinterDriver</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/getprinterdriver"><strong>GetPrinterDriver</strong></a> recupera los datos del controlador de la impresora especificada. Si el controlador no está instalado en el equipo local, <strong>GetPrinterDriver</strong> lo instala.<br/></td>
</tr>
<tr class="even">
<td><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a><br/></td>
<td>La función <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> recupera los datos del controlador de la impresora especificada. Si el controlador no está instalado en el equipo local, <strong>GetPrinterDriver2</strong> lo instala y muestra cualquier interfaz de usuario en la ventana especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="getprinterdriverdirectory.md"><strong>GetPrinterDriverDirectory</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>GetPrinterDriverDirectory</strong></a> recupera la ruta de acceso del directorio del controlador de impresora.<br/></td>
</tr>
<tr class="even">
<td><a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a><br/></td>
<td>Recupera la ruta de acceso al paquete de controladores de impresora especificado en un servidor de impresión.<br/></td>
</tr>
<tr class="odd">
<td><a href="getprintprocessordirectory.md"><strong>GetPrintProcessorDirectory</strong></a><br/></td>
<td>La función <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>GetPrintProcessorDirectory</strong></a> recupera la ruta de acceso al directorio del procesador de impresión en el servidor especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a><br/></td>
<td>Instala un controlador de impresora desde un paquete de controladores que se encuentra en el almacén de controladores del servidor de impresión.<br/></td>
</tr>
<tr class="odd">
<td><a href="uploadprinterdriverpackage.md"><strong>UploadPrinterDriverPackage</strong></a><br/></td>
<td>Carga un controlador de impresora en el almacén de controladores del servidor de impresión para que se pueda instalar llamando a <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

 

