---
title: Acerca de la implementación de Microsoft WinSNMP
description: La implementación de Microsoft WinSNMP cumple con la versión WinSNMP 2,0.
ms.assetid: 99e11d30-d159-4d9b-94d0-baa6e49d82cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cbf142ba85458374105af5b80ca5af30a6c5082
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993821"
---
# <a name="about-the-microsoft-winsnmp-implementation"></a><span data-ttu-id="bd18f-103">Acerca de la implementación de Microsoft WinSNMP</span><span class="sxs-lookup"><span data-stu-id="bd18f-103">About the Microsoft WinSNMP Implementation</span></span>

<span data-ttu-id="bd18f-104">La implementación de Microsoft WinSNMP cumple con la versión WinSNMP 2,0.</span><span class="sxs-lookup"><span data-stu-id="bd18f-104">The Microsoft WinSNMP implementation complies with WinSNMP version 2.0.</span></span> <span data-ttu-id="bd18f-105">Admite todas las funciones y operaciones definidas en la especificación de la versión 1.1 de WinSNMP y en el anexo de la versión WinSNMP 2,0.</span><span class="sxs-lookup"><span data-stu-id="bd18f-105">It supports all the functions and operations defined in both the WinSNMP version 1.1a specification and the WinSNMP version 2.0 Addendum.</span></span> <span data-ttu-id="bd18f-106">La implementación de proporciona los siguientes servicios para las aplicaciones WinSNMP:</span><span class="sxs-lookup"><span data-stu-id="bd18f-106">The implementation provides the following services for WinSNMP applications:</span></span>

-   <span data-ttu-id="bd18f-107">Administra las comunicaciones hacia y desde las entidades de administración.</span><span class="sxs-lookup"><span data-stu-id="bd18f-107">Manages communications to and from management entities.</span></span> <span data-ttu-id="bd18f-108">La entidad puede residir en el equipo local o conectarse a través de una red local o de área extensa, o Internet.</span><span class="sxs-lookup"><span data-stu-id="bd18f-108">The entity can reside on the local computer or be connected through a local or wide-area network, or the Internet.</span></span> <span data-ttu-id="bd18f-109">Para obtener más información, consulte [niveles de compatibilidad con SNMP](levels-of-snmp-support.md).</span><span class="sxs-lookup"><span data-stu-id="bd18f-109">For more information, see [Levels of SNMP Support](levels-of-snmp-support.md).</span></span>
-   <span data-ttu-id="bd18f-110">Oculta los detalles del protocolo SNMP, la notación de sintaxis abstracta uno (ASN. 1) y las reglas de codificación básicas (BER) para describir la sintaxis de transferencia.</span><span class="sxs-lookup"><span data-stu-id="bd18f-110">Hides the details of SNMP protocol, Abstract Syntax Notation One (ASN.1), and the Basic Encoding Rules (BER) for describing transfer syntax.</span></span>
-   <span data-ttu-id="bd18f-111">Comprueba la exactitud de las PDU y rechaza las PDU no válidas.</span><span class="sxs-lookup"><span data-stu-id="bd18f-111">Verifies the correctness of PDUs and rejects invalid PDUs.</span></span> <span data-ttu-id="bd18f-112">Para obtener más información, vea [trabajar con unidades de datos de protocolo](working-with-protocol-data-units.md).</span><span class="sxs-lookup"><span data-stu-id="bd18f-112">For more information, see [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>
-   <span data-ttu-id="bd18f-113">Transforma los tipos de PDU de SNMPv2C cuando sea necesario de acuerdo con las RFC pertinentes.</span><span class="sxs-lookup"><span data-stu-id="bd18f-113">Transforms SNMPv2C PDU types when necessary in accordance with the relevant RFCs.</span></span>
-   <span data-ttu-id="bd18f-114">Convierte las capturas de SNMPv1 de un agente SNMPv1 en capturas de SNMPv2C de acuerdo con RFC 1908, "coexistencia entre la versión 1 y la versión 2 del marco de administración de redes estándar de Internet".</span><span class="sxs-lookup"><span data-stu-id="bd18f-114">Converts SNMPv1 traps from an SNMPv1 agent to SNMPv2C traps in accordance with RFC 1908, "Coexistence between Version 1 and Version 2 of the Internet-standard Network Management Framework."</span></span> <span data-ttu-id="bd18f-115">Para obtener más información, consulte [trasladar capturas de SNMPv1 a SNMPv2c](translating-traps-from-snmpv1-to-snmpv2c.md).</span><span class="sxs-lookup"><span data-stu-id="bd18f-115">For more information, see [Translating Traps from SNMPv1 to SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md).</span></span>
-   <span data-ttu-id="bd18f-116">Admite la Directiva de retransmisión de la aplicación y proporciona compatibilidad con la ejecución de la retransmisión.</span><span class="sxs-lookup"><span data-stu-id="bd18f-116">Supports the application's retransmission policy and provides retransmission execution support.</span></span> <span data-ttu-id="bd18f-117">Para obtener más información, consulte [la base de datos WinSNMP](the-winsnmp-database.md) y [acerca de la retransmisión](about-retransmission.md).</span><span class="sxs-lookup"><span data-stu-id="bd18f-117">For more information, see [The WinSNMP Database](the-winsnmp-database.md) and [About Retransmission](about-retransmission.md).</span></span>
-   <span data-ttu-id="bd18f-118">Proporciona compatibilidad con la traducción de entidades y contextos para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bd18f-118">Provides entity and context translation support for the application.</span></span> <span data-ttu-id="bd18f-119">Para obtener más información, consulte [la base de datos WinSNMP](the-winsnmp-database.md) y [establezca la entidad y el modo de traducción de contexto](setting-the-entity-and-context-translation-mode.md).</span><span class="sxs-lookup"><span data-stu-id="bd18f-119">For more information, see [The WinSNMP Database](the-winsnmp-database.md) and [Setting the Entity and Context Translation Mode](setting-the-entity-and-context-translation-mode.md).</span></span>

<span data-ttu-id="bd18f-120">Para obtener más información sobre la relación entre una aplicación WinSNMP y la implementación de, consulte los [conceptos de administración de datos WinSNMP](winsnmp-data-management-concepts.md) y las [sesiones de WinSNMP](winsnmp-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="bd18f-120">For additional information about the relationship between a WinSNMP application and the implementation, see [WinSNMP Data Management Concepts](winsnmp-data-management-concepts.md) and [WinSNMP Sessions](winsnmp-sessions.md).</span></span>

 

 




