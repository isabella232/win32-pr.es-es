---
title: Abrir y cerrar una aplicación WinSNMP
description: La aplicación WinSNMP debe llamar correctamente a la función SnmpStartup antes de llamar a cualquier otra función WinSNMP.
ms.assetid: ff2b99c9-c2fd-4bb7-8fd5-799e72c4560d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f960a22a6155d3f3eeec770af361fac2c0eb036e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076048"
---
# <a name="opening-and-closing-a-winsnmp-application"></a><span data-ttu-id="24de6-103">Abrir y cerrar una aplicación WinSNMP</span><span class="sxs-lookup"><span data-stu-id="24de6-103">Opening and Closing a WinSNMP Application</span></span>

<span data-ttu-id="24de6-104">La aplicación WinSNMP debe llamar correctamente a la función [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) antes de llamar a cualquier otra función WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="24de6-104">The WinSNMP application must call the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function successfully before it calls any other WinSNMP function.</span></span> <span data-ttu-id="24de6-105">La función **SnmpStartup** permite que la implementación de Microsoft WinSNMP realice procedimientos de inicialización.</span><span class="sxs-lookup"><span data-stu-id="24de6-105">The **SnmpStartup** function enables the Microsoft WinSNMP implementation to perform initialization procedures.</span></span> <span data-ttu-id="24de6-106">La función también devuelve a la aplicación la versión de la API WinSNMP que admite la implementación, el nivel de comunicaciones SNMP que admite y los modos de traducción y retransmisión predeterminados de la implementación.</span><span class="sxs-lookup"><span data-stu-id="24de6-106">The function also returns to the application the version of the WinSNMP API that the implementation supports, the level of SNMP communications it supports, and the implementation's default translation and retransmission modes.</span></span>

<span data-ttu-id="24de6-107">La aplicación WinSNMP debe llamar a la función [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) cuando la aplicación ya no requiere los servicios de la implementación.</span><span class="sxs-lookup"><span data-stu-id="24de6-107">The WinSNMP application must call the [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) function when the application no longer requires the implementation's services.</span></span> <span data-ttu-id="24de6-108">Aunque **SnmpCleanup** permite que la implementación Desasigne todos los recursos asignados a la aplicación, se recomienda que la aplicación llame primero a la función [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) una vez por cada sesión WinSNMP abierta para maximizar el rendimiento de la implementación.</span><span class="sxs-lookup"><span data-stu-id="24de6-108">Even though **SnmpCleanup** enables the implementation to deallocate all resources allocated to the application, it is recommended that the application first call the [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) function once for each open WinSNMP session, to maximize the implementation's performance.</span></span> <span data-ttu-id="24de6-109">La aplicación WinSNMP debe llamar a [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) como la última función WinSNMP antes de finalizar.</span><span class="sxs-lookup"><span data-stu-id="24de6-109">The WinSNMP application must call [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) as the last WinSNMP function before it terminates.</span></span>

 

 




