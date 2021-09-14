---
title: Windows Defender Funciones
description: Funciones a las que llaman las aplicaciones para solicitar exámenes, actualizaciones de firmas o información de Windows Defender.
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ecfa00a38c2263fe1db1b996bb3ec052f8caef1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172262"
---
# <a name="windows-defender-functions"></a>Windows Defender Funciones

Funciones a las que llaman las aplicaciones para solicitar exámenes, actualizaciones de firmas o información de Windows Defender.




| Función | Descripción | 
|----------|-------------|
| <a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a> | Devuelve un mensaje de error con formato basado en un código de error.<br /> | 
| <a href="mpfreememory.md"><strong>MpFreeMemory</strong></a> | Libera memoria para el administrador de protección contra malware.<br /> | 
| <a href="mphandleclose.md"><strong>MpHandleClose</strong></a> | Cierra el identificador devuelto por <a href="mpmanageropen.md"><strong>MpManagerOpen,</strong></a> <a href="mpscanstart.md"><strong>MpScanStart,</strong></a> <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>o <a href="mpupdatestart.md"><strong>MpUpdateStart.</strong></a><br /> | 
| <a href="mpmanageropen.md"><strong>MpManagerAbrir</strong></a> | Establece una conexión con el administrador de protección contra malware en el equipo local.<br /> | 
| <a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a> | <strong>No compatible.</strong> Devuelve información de estado sobre varios componentes del administrador de protección contra malware.<br /> | 
| <a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a> | Devuelve información de estado sobre varios componentes del administrador de protección contra malware.<br /> | 
| <a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a> | Devuelve información de versión sobre varios componentes del administrador de protección contra malware.<br /> | 
| <a href="mpscancontrol.md"><strong>MpScanControl</strong></a> | Permite el control de un examen que se inició de forma asincrónica a través de <a href="mpscanstart.md"><strong>MpScanStart</strong></a>.<br /> | 
| <a href="mpscanstart.md"><strong>MpScanStart</strong></a> | Inicia una operación de examen.<br /> | 
| <a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a> | Devuelve información sobre la siguiente amenaza en la lista de enumeración. Se puede llamar a esta función repetidamente hasta que se complete la enumeración de todas las amenazas.<br /> | 
| <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a> | Devuelve un identificador de enumeración para recuperar amenazas. Esta función se puede usar para abrir las amenazas detectadas por un examen específico, todas las amenazas activas en el sistema, el historial de la trata de amenazas o todas las amenazas presentes en la base de datos de firmas.<br /> | 
| <a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a> | Se usa para consultar información estática (como gravedad y categoría) o localizada (por ejemplo, descripción de categoría y consejos) sobre una amenaza determinada.<br /> | 
| <a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a> | Permite el control de una operación de actualización de firma que se inició de forma asincrónica a través <a href="mpupdatestart.md"><strong>de MpUpdateStart</strong></a>.<br /> | 
| <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a> | Inicia una operación de actualización de firma.<br /> | 
| <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> | Cambia Windows Defender estado a on o off.<br /><blockquote>[!Note]<br />A partir Windows 10, versión 1607 y Windows Server 2016, la <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>función WDEnable</strong></a> siempre <strong>devuelve E_NOTIMPL</strong>.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a> | Devuelve el estado actual de Windows Defender.<br /> | 




 

 

 





