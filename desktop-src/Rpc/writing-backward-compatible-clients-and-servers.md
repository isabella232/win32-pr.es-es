---
title: Escritura de clientes y servidores compatibles con versiones anteriores
description: En teoría, el esquema de control de versiones de RPC ayuda a evitar la comunicación indebido entre los servidores y los clientes modificados y sus homólogos implementados.
ms.assetid: 0c7d6716-e4ed-447e-bf64-906d55bec907
keywords:
- RPC (llamada a procedimiento remoto), procedimientos recomendados, compatibilidad con versiones anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac5ae011c8a9c346bc0f89fb73e26265d487721
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148785"
---
# <a name="writing-backward-compatible-clients-and-servers"></a><span data-ttu-id="3af4e-104">Escritura de clientes y servidores compatibles con versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="3af4e-104">Writing Backward Compatible Clients and Servers</span></span>

<span data-ttu-id="3af4e-105">En teoría, el esquema de control de versiones de RPC ayuda a evitar la comunicación indebido entre los servidores y los clientes modificados y sus homólogos implementados.</span><span class="sxs-lookup"><span data-stu-id="3af4e-105">In theory, the versioning scheme of RPC helps prevent miscommunication between modified servers and clients and their deployed counterparts.</span></span> <span data-ttu-id="3af4e-106">Sin embargo, en la práctica, los desarrolladores deben introducir cambios en las interfaces existentes sin modificar la versión, ya que los clientes y servidores anteriores deben ser capaces de comunicarse con otros nuevos.</span><span class="sxs-lookup"><span data-stu-id="3af4e-106">In practice, however, developers frequently must introduce changes to existing interfaces without modifying the version, because previous clients and servers must be able to communicate with new ones.</span></span> <span data-ttu-id="3af4e-107">Se trata de un problema mayor para RPC estándar que para COM; la consulta es una forma natural de buscar interfaces compatibles en COM, mientras que en el control de excepciones RPC debe usarse para una cobertura equivalente.</span><span class="sxs-lookup"><span data-stu-id="3af4e-107">This is a larger issue for standard RPC than for COM; querying is a natural way of searching for supported interfaces in COM, while in RPC exception handling must be used for equivalent coverage.</span></span>

<span data-ttu-id="3af4e-108">En esta sección se describen las mejores prácticas de programación de RPC para abordar estas situaciones.</span><span class="sxs-lookup"><span data-stu-id="3af4e-108">This section discusses the best RPC programming practices for addressing these situations.</span></span> <span data-ttu-id="3af4e-109">Esta sección se divide en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="3af4e-109">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="3af4e-110">La teoría de control de versiones de RPC y COM</span><span class="sxs-lookup"><span data-stu-id="3af4e-110">The Versioning Theory for RPC and COM</span></span>](the-versioning-theory-for-rpc-and-com.md)
-   [<span data-ttu-id="3af4e-111">Cambiar las interfaces de una manera compatible con versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="3af4e-111">Changing Interfaces in a Backward Compatible Manner</span></span>](changing-interfaces-in-a-backward-compatible-manner.md)
-   [<span data-ttu-id="3af4e-112">Ejemplos de cambios incompatibles</span><span class="sxs-lookup"><span data-stu-id="3af4e-112">Examples of Incompatible Changes</span></span>](examples-of-incompatible-changes.md)

 

 




