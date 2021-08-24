---
title: Escritura de aplicaciones WinSNMP con varios subprocesos
description: La implementación de Microsoft WinSNMP garantiza que las operaciones WinSNMP de un proceso no modifiquen la configuración de WinSNMP de otro proceso.
ms.assetid: faa98704-f55f-4450-9f6e-d2bbbc7a50b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33ee400009204a1117eb54b8166ade2c10f3d1dd3317a8316d70fc8c2d606d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142738"
---
# <a name="writing-winsnmp-applications-with-multiple-threads"></a>Escritura de aplicaciones WinSNMP con varios subprocesos

La implementación de Microsoft WinSNMP garantiza que las operaciones WinSNMP de un proceso no modifiquen la configuración de WinSNMP de otro proceso.

Una aplicación WinSNMP con varios subprocesos debe asegurarse de que las operaciones de WinSNMP que establecen parámetros de nivel de aplicación sean seguras para subprocesos. Las funciones que establecen parámetros de nivel de aplicación [**son SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) y [**SnmpSetRetransmitMode.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) Estas funciones modifican la configuración del modo de traducción de entidades y contexto y el modo de retransmisión.

Para obtener más información, [vea Multiple Threads](/windows/desktop/ProcThread/multiple-threads) and Thread Security and Access [Rights](/windows/desktop/ProcThread/thread-security-and-access-rights).

 

 