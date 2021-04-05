---
title: Funciones de Windows Defender
description: Funciones a las que llaman las aplicaciones para solicitar exámenes, actualizaciones de firmas o información de Windows Defender.
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225530c9d0c2970930d0bc38e23f7907f588e89e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420185"
---
# <a name="windows-defender-functions"></a><span data-ttu-id="f880d-103">Funciones de Windows Defender</span><span class="sxs-lookup"><span data-stu-id="f880d-103">Windows Defender Functions</span></span>

<span data-ttu-id="f880d-104">Funciones a las que llaman las aplicaciones para solicitar exámenes, actualizaciones de firmas o información de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="f880d-104">Functions called by apps to request scans, signature updates, or information from Windows Defender.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f880d-105">Función</span><span class="sxs-lookup"><span data-stu-id="f880d-105">Function</span></span></th>
<th><span data-ttu-id="f880d-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="f880d-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f880d-107"><a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a></span><span class="sxs-lookup"><span data-stu-id="f880d-107"><a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a></span></span></td>
<td><span data-ttu-id="f880d-108">Devuelve un mensaje de error con formato basado en un código de error.</span><span class="sxs-lookup"><span data-stu-id="f880d-108">Returns a formatted error message based on an error code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f880d-109"><a href="mpfreememory.md"><strong>MpFreeMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="f880d-109"><a href="mpfreememory.md"><strong>MpFreeMemory</strong></a></span></span></td>
<td><span data-ttu-id="f880d-110">Libera memoria para el administrador de protección contra malware de.</span><span class="sxs-lookup"><span data-stu-id="f880d-110">Frees memory for the malware protection manager.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f880d-111"><a href="mphandleclose.md"><strong>MpHandleClose</strong></a></span><span class="sxs-lookup"><span data-stu-id="f880d-111"><a href="mphandleclose.md"><strong>MpHandleClose</strong></a></span></span></td>
<td><span data-ttu-id="f880d-112">Cierra el identificador devuelto por <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>, <a href="mpscanstart.md"><strong>MpScanStart</strong></a>, <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>o <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f880d-112">Closes the handle returned by <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>, <a href="mpscanstart.md"><strong>MpScanStart</strong></a>, <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>, or <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f880d-113"><a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a></span><span class="sxs-lookup"><span data-stu-id="f880d-113"><a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a></span></span></td>
<td><span data-ttu-id="f880d-114">Establece una conexión con el administrador de protección contra malware en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="f880d-114">Establishes a connection to the malware protection manager on the local computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f880d-115"><a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="f880d-115"><a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a></span></span></td>
<td><span data-ttu-id="f880d-116"><strong>No compatible.</strong></span><span class="sxs-lookup"><span data-stu-id="f880d-116"><strong>Not supported.</strong></span></span> <span data-ttu-id="f880d-117">Devuelve información de estado sobre los distintos componentes del administrador de protección contra malware de.</span><span class="sxs-lookup"><span data-stu-id="f880d-117">Returns status information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f880d-118"><a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="f880d-118"><a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a></span></span></td>
<td><span data-ttu-id="f880d-119">Devuelve información de estado sobre los distintos componentes del administrador de protección contra malware de.</span><span class="sxs-lookup"><span data-stu-id="f880d-119">Returns status information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f880d-120"><a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="f880d-120"><a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a></span></span></td>
<td><span data-ttu-id="f880d-121">Devuelve información de versión sobre varios componentes del administrador de protección contra malware de.</span><span class="sxs-lookup"><span data-stu-id="f880d-121">Returns version information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f880d-122"><a href="mpscancontrol.md"><strong>MpScanControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="f880d-122"><a href="mpscancontrol.md"><strong>MpScanControl</strong></a></span></span></td>
<td><span data-ttu-id="f880d-123">Permite el control de un examen que se inició de forma asincrónica a través de <a href="mpscanstart.md"><strong>MpScanStart</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f880d-123">Allows the control of a scan that was asynchronously initiated via <a href="mpscanstart.md"><strong>MpScanStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f880d-124"><a href="mpscanstart.md"><strong>MpScanStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="f880d-124"><a href="mpscanstart.md"><strong>MpScanStart</strong></a></span></span></td>
<td><span data-ttu-id="f880d-125">Inicia una operación de digitalización.</span><span class="sxs-lookup"><span data-stu-id="f880d-125">Starts a scanning operation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f880d-126"><a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a></span><span class="sxs-lookup"><span data-stu-id="f880d-126"><a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a></span></span></td>
<td><span data-ttu-id="f880d-127">Devuelve información sobre la siguiente amenaza en la lista de enumeración.</span><span class="sxs-lookup"><span data-stu-id="f880d-127">Returns information about the next threat in the enumeration list.</span></span> <span data-ttu-id="f880d-128">Se puede llamar a esta función varias veces hasta que se complete la enumeración de todas las amenazas.</span><span class="sxs-lookup"><span data-stu-id="f880d-128">This function can be called repeatedly until the enumeration of all the threats is complete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f880d-129"><a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a></span><span class="sxs-lookup"><span data-stu-id="f880d-129"><a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a></span></span></td>
<td><span data-ttu-id="f880d-130">Devuelve un identificador de enumeración con el fin de recuperar las amenazas.</span><span class="sxs-lookup"><span data-stu-id="f880d-130">Returns an enumeration handle for the purpose of retrieving threats.</span></span> <span data-ttu-id="f880d-131">Esta función se puede usar para abrir amenazas detectadas por un análisis específico, todas las amenazas activas del sistema, el historial de la desinfección de amenazas o todas las amenazas presentes en la base de datos de firmas.</span><span class="sxs-lookup"><span data-stu-id="f880d-131">This function can be used to open threats detected by a specific scan, all the active threats in the system, the history of threat disinfection, or all the threats present in the signature database.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f880d-132"><a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="f880d-132"><a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a></span></span></td>
<td><span data-ttu-id="f880d-133">Se usa para consultar información estática (como gravedad y categoría) o localizada (como descripción de la categoría y consejos) sobre una amenaza determinada.</span><span class="sxs-lookup"><span data-stu-id="f880d-133">Used to query static (such as severity and category) or localized (such as category description and advice) information about a particular threat.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f880d-134"><a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="f880d-134"><a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a></span></span></td>
<td><span data-ttu-id="f880d-135">Permite el control de una operación de actualización de firmas que se inició de forma asincrónica a través de <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f880d-135">Allows the control of a signature update operation that was asynchronously initiated via <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f880d-136"><a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="f880d-136"><a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a></span></span></td>
<td><span data-ttu-id="f880d-137">Inicia una operación de actualización de firma.</span><span class="sxs-lookup"><span data-stu-id="f880d-137">Starts a signature update operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f880d-138"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a></span><span class="sxs-lookup"><span data-stu-id="f880d-138"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a></span></span></td>
<td><span data-ttu-id="f880d-139">Cambia el estado de Windows Defender a activado o desactivado.</span><span class="sxs-lookup"><span data-stu-id="f880d-139">Changes Windows Defender status to on or off.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f880d-140">A partir de Windows 10, versión 1607 y Windows Server 2016, la función <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> siempre devuelve <strong>E_NOTIMPL</strong>.</span><span class="sxs-lookup"><span data-stu-id="f880d-140">Beginning in Windows 10, version 1607 and Windows Server 2016, the <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> function always returns <strong>E_NOTIMPL</strong>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f880d-141"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a></span><span class="sxs-lookup"><span data-stu-id="f880d-141"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a></span></span></td>
<td><span data-ttu-id="f880d-142">Devuelve el estado actual de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="f880d-142">Returns the current status of Windows Defender.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





