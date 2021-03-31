---
title: Novedades de SNMP
description: SNMP admite el uso de IPv6 a partir de Windows Vista.
ms.assetid: 38d71c0a-8de1-45a7-958c-aa44411451bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913f71cdf0b23800340f2c43f7b7fa22f45883a2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793486"
---
# <a name="new-in-snmp"></a>Novedades de SNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]

SNMP admite el uso de IPv6 a partir de Windows Vista. Sin embargo, SNMP solo es compatible con IPv6 para redes que ejecutan Windows Server 2008 y Windows Vista. Esto se debe a que SNMP requiere que la pila de protocolos actualizada esté disponible en estos sistemas operativos para su compatibilidad con IPv6.

A menos que la red sea únicamente una red de Windows Server 2008, se producirá un error en las comunicaciones IPv6, incluso si una pila de protocolo IPv6 se instala por separado en los equipos que ejecutan versiones anteriores de Windows. Por ejemplo, los agentes SNMP que se ejecutan en Windows Server 2003 o Windows XP o Windows 2000, solo responden a las consultas que se realizan en sus direcciones IPv4.

 

 