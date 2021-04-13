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
# <a name="writing-winsnmp-applications-with-multiple-threads"></a><span data-ttu-id="b19fe-103">Escribir aplicaciones WinSNMP con varios subprocesos</span><span class="sxs-lookup"><span data-stu-id="b19fe-103">Writing WinSNMP Applications with Multiple Threads</span></span>

<span data-ttu-id="b19fe-104">La implementación de Microsoft WinSNMP garantiza que las operaciones WinSNMP de un proceso no modifiquen la configuración de WinSNMP de otro proceso.</span><span class="sxs-lookup"><span data-stu-id="b19fe-104">The Microsoft WinSNMP implementation ensures that the WinSNMP operations of one process do not modify the WinSNMP settings of another process.</span></span>

<span data-ttu-id="b19fe-105">Una aplicación WinSNMP con varios subprocesos debe asegurarse de que las operaciones de WinSNMP que establecen los parámetros de nivel de aplicación sean seguras para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="b19fe-105">A WinSNMP application with multiple threads must ensure that WinSNMP operations that set application-level parameters are thread-safe.</span></span> <span data-ttu-id="b19fe-106">Las funciones que establecen los parámetros de nivel de aplicación son [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) y [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode).</span><span class="sxs-lookup"><span data-stu-id="b19fe-106">The functions that set application-level parameters are [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) and [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode).</span></span> <span data-ttu-id="b19fe-107">Estas funciones modifican la configuración de la entidad y el modo de traducción de contexto y el modo de retransmisión.</span><span class="sxs-lookup"><span data-stu-id="b19fe-107">These functions modify settings for the entity and context translation mode and the retransmission mode.</span></span>

<span data-ttu-id="b19fe-108">Para obtener más información, vea [varios](/windows/desktop/ProcThread/multiple-threads) subprocesos y [seguridad para subprocesos y derechos de acceso](/windows/desktop/ProcThread/thread-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="b19fe-108">For more information, see [Multiple Threads](/windows/desktop/ProcThread/multiple-threads) and [Thread Security and Access Rights](/windows/desktop/ProcThread/thread-security-and-access-rights).</span></span>

 

 