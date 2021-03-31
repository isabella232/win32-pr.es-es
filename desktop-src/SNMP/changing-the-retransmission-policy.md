---
title: Cambio de la Directiva de retransmisión
description: La implementación de Microsoft WinSNMP proporciona compatibilidad con la Directiva de retransmisión mediante el almacenamiento de un valor de tiempo de espera y un número de reintentos para la aplicación WinSNMP en una base de datos.
ms.assetid: 9ab45adc-12b7-40b1-8fec-40bf04302f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f21fc479517b8844e9c1db75834b5b1c02edc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903496"
---
# <a name="changing-the-retransmission-policy"></a><span data-ttu-id="fdb04-103">Cambio de la Directiva de retransmisión</span><span class="sxs-lookup"><span data-stu-id="fdb04-103">Changing the Retransmission Policy</span></span>

<span data-ttu-id="fdb04-104">La implementación de Microsoft WinSNMP proporciona compatibilidad con la Directiva de retransmisión mediante el almacenamiento de un valor de tiempo de espera y un número de reintentos para la aplicación WinSNMP en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="fdb04-104">The Microsoft WinSNMP implementation provides retransmission policy support by storing a time-out value and a retry count for the WinSNMP application in a database.</span></span> <span data-ttu-id="fdb04-105">La implementación de almacena valores para entidades de destino individuales.</span><span class="sxs-lookup"><span data-stu-id="fdb04-105">The implementation stores values for individual destination entities.</span></span> <span data-ttu-id="fdb04-106">La implementación proporciona inicialmente valores predeterminados para estos elementos, pero una aplicación puede Agregar o modificar valores para entidades individuales.</span><span class="sxs-lookup"><span data-stu-id="fdb04-106">The implementation initially supplies default values for these elements, but an application can add or modify values for individual entities.</span></span>

<span data-ttu-id="fdb04-107">Una llamada a las funciones [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) y [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) devuelve los valores de tiempo de espera y número de reintentos para una entidad de destino específica.</span><span class="sxs-lookup"><span data-stu-id="fdb04-107">A call to the [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) and [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) functions returns the time-out and retry count values for a specific destination entity.</span></span> <span data-ttu-id="fdb04-108">Para cambiar el valor de tiempo de espera, una aplicación WinSNMP debe llamar a la función [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) .</span><span class="sxs-lookup"><span data-stu-id="fdb04-108">To change the time-out value, a WinSNMP application must call the [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) function.</span></span> <span data-ttu-id="fdb04-109">Para cambiar el valor de número de reintentos, la aplicación debe llamar a la función [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) .</span><span class="sxs-lookup"><span data-stu-id="fdb04-109">To change the retry count value the application must call the [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) function.</span></span> <span data-ttu-id="fdb04-110">La configuración actualizada afecta a las nuevas solicitudes de mensajes SNMP a la entidad de destino.</span><span class="sxs-lookup"><span data-stu-id="fdb04-110">The updated settings affect new SNMP message requests to the destination entity.</span></span>

 

 




