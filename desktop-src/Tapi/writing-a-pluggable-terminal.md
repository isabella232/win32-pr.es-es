---
description: Normalmente, un proveedor de servicios multimedia (MSP) implementa la creación de terminal.
ms.assetid: 203fccc0-aa5a-4ec3-97d3-546c36018d52
title: Escritura de un terminal conectable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6cbfe2da0c121fcee820d47fd57216840d23c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542438"
---
# <a name="writing-a-pluggable-terminal"></a>Escritura de un terminal conectable

Normalmente, un proveedor de servicios multimedia (MSP) implementa la creación de terminal. A partir de Windows 2000 SP1, TAPI 3 incluye terminales conectables para permitir que una aplicación implemente la creación de terminal. Consulte la información general sobre la [implementación de terminales conectables](implementing-pluggable-terminals.md) para obtener información adicional sobre el uso de estos terminales.

No debe usar los terminales conectables de forma rutinaria porque las capacidades completas de un terminal solo estarán disponibles cuando un MSP sea totalmente consciente de ello. Además, no debe intentar implementar terminales conectables a menos que ya esté familiarizado con la escritura de proveedores de servicios multimedia. Las técnicas y los posibles problemas que conlleva son bastante similares.

El aprovisionamiento de un caso especial de terminal acoplable existe actualmente para la situación de un servidor de conferencia que necesita agregar clientes que no son de Windows 2000 SP1 o que no son de multidifusión H. 323 a conferencias de multidifusión a SDP/IP en TAPI 3

 

 



