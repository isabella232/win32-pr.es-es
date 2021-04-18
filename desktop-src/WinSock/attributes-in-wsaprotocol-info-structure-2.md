---
description: XP1 \_ admiten \_ \_ los parámetros de Multipoint, plano de control MULTIpoint \_ y XP1 Multipoint de XP1 \_ \_ \_ \_ en la estructura de información de Winsock WSAPROTOCOL \_ .
ms.assetid: 62f5b8b0-a404-49d1-b163-026f79a46845
title: Atributos en WSAPROTOCOL_INFO estructura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39ea2905da3228860d4fe22f5a0f0d954ce0624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715143"
---
# <a name="attributes-in-wsaprotocol_info-structure"></a><span data-ttu-id="e8a61-103">Atributos en la \_ estructura de información de WSAPROTOCOL</span><span class="sxs-lookup"><span data-stu-id="e8a61-103">Attributes in WSAPROTOCOL\_INFO Structure</span></span>

<span data-ttu-id="e8a61-104">En la compatibilidad con la taxonomía descrita anteriormente, se usan tres parámetros de atributo en la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para distinguir los esquemas utilizados en los planos de control y de datos, respectivamente:</span><span class="sxs-lookup"><span data-stu-id="e8a61-104">In support of the taxonomy described above, three attribute parameters in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure are used to distinguish the schemes used in the control and data planes respectively:</span></span>

-   <span data-ttu-id="e8a61-105">XP1 \_ support \_ multipoint con un valor de 1 indica que esta entrada de protocolo admite comunicaciones multipunto y que los dos parámetros siguientes son significativos.</span><span class="sxs-lookup"><span data-stu-id="e8a61-105">XP1\_SUPPORT\_MULTIPOINT with a value of 1 indicates this protocol entry supports multipoint communications, and that the following two parameters are meaningful.</span></span>
-   <span data-ttu-id="e8a61-106">\_ \_ \_ El plano de control Multipoint de XP1 indica si el plano de control es de raíz (valor = 1) o no raíz (valor = 0).</span><span class="sxs-lookup"><span data-stu-id="e8a61-106">XP1\_MULTIPOINT\_CONTROL\_PLANE indicates whether the control plane is rooted (value = 1) or nonrooted (value = 0).</span></span>
-   <span data-ttu-id="e8a61-107">\_ \_ \_ El plano de datos Multipoint de XP1 indica si el plano de datos tiene raíz (valor = 1) o no raíz (valor = 0).</span><span class="sxs-lookup"><span data-stu-id="e8a61-107">XP1\_MULTIPOINT\_DATA\_PLANE indicates whether the data plane is rooted (value = 1) or nonrooted (value = 0).</span></span>

<span data-ttu-id="e8a61-108">Tenga en cuenta que dos entradas de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) estarán presentes si un protocolo Multipoint admitía los planos de datos raíz y no raíz, una entrada para cada uno.</span><span class="sxs-lookup"><span data-stu-id="e8a61-108">Note that two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entries would be present if a multipoint protocol supported both rooted and nonrooted data planes, one entry for each.</span></span>

<span data-ttu-id="e8a61-109">La aplicación puede utilizar [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) para detectar si se admiten las comunicaciones multipunto para un protocolo determinado y, si es así, cómo se admite con respecto al control y a los planos de datos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e8a61-109">The application can use [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) to discover whether multipoint communications is supported for a given protocol and, if so, how it is supported with respect to the control and data planes, respectively.</span></span>

 

 
