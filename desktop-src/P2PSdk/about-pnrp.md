---
description: El proveedor de espacios de nombres del Protocolo de resolución de nombres de mismo nivel (PNRP) es una tecnología de resolución de nombres sin servidor que permite a los nodos detectarse entre sí.
ms.assetid: e11d0f07-f3a0-4c0f-94ce-1d4944a34230
title: Acerca de PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec402548423ef6baeb15e64a859455fe52332cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156548"
---
# <a name="about-pnrp"></a>Acerca de PNRP

El proveedor de espacios de nombres del Protocolo de resolución de nombres de mismo nivel (PNRP) es una tecnología de resolución de nombres sin servidor que permite a los nodos detectarse entre sí. PNRP usa la API del proveedor de espacios de nombres Winsock 2.

PNRP requiere compatibilidad con IPv6 y es el único protocolo de Internet nativo para la API. Sin embargo, PNRP puede resolver direcciones IPv4 a través de las tecnologías de transición 6to4 o [Teredo](/windows/desktop/Teredo/portal) . Los usuarios de Windows XP con Service Pack 1 (SP1) deben descargar el [paquete de redes avanzadas](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) para habilitar la compatibilidad con IPv6 que requiere PNRP.

> [!Note]  
> Las aplicaciones que usan PNRP en un entorno con un firewall requieren grupos de excepciones que cubran el puerto específico de la aplicación, así como el puerto ' 3540-UDP ' para PNRP. Estos grupos de excepciones se deben habilitar cada vez que se ejecute la aplicación.

 

Aunque PNRP 2,0 es nativo para las plataformas Windows Vista y Windows Server 2008, los usuarios de Windows XP deben descargar Windows Update [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) para actualizar a PNRP 2,0.

 

 
