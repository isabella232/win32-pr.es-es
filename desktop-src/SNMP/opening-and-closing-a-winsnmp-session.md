---
title: Abrir y cerrar una sesión WinSNMP
description: Para abrir una sesión, una aplicación llama a la función SnmpCreateSession.
ms.assetid: 76650231-509b-45be-b156-09752b817854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e006ffb81f6c2508b3505678b28c3ace8e60c85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076046"
---
# <a name="opening-and-closing-a-winsnmp-session"></a><span data-ttu-id="d6a66-103">Abrir y cerrar una sesión WinSNMP</span><span class="sxs-lookup"><span data-stu-id="d6a66-103">Opening and Closing a WinSNMP Session</span></span>

<span data-ttu-id="d6a66-104">Para abrir una sesión, una aplicación llama a la función [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) .</span><span class="sxs-lookup"><span data-stu-id="d6a66-104">To open a session, an application calls the [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function.</span></span> <span data-ttu-id="d6a66-105">Si la función se completa correctamente, la implementación de Microsoft WinSNMP abre una sesión y la función devuelve un identificador de sesión en forma de un identificador **de \_ sesión HSNMP** .</span><span class="sxs-lookup"><span data-stu-id="d6a66-105">If the function completes successfully, the Microsoft WinSNMP implementation opens a session, and the function returns a session identifier in the form of an **HSNMP\_SESSION** handle.</span></span> <span data-ttu-id="d6a66-106">Todas las funciones WinSNMP que devuelven variables de identificador incluyen el identificador de sesión como parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="d6a66-106">All WinSNMP functions that return handle variables include the session identifier as an input parameter.</span></span> <span data-ttu-id="d6a66-107">Esto permite a la implementación utilizar el identificador para administrar de forma eficaz los recursos en el nivel de sesión.</span><span class="sxs-lookup"><span data-stu-id="d6a66-107">This enables the implementation to use the handle to efficiently manage resources at the session level.</span></span>

<span data-ttu-id="d6a66-108">Una aplicación puede tener varias sesiones abiertas al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="d6a66-108">An application can have multiple sessions open at one time.</span></span> <span data-ttu-id="d6a66-109">Varias sesiones dentro de una aplicación pueden compartir variables de identificador.</span><span class="sxs-lookup"><span data-stu-id="d6a66-109">Multiple sessions within an application can share handle variables.</span></span>

<span data-ttu-id="d6a66-110">Si la implementación no puede abrir una sesión debido a las limitaciones de recursos, devuelve un error de SNMPAPI \_ cuando la aplicación llama a [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span><span class="sxs-lookup"><span data-stu-id="d6a66-110">If the implementation cannot open a session because of resource limitations, it returns SNMPAPI\_FAILURE when the application calls [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span></span> <span data-ttu-id="d6a66-111">Si la aplicación llama a la función [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) , devuelve snmpapi \_ error de asignación \_ .</span><span class="sxs-lookup"><span data-stu-id="d6a66-111">If the application then calls the [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) function, it returns SNMPAPI\_ALLOC\_ERROR.</span></span>

<span data-ttu-id="d6a66-112">Una llamada a la función [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) permite a la implementación liberar los recursos restantes y cerrar la sesión.</span><span class="sxs-lookup"><span data-stu-id="d6a66-112">A call to the [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) function enables the implementation to free any remaining resources and to close the session.</span></span>

<span data-ttu-id="d6a66-113">Para obtener más información, vea [objetos de identificador de recursos](resource-handle-objects.md) y [sesiones WinSNMP](winsnmp-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="d6a66-113">For more information, see [Resource Handle Objects](resource-handle-objects.md) and [WinSNMP Sessions](winsnmp-sessions.md).</span></span>

 

 




