---
title: El modelo WinSNMP
description: El modelo compatible con WinSNMP incluye los siguientes componentes básicos.
ms.assetid: 491df017-0b91-4fcf-97c3-4e296c3324bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7ae4fa1c1ee56fc534e4aa4c9bffefb8d7f4d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075378"
---
# <a name="the-winsnmp-model"></a><span data-ttu-id="965ca-103">El modelo WinSNMP</span><span class="sxs-lookup"><span data-stu-id="965ca-103">The WinSNMP Model</span></span>

<span data-ttu-id="965ca-104">El modelo compatible con WinSNMP incluye los siguientes componentes básicos:</span><span class="sxs-lookup"><span data-stu-id="965ca-104">The WinSNMP-compliant model includes the following basic components:</span></span>

-   <span data-ttu-id="965ca-105">Una aplicación de administración de red SNMP habilitada para WinSNMP, es decir, una *aplicación* compatible con WinSNMP</span><span class="sxs-lookup"><span data-stu-id="965ca-105">A WinSNMP-enabled SNMP network management application, that is, a WinSNMP-compliant *application*</span></span>
-   <span data-ttu-id="965ca-106">La capa de función WinSNMP</span><span class="sxs-lookup"><span data-stu-id="965ca-106">The WinSNMP function layer</span></span>
-   <span data-ttu-id="965ca-107">Un proveedor de servicios SNMP habilitado para WinSNMP, es decir, una *implementación* compatible con WinSNMP</span><span class="sxs-lookup"><span data-stu-id="965ca-107">A WinSNMP-enabled SNMP service provider, that is, a WinSNMP-compliant *implementation*</span></span>

<span data-ttu-id="965ca-108">Las aplicaciones de administración de red que deben transmitir mensajes SNMP funcionan de manera eficaz en un entorno orientado a eventos.</span><span class="sxs-lookup"><span data-stu-id="965ca-108">Network management applications that must convey SNMP messages operate efficiently in an event-driven environment.</span></span> <span data-ttu-id="965ca-109">Esto se debe a que SNMP es un protocolo basado en datagramas o sin conexión entre entidades remotas que no establecen circuitos virtuales.</span><span class="sxs-lookup"><span data-stu-id="965ca-109">This is because SNMP is a datagram-based or connectionless protocol between remote entities that do not establish virtual circuits.</span></span>

<span data-ttu-id="965ca-110">Dado que las aplicaciones de Microsoft Windows también están orientadas a eventos, WinSNMP usa un modelo de programación en el que la recepción y el procesamiento de las aplicaciones de administración de la unidad de *eventos de mensajes* asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="965ca-110">Since Microsoft Windows applications are also event-driven, WinSNMP uses a programming model in which the receipt and processing of asynchronous *message-events* drive management applications.</span></span> <span data-ttu-id="965ca-111">Un evento de mensaje asincrónico puede ser una solicitud de operación SNMP por parte de una aplicación de administrador o la respuesta a una solicitud de una aplicación de agente.</span><span class="sxs-lookup"><span data-stu-id="965ca-111">An asynchronous message-event can be an SNMP operation request by a manager application, or the response to a request by an agent application.</span></span>

<span data-ttu-id="965ca-112">SNMP envía solicitudes y respuestas como mensajes SNMP.</span><span class="sxs-lookup"><span data-stu-id="965ca-112">SNMP sends requests and responses as SNMP messages.</span></span> <span data-ttu-id="965ca-113">Un mensaje SNMP es una unidad de datos de protocolo SNMP (PDU) más elementos de encabezado de mensaje adicionales definidos por la RFC correspondiente.</span><span class="sxs-lookup"><span data-stu-id="965ca-113">An SNMP message is an SNMP protocol data unit (PDU) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="965ca-114">Para obtener más información, consulte [About SNMP messages](about-snmp-messages.md), [Working with variables Binding lists](working-with-variable-binding-lists.md) and [Working with Protocol Data Units](working-with-protocol-data-units.md).</span><span class="sxs-lookup"><span data-stu-id="965ca-114">For more information, see [About SNMP Messages](about-snmp-messages.md), [Working with Variable Binding Lists](working-with-variable-binding-lists.md) and [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>

 

 




