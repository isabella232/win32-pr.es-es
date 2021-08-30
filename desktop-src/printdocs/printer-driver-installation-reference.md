---
description: Las funciones de esta sección instalan y configuran controladores de impresora en un equipo.
ms.assetid: e6aa8963-aa1a-4313-bc24-2aeb4f4b93c4
title: Referencia de instalación del controlador de impresora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 627785e4b6b01302358aedb2dc3527949cb688f3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470741"
---
# <a name="printer-driver-installation-reference"></a>Referencia de instalación del controlador de impresora

Las funciones de esta sección instalan y configuran controladores de impresora en un equipo.

## <a name="in-this-section"></a>En esta sección




| Función | Descripción | 
|----------|-------------|
| <a href="addmonitor.md"><strong>AddMonitor</strong></a><br /> | La <a href="/windows/desktop/printdocs/addmonitor"><strong>función AddMonitor</strong></a> instala un monitor de puerto local y vincula los archivos de configuración, datos y supervisión.<br /> | 
| <a href="addport.md"><strong>AddPort</strong></a><br /> | La <a href="/windows/desktop/printdocs/addport"><strong>función AddPort</strong></a> agrega el nombre de un puerto a la lista de puertos admitidos. El monitor de puerto exporta la función <strong>AddPort.</strong><br /> | 
| <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a><br /> | La <a href="/windows/desktop/printdocs/addprinterdriver"><strong>función AddPrinterDriver</strong></a> instala un controlador de impresora local o remoto y asocia los archivos de configuración, datos y controladores.<br /> Para mayor flexibilidad en la instalación o actualización de controladores de impresora, use la función <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a> porque permite una actualización estricta, una degradación estricta, la copia solo de archivos más recientes y la copia de todos los archivos (independientemente de las marcas de tiempo de archivo).<br /><blockquote>[!Note]<br />Ya no se recomienda instalar un controlador de impresora sin un paquete de controladores. Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage en su</strong></a> lugar.</blockquote><br /> | 
| <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a><br /> | La <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>función AddPrinterDriverEx</strong></a> instala un controlador de impresora local o remoto y vincula los archivos de configuración, datos y controlador. Además de tener las funcionalidades de <a href="addprinterdriver.md"><strong>AddPrinterDriver,</strong></a>también tiene opciones que permiten una actualización estricta, una degradación estricta, la copia solo de archivos más recientes y la copia de todos los archivos (independientemente de las marcas de tiempo de los archivos).<br /><blockquote>[!Note]<br />Ya no se recomienda instalar un controlador de impresora sin un paquete de controladores. Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage en su</strong></a> lugar.</blockquote><br /> | 
| <a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a><br /> | La <a href="/windows/desktop/printdocs/addprintprocessor"><strong>función AddPrintProcessor</strong></a> instala un procesador de impresión en el servidor especificado y agrega el nombre del procesador de impresión a la lista de procesadores de impresión admitidos.<br /> | 
| <a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a><br /> | La <a href="/windows/desktop/printdocs/addprintprovidor"><strong>función AddPrintProvidor</strong></a> instala un proveedor de impresión local y vincula los archivos de configuración, datos y proveedor.<br /> | 
| <a href="coreprinterdriverinstalled.md"><strong>CorePrinterDriverInstalled</strong></a><br /> | La <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>función CorePrinterDriverInstalled</strong></a> informa de si está instalado un controlador de impresora principal con un GUID, una fecha y una versión especificados.<br /> | 
| <a href="deletemonitor.md"><strong>DeleteMonitor</strong></a><br /> | La <a href="/windows/desktop/printdocs/deletemonitor"><strong>función DeleteMonitor</strong></a> quita un monitor de puerto agregado por <a href="addmonitor.md"><strong>la función AddMonitor.</strong></a><br /> | 
| <a href="deleteport.md"><strong>DeletePort</strong></a><br /> | La <a href="/windows/desktop/printdocs/deleteport"><strong>función DeletePort</strong></a> muestra un cuadro de diálogo que permite al usuario eliminar un nombre de puerto.<br /> | 
| <a href="deleteprinterdriver.md"><strong>DeletePrinterDriver</strong></a><br /> | La <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>función DeletePrinterDriver</strong></a> quita el nombre de controlador de impresora especificado de la lista de nombres de controladores admitidos en un servidor.<br /> Para eliminar los archivos asociados al controlador, además de quitar el nombre de controlador de impresora especificado de la lista de nombres de controladores admitidos para un servidor, use la <a href="deleteprinterdriverex.md"><strong>función DeletePrinterDriverEx.</strong></a><br /><a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver elimina</strong></a> un controlador solo si no hay ninguna versión del controlador en uso para el entorno especificado. <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx puede</strong></a> eliminar versiones específicas del controlador.<br /> | 
| <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a><br /> | La <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>función DeletePrinterDriverEx</strong></a> quita el nombre de controlador de impresora especificado de la lista de nombres de controladores admitidos en un servidor y elimina los archivos asociados al controlador. Esta función también puede eliminar versiones específicas del controlador.<br /> | 
| <a href="deleteprinterdriverpackage.md"><strong>DeletePrinterDriverPackage</strong></a><br /> | Elimina un paquete de controladores de impresora del almacén de controladores.<br /> | 
| <a href="deleteprintprocessor.md"><strong>DeletePrintProcessor</strong></a><br /> | La <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>función DeletePrintProcessor</strong></a> quita un procesador de impresión agregado por <a href="addprintprocessor.md"><strong>la función AddPrintProcessor.</strong></a><br /> | 
| <a href="deleteprintprovidor.md"><strong>DeletePrintProvidor</strong></a><br /> | La <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>función DeletePrintProvidor</strong></a> quita un proveedor de impresión agregado por <a href="addprintprovidor.md"><strong>la función AddPrintProvidor.</strong></a><br /> | 
| <a href="enummonitors.md"><strong>EnumMonitors</strong></a><br /> | La <a href="/windows/desktop/printdocs/enummonitors"><strong>función EnumMonitors</strong></a> recupera información sobre los monitores de puerto instalados en el servidor especificado.<br /> | 
| <a href="enumports.md"><strong>EnumPorts</strong></a><br /> | La <a href="/windows/desktop/printdocs/enumports"><strong>función EnumPorts</strong></a> enumera los puertos que están disponibles para imprimirse en un servidor especificado.<br /> | 
| <a href="enumprinterdrivers.md"><strong>EnumPrinterDrivers</strong></a><br /> | La <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>función EnumPrinterDrivers</strong></a> enumera los controladores de impresora instalados en un servidor de impresora especificado.<br /> | 
| <a href="enumprintprocessordatatypes.md"><strong>EnumPrintProcessorDatatypes</strong></a><br /> | La <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>función EnumPrintProcessorDatatypes</strong></a> enumera los tipos de datos que admite un procesador de impresión especificado.<br /> | 
| <a href="enumprintprocessors.md"><strong>EnumPrintProcessors</strong></a><br /> | La <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>función EnumPrintProcessors</strong></a> enumera los procesadores de impresión instalados en el servidor especificado.<br /> | 
| <a href="getcoreprinterdrivers.md"><strong>GetCorePrinterDrivers</strong></a><br /> | Recupera el GUID, la versión y la fecha de los controladores de impresora principales especificados y la ruta de acceso a sus paquetes.<br /> | 
| <a href="getprinterdriver.md"><strong>GetPrinterDriver</strong></a><br /> | La <a href="/windows/desktop/printdocs/getprinterdriver"><strong>función GetPrinterDriver</strong></a> recupera los datos del controlador de la impresora especificada. Si el controlador no está instalado en el equipo local, <strong>GetPrinterDriver</strong> lo instala.<br /> | 
| <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a><br /> | La <a href="getprinterdriver2.md"><strong>función GetPrinterDriver2</strong></a> recupera los datos del controlador de la impresora especificada. Si el controlador no está instalado en el equipo local, <strong>GetPrinterDriver2</strong> lo instala y muestra cualquier interfaz de usuario en la ventana especificada.<br /> | 
| <a href="getprinterdriverdirectory.md"><strong>GetPrinterDriverDirectory</strong></a><br /> | La <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>función GetPrinterDriverDirectory</strong></a> recupera la ruta de acceso del directorio printer-driver.<br /> | 
| <a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a><br /> | Recupera la ruta de acceso al paquete de controladores de impresora especificado en un servidor de impresión.<br /> | 
| <a href="getprintprocessordirectory.md"><strong>GetPrintProcessorDirectory</strong></a><br /> | La <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>función GetPrintProcessorDirectory</strong></a> recupera la ruta de acceso al directorio del procesador de impresión en el servidor especificado.<br /> | 
| <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a><br /> | Instala un controlador de impresora desde un paquete de controladores que se encuentra en el almacén de controladores del servidor de impresión.<br /> | 
| <a href="uploadprinterdriverpackage.md"><strong>UploadPrinterDriverPackage</strong></a><br /> | Carga un controlador de impresora en el almacén de controladores del servidor de impresión para que se pueda instalar mediante una llamada a <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a>.<br /> | 




 

 

