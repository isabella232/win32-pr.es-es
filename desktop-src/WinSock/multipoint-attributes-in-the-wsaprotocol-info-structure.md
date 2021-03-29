---
title: Atributos multipunto en WSAPROTOCOL_INFO
description: Los atributos multipunto de la \_ estructura WSAPROTOCOL info incluyen XP1 support Multipoint \_ \_ , XP1 \_ Multipoint \_ control \_ Plane y XP1 \_ Multipoint \_ Data \_ Plane.
ms.assetid: f1bd5aa1-e705-4eaf-9436-fed0ea03f113
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baedcd07f53db462eb090217b53d93a1a4aa8c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809728"
---
# <a name="multipoint-attributes-in-wsaprotocol_info"></a><span data-ttu-id="746f3-103">Atributos multipunto en WSAPROTOCOL_INFO</span><span class="sxs-lookup"><span data-stu-id="746f3-103">Multipoint attributes in WSAPROTOCOL_INFO</span></span>

<span data-ttu-id="746f3-104">Se definen tres parámetros de atributo en la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para distinguir los distintos esquemas que se usan en los planos de control y de datos, respectivamente:</span><span class="sxs-lookup"><span data-stu-id="746f3-104">Three attribute parameters are defined in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure in order to distinguish the different schemes used in the control and data planes, respectively:</span></span>

-   <span data-ttu-id="746f3-105">XP1 \_ support \_ multipoint con un valor de 1 indica que esta entrada de protocolo admite comunicaciones multipunto y que los dos parámetros siguientes son significativos.</span><span class="sxs-lookup"><span data-stu-id="746f3-105">XP1\_SUPPORT\_MULTIPOINT with a value of 1 indicates this protocol entry supports multipoint communications, and that the following two parameters are meaningful.</span></span>
-   <span data-ttu-id="746f3-106">\_ \_ \_ El plano de control Multipoint de XP1 indica si el plano de control es de raíz (valor = 1) o no raíz (valor = 0).</span><span class="sxs-lookup"><span data-stu-id="746f3-106">XP1\_MULTIPOINT\_CONTROL\_PLANE indicates whether the control plane is rooted (value = 1) or nonrooted (value = 0).</span></span>
-   <span data-ttu-id="746f3-107">\_ \_ \_ El plano de datos Multipoint de XP1 indica si el plano de datos tiene raíz (valor = 1) o no raíz (valor = 0).</span><span class="sxs-lookup"><span data-stu-id="746f3-107">XP1\_MULTIPOINT\_DATA\_PLANE indicates whether the data plane is rooted (value = 1) or nonrooted (value = 0).</span></span>

<span data-ttu-id="746f3-108">Dos entradas de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) estarán presentes si un protocolo Multipoint admitía los planos de datos raíz y no raíz, una entrada para cada uno.</span><span class="sxs-lookup"><span data-stu-id="746f3-108">Two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entries would be present if a multipoint protocol supported both rooted and nonrooted data planes, one entry for each.</span></span>

 

 
