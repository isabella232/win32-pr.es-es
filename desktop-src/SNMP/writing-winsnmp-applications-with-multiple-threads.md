---
title: Escribir aplicaciones WinSNMP con varios subprocesos
description: La implementación de Microsoft WinSNMP garantiza que las operaciones WinSNMP de un proceso no modifiquen la configuración de WinSNMP de otro proceso.
ms.assetid: faa98704-f55f-4450-9f6e-d2bbbc7a50b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb6b7991968c5c5efafa898758c3c60cad1abb2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421020"
---
# <a name="writing-winsnmp-applications-with-multiple-threads"></a>Escribir aplicaciones WinSNMP con varios subprocesos

La implementación de Microsoft WinSNMP garantiza que las operaciones WinSNMP de un proceso no modifiquen la configuración de WinSNMP de otro proceso.

Una aplicación WinSNMP con varios subprocesos debe asegurarse de que las operaciones de WinSNMP que establecen los parámetros de nivel de aplicación sean seguras para subprocesos. Las funciones que establecen los parámetros de nivel de aplicación son [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) y [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode). Estas funciones modifican la configuración de la entidad y el modo de traducción de contexto y el modo de retransmisión.

Para obtener más información, vea [varios](/windows/desktop/ProcThread/multiple-threads) subprocesos y [seguridad para subprocesos y derechos de acceso](/windows/desktop/ProcThread/thread-security-and-access-rights).

 

 