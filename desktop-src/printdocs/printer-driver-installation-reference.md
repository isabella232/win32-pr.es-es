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
# <a name="printer-driver-installation-reference"></a><span data-ttu-id="805ef-103">Referencia de instalación del controlador de impresora</span><span class="sxs-lookup"><span data-stu-id="805ef-103">Printer Driver Installation Reference</span></span>

<span data-ttu-id="805ef-104">Las funciones de esta sección instalan y configuran controladores de impresora en un equipo.</span><span class="sxs-lookup"><span data-stu-id="805ef-104">The functions in this section install and configure printer drivers on a computer.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="805ef-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="805ef-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="805ef-106">Función</span><span class="sxs-lookup"><span data-stu-id="805ef-106">Function</span></span></th>
<th><span data-ttu-id="805ef-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="805ef-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="805ef-108"><a href="addmonitor.md"><strong>AddMonitor</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-108"><a href="addmonitor.md"><strong>AddMonitor</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-109">La función <a href="/windows/desktop/printdocs/addmonitor"><strong>AddMonitor</strong></a> instala un monitor de puerto local y vincula los archivos de configuración, datos y supervisión.</span><span class="sxs-lookup"><span data-stu-id="805ef-109">The <a href="/windows/desktop/printdocs/addmonitor"><strong>AddMonitor</strong></a> function installs a local port monitor and links the configuration, data, and monitor files.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="805ef-110"><a href="addport.md"><strong>AddPort</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-110"><a href="addport.md"><strong>AddPort</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-111">La función <a href="/windows/desktop/printdocs/addport"><strong>AddPort</strong></a> agrega el nombre de un puerto a la lista de puertos admitidos.</span><span class="sxs-lookup"><span data-stu-id="805ef-111">The <a href="/windows/desktop/printdocs/addport"><strong>AddPort</strong></a> function adds the name of a port to the list of supported ports.</span></span> <span data-ttu-id="805ef-112">El monitor de Puerto exporta la función <strong>AddPort</strong> .</span><span class="sxs-lookup"><span data-stu-id="805ef-112">The <strong>AddPort</strong> function is exported by the port monitor.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="805ef-113"><a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-113"><a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-114">La función <a href="/windows/desktop/printdocs/addprinterdriver"><strong>AddPrinterDriver</strong></a> instala un controlador de impresora local o remoto y asocia los archivos de configuración, datos y controlador.</span><span class="sxs-lookup"><span data-stu-id="805ef-114">The <a href="/windows/desktop/printdocs/addprinterdriver"><strong>AddPrinterDriver</strong></a> function installs a local or remote printer driver and associates the configuration, data, and driver files.</span></span><br/> <span data-ttu-id="805ef-115">Para obtener más flexibilidad a la hora de instalar o actualizar controladores de impresora, use la función <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a> porque permite una actualización estricta, una degradación estricta, la copia de archivos más recientes solamente y la copia de todos los archivos (independientemente de las marcas de tiempo de archivo).</span><span class="sxs-lookup"><span data-stu-id="805ef-115">For more flexibility in installing or upgrading printer drivers, use the <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a> function because it allows strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of the file time stamps).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="805ef-116">Ya no se recomienda instalar un controlador de impresora sin un paquete de controladores.</span><span class="sxs-lookup"><span data-stu-id="805ef-116">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="805ef-117">Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> en su lugar.</span><span class="sxs-lookup"><span data-stu-id="805ef-117">Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="805ef-118"><a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-118"><a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-119">La función <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>AddPrinterDriverEx</strong></a> instala un controlador de impresora local o remota y vincula los archivos de configuración, datos y controlador.</span><span class="sxs-lookup"><span data-stu-id="805ef-119">The <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>AddPrinterDriverEx</strong></a> function installs a local or remote printer driver and links the configuration, data, and driver files.</span></span> <span data-ttu-id="805ef-120">Además de tener las funcionalidades de <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a>, también tiene opciones que permiten una actualización estricta, una degradación estricta, la copia de archivos más recientes solamente y la copia de todos los archivos (independientemente de las marcas de tiempo de archivo).</span><span class="sxs-lookup"><span data-stu-id="805ef-120">Besides having the capabilities of <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a>, it also has options that permit strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of file time stamps).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="805ef-121">Ya no se recomienda instalar un controlador de impresora sin un paquete de controladores.</span><span class="sxs-lookup"><span data-stu-id="805ef-121">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="805ef-122">Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> en su lugar.</span><span class="sxs-lookup"><span data-stu-id="805ef-122">Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="805ef-123"><a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-123"><a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-124">La función <a href="/windows/desktop/printdocs/addprintprocessor"><strong>AddPrintProcessor</strong></a> instala un procesador de impresión en el servidor especificado y agrega el nombre del procesador de impresión a la lista de procesadores de impresión admitidos.</span><span class="sxs-lookup"><span data-stu-id="805ef-124">The <a href="/windows/desktop/printdocs/addprintprocessor"><strong>AddPrintProcessor</strong></a> function installs a print processor on the specified server and adds the print-processor name to the list of supported print processors.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="805ef-125"><a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-125"><a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-126">La función <a href="/windows/desktop/printdocs/addprintprovidor"><strong>AddPrintProvidor</strong></a> instala un proveedor de impresión local y vincula los archivos de configuración, datos y proveedor.</span><span class="sxs-lookup"><span data-stu-id="805ef-126">The <a href="/windows/desktop/printdocs/addprintprovidor"><strong>AddPrintProvidor</strong></a> function installs a local print provider and links the configuration, data, and provider files.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="805ef-127"><a href="coreprinterdriverinstalled.md"><strong>CorePrinterDriverInstalled</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-127"><a href="coreprinterdriverinstalled.md"><strong>CorePrinterDriverInstalled</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-128">La función <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>CorePrinterDriverInstalled</strong></a> notifica si está instalado un controlador de impresora principal con un GUID, una fecha y una versión especificados.</span><span class="sxs-lookup"><span data-stu-id="805ef-128">The <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>CorePrinterDriverInstalled</strong></a> function reports whether a core printer driver with a specified GUID, date, and version is installed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="805ef-129"><a href="deletemonitor.md"><strong>DeleteMonitor</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-129"><a href="deletemonitor.md"><strong>DeleteMonitor</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-130">La función <a href="/windows/desktop/printdocs/deletemonitor"><strong>DeleteMonitor</strong></a> quita un monitor de Puerto agregado por la función <a href="addmonitor.md"><strong>AddMonitor</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="805ef-130">The <a href="/windows/desktop/printdocs/deletemonitor"><strong>DeleteMonitor</strong></a> function removes a port monitor added by the <a href="addmonitor.md"><strong>AddMonitor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="805ef-131"><a href="deleteport.md"><strong>DeletePort</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-131"><a href="deleteport.md"><strong>DeletePort</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-132">La función <a href="/windows/desktop/printdocs/deleteport"><strong>DeletePort</strong></a> muestra un cuadro de diálogo que permite al usuario eliminar un nombre de puerto.</span><span class="sxs-lookup"><span data-stu-id="805ef-132">The <a href="/windows/desktop/printdocs/deleteport"><strong>DeletePort</strong></a> function displays a dialog box that allows the user to delete a port name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="805ef-133"><a href="deleteprinterdriver.md"><strong>DeletePrinterDriver</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-133"><a href="deleteprinterdriver.md"><strong>DeletePrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-134">La función <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> quita el nombre del controlador de impresora especificado de la lista de nombres de los controladores admitidos en un servidor.</span><span class="sxs-lookup"><span data-stu-id="805ef-134">The <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> function removes the specified printer-driver name from the list of names of supported drivers on a server.</span></span><br/> <span data-ttu-id="805ef-135">Para eliminar los archivos asociados al controlador además de quitar el nombre del controlador de impresora especificado de la lista de nombres de los controladores admitidos para un servidor, utilice la función <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="805ef-135">To delete the files associated with the driver in addition to removing the specified printer-driver name from the list of names of supported drivers for a server, use the <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> function.</span></span><br/> <span data-ttu-id="805ef-136"><a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> elimina un controlador solo si no se está usando ninguna versión del controlador para el entorno especificado.</span><span class="sxs-lookup"><span data-stu-id="805ef-136"><a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> deletes a driver only if no version of the driver is in use for the specified environment.</span></span> <span data-ttu-id="805ef-137"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> puede eliminar versiones específicas del controlador.</span><span class="sxs-lookup"><span data-stu-id="805ef-137"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> can delete specific versions of the driver.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="805ef-138"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-138"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-139">La función <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>DeletePrinterDriverEx</strong></a> quita el nombre del controlador de impresora especificado de la lista de nombres de los controladores admitidos en un servidor y elimina los archivos asociados con el controlador.</span><span class="sxs-lookup"><span data-stu-id="805ef-139">The <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>DeletePrinterDriverEx</strong></a> function removes the specified printer-driver name from the list of names of supported drivers on a server and deletes the files associated with the driver.</span></span> <span data-ttu-id="805ef-140">Esta función también puede eliminar versiones específicas del controlador.</span><span class="sxs-lookup"><span data-stu-id="805ef-140">This function can also delete specific versions of the driver.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="805ef-141"><a href="deleteprinterdriverpackage.md"><strong>DeletePrinterDriverPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-141"><a href="deleteprinterdriverpackage.md"><strong>DeletePrinterDriverPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-142">Elimina un paquete de controladores de impresora del almacén de controladores.</span><span class="sxs-lookup"><span data-stu-id="805ef-142">Deletes a printer driver package from the driver store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="805ef-143"><a href="deleteprintprocessor.md"><strong>DeletePrintProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-143"><a href="deleteprintprocessor.md"><strong>DeletePrintProcessor</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-144">La función <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>DeletePrintProcessor</strong></a> quita un procesador de impresión agregado por la función <a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="805ef-144">The <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>DeletePrintProcessor</strong></a> function removes a print processor added by the <a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="805ef-145"><a href="deleteprintprovidor.md"><strong>DeletePrintProvidor</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-145"><a href="deleteprintprovidor.md"><strong>DeletePrintProvidor</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-146">La función <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>DeletePrintProvidor</strong></a> quita un proveedor de impresión agregado por la función <a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="805ef-146">The <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>DeletePrintProvidor</strong></a> function removes a print provider added by the <a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="805ef-147"><a href="enummonitors.md"><strong>EnumMonitors</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-147"><a href="enummonitors.md"><strong>EnumMonitors</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-148">La función <a href="/windows/desktop/printdocs/enummonitors"><strong>EnumMonitors</strong></a> recupera información acerca de los monitores de Puerto instalados en el servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="805ef-148">The <a href="/windows/desktop/printdocs/enummonitors"><strong>EnumMonitors</strong></a> function retrieves information about the port monitors installed on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="805ef-149"><a href="enumports.md"><strong>EnumPorts</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-149"><a href="enumports.md"><strong>EnumPorts</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-150">La función <a href="/windows/desktop/printdocs/enumports"><strong>EnumPorts</strong></a> enumera los puertos que están disponibles para imprimir en un servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="805ef-150">The <a href="/windows/desktop/printdocs/enumports"><strong>EnumPorts</strong></a> function enumerates the ports that are available for printing on a specified server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="805ef-151"><a href="enumprinterdrivers.md"><strong>EnumPrinterDrivers</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-151"><a href="enumprinterdrivers.md"><strong>EnumPrinterDrivers</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-152">La función <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>EnumPrinterDrivers</strong></a> enumera los controladores de impresora instalados en un servidor de impresión especificado.</span><span class="sxs-lookup"><span data-stu-id="805ef-152">The <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>EnumPrinterDrivers</strong></a> function enumerates the printer drivers installed on a specified printer server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="805ef-153"><a href="enumprintprocessordatatypes.md"><strong>EnumPrintProcessorDatatypes</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-153"><a href="enumprintprocessordatatypes.md"><strong>EnumPrintProcessorDatatypes</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-154">La función <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>EnumPrintProcessorDatatypes</strong></a> enumera los tipos de datos que admite un procesador de impresión especificado.</span><span class="sxs-lookup"><span data-stu-id="805ef-154">The <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>EnumPrintProcessorDatatypes</strong></a> function enumerates the data types that a specified print processor supports.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="805ef-155"><a href="enumprintprocessors.md"><strong>EnumPrintProcessors</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-155"><a href="enumprintprocessors.md"><strong>EnumPrintProcessors</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-156">La función <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>EnumPrintProcessors</strong></a> enumera los procesadores de impresión instalados en el servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="805ef-156">The <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>EnumPrintProcessors</strong></a> function enumerates the print processors installed on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="805ef-157"><a href="getcoreprinterdrivers.md"><strong>GetCorePrinterDrivers</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-157"><a href="getcoreprinterdrivers.md"><strong>GetCorePrinterDrivers</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-158">Recupera el GUID, la versión y la fecha de los controladores de impresora principales especificados y la ruta de acceso a sus paquetes.</span><span class="sxs-lookup"><span data-stu-id="805ef-158">Retrieves GUID, version, and date of the specified core printer drivers and the path to their packages.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="805ef-159"><a href="getprinterdriver.md"><strong>GetPrinterDriver</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-159"><a href="getprinterdriver.md"><strong>GetPrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-160">La función <a href="/windows/desktop/printdocs/getprinterdriver"><strong>GetPrinterDriver</strong></a> recupera los datos del controlador de la impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="805ef-160">The <a href="/windows/desktop/printdocs/getprinterdriver"><strong>GetPrinterDriver</strong></a> function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="805ef-161">Si el controlador no está instalado en el equipo local, <strong>GetPrinterDriver</strong> lo instala.</span><span class="sxs-lookup"><span data-stu-id="805ef-161">If the driver is not installed on the local computer, <strong>GetPrinterDriver</strong> installs it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="805ef-162"><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-162"><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-163">La función <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> recupera los datos del controlador de la impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="805ef-163">The <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="805ef-164">Si el controlador no está instalado en el equipo local, <strong>GetPrinterDriver2</strong> lo instala y muestra cualquier interfaz de usuario en la ventana especificada.</span><span class="sxs-lookup"><span data-stu-id="805ef-164">If the driver is not installed on the local computer, <strong>GetPrinterDriver2</strong> installs it and displays any user interface to the specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="805ef-165"><a href="getprinterdriverdirectory.md"><strong>GetPrinterDriverDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-165"><a href="getprinterdriverdirectory.md"><strong>GetPrinterDriverDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-166">La función <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>GetPrinterDriverDirectory</strong></a> recupera la ruta de acceso del directorio del controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="805ef-166">The <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>GetPrinterDriverDirectory</strong></a> function retrieves the path of the printer-driver directory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="805ef-167"><a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-167"><a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-168">Recupera la ruta de acceso al paquete de controladores de impresora especificado en un servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="805ef-168">Retrieves the path to the specified printer driver package on a print server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="805ef-169"><a href="getprintprocessordirectory.md"><strong>GetPrintProcessorDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-169"><a href="getprintprocessordirectory.md"><strong>GetPrintProcessorDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-170">La función <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>GetPrintProcessorDirectory</strong></a> recupera la ruta de acceso al directorio del procesador de impresión en el servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="805ef-170">The <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>GetPrintProcessorDirectory</strong></a> function retrieves the path to the print processor directory on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="805ef-171"><a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-171"><a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-172">Instala un controlador de impresora desde un paquete de controladores que se encuentra en el almacén de controladores del servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="805ef-172">Installs a printer driver from a driver package that is in the print server's driver store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="805ef-173"><a href="uploadprinterdriverpackage.md"><strong>UploadPrinterDriverPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="805ef-173"><a href="uploadprinterdriverpackage.md"><strong>UploadPrinterDriverPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="805ef-174">Carga un controlador de impresora en el almacén de controladores del servidor de impresión para que se pueda instalar llamando a <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="805ef-174">Uploads a printer driver to the print server's driver store so that it can be installed by calling <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

