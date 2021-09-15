---
title: Novedades de SNMP
description: SNMP admite el uso de IPv6 a partir de Windows Vista.
ms.assetid: 38d71c0a-8de1-45a7-958c-aa44411451bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913f71cdf0b23800340f2c43f7b7fa22f45883a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473486"
---
# <a name="new-in-snmp"></a>Novedades de SNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, [Windows administración remota](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-Man.\]

SNMP admite el uso de IPv6 a partir de Windows Vista. Sin embargo, SNMP solo admite IPv6 para redes que ejecutan Windows Server 2008 y Windows Vista. Esto se debe a que SNMP requiere la pila de protocolos actualizada disponible en estos sistemas operativos para su compatibilidad con IPv6.

A menos que la red sea únicamente una red de Windows Server 2008, se producirá un error en las comunicaciones IPv6, incluso si una pila de protocolos IPv6 se instala por separado en los equipos que ejecutan versiones anteriores de Windows. Por ejemplo, los agentes SNMP que se ejecutan en Windows Server 2003, Windows XP o Windows 2000 solo responden a las consultas realizadas a sus direcciones IPv4.

 

 