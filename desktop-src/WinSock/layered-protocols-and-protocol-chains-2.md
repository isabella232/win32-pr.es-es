---
description: 'Windows Sockets 2 incorpora el concepto de protocolo en capas: uno que implementa solo funciones de comunicaciones de nivel superior mientras se basa en una pila de transporte subyacente para el intercambio de datos real con un punto de conexión remoto.'
ms.assetid: 80e0b229-ebdc-4ac1-8e8e-9e5b7cfc3ab5
title: Protocolos en capas y cadenas de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf74a11dffca9d8c49c61af82132857f5510e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154269"
---
# <a name="layered-protocols-and-protocol-chains"></a><span data-ttu-id="cb89e-103">Protocolos en capas y cadenas de protocolo</span><span class="sxs-lookup"><span data-stu-id="cb89e-103">Layered Protocols and Protocol Chains</span></span>

<span data-ttu-id="cb89e-104">Windows Sockets 2 incorpora el concepto de protocolo en capas: uno que implementa solo funciones de comunicaciones de nivel superior mientras se basa en una pila de transporte subyacente para el intercambio de datos real con un punto de conexión remoto.</span><span class="sxs-lookup"><span data-stu-id="cb89e-104">Windows Sockets 2 incorporates the concept of a layered protocol: one that implements only higher-level communications functions while relying on an underlying transport stack for the actual exchange of data with a remote endpoint.</span></span> <span data-ttu-id="cb89e-105">Un ejemplo de este tipo de protocolo superpuesto es un nivel de seguridad que agrega un protocolo al proceso de conexión de socket para realizar la autenticación y establecer un esquema de cifrado.</span><span class="sxs-lookup"><span data-stu-id="cb89e-105">An example of this type of layered protocol is a security layer that adds a protocol to the socket connection process in order to perform authentication and establish an encryption scheme.</span></span> <span data-ttu-id="cb89e-106">Este protocolo de seguridad suele requerir los servicios de un protocolo de transporte subyacente y confiable, como TCP o SPX.</span><span class="sxs-lookup"><span data-stu-id="cb89e-106">Such a security protocol generally requires the services of an underlying and reliable transport protocol such as TCP or SPX.</span></span>

<span data-ttu-id="cb89e-107">El término *Protocolo base* hace referencia a un protocolo, como TCP o SPX, que es totalmente capaz de realizar comunicaciones de datos con un punto de conexión remoto.</span><span class="sxs-lookup"><span data-stu-id="cb89e-107">The term *base protocol* refers to a protocol, such as TCP or SPX, that is fully capable of performing data communications with a remote endpoint.</span></span> <span data-ttu-id="cb89e-108">Un *Protocolo por capas* es un protocolo que no puede ser independiente, mientras que una *cadena de protocolos* es uno o varios protocolos en capas agrupadosdos juntos y delimitados por un protocolo base.</span><span class="sxs-lookup"><span data-stu-id="cb89e-108">A *layered protocol* is a protocol that cannot stand alone, while a *protocol chain* is one or more layered protocols strung together and anchored by a base protocol.</span></span>

<span data-ttu-id="cb89e-109">Puede crear una cadena de protocolos si diseña los protocolos superpuestos para admitir Windows Sockets 2 SPI en los bordes superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="cb89e-109">You can create a protocol chain if you design the layered protocols to support the Windows Sockets 2 SPI at both their upper and lower edges.</span></span> <span data-ttu-id="cb89e-110">Una estructura especial de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) hace referencia a la cadena de protocolos en conjunto y describe el orden explícito en el que se unen los protocolos en capas.</span><span class="sxs-lookup"><span data-stu-id="cb89e-110">A special [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure refers to the protocol chain as a whole and describes the explicit order in which the layered protocols are joined.</span></span> <span data-ttu-id="cb89e-111">Esto se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="cb89e-111">This is illustrated in the figure below.</span></span> <span data-ttu-id="cb89e-112">Dado que solo las aplicaciones pueden usar directamente los protocolos base y las cadenas de protocolo, son los únicos que se muestran cuando los protocolos instalados se enumeran con la función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) .</span><span class="sxs-lookup"><span data-stu-id="cb89e-112">Since only base protocols and protocol chains are directly usable by applications, they are the only ones listed when the installed protocols are enumerated with the [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) function.</span></span>

![arquitectura de protocolo superpuesto](images/ovrvw2-3.png)

 

 
