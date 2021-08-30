---
description: Normalmente, un proveedor de servicios multimedia (MSP) implementa la creación del terminal.
ms.assetid: 203fccc0-aa5a-4ec3-97d3-546c36018d52
title: Escritura de un terminal conectable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47395515418a4c2fcc66b972674950ca0c58aa8b01276973ea4ab3e91cbd314
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072805"
---
# <a name="writing-a-pluggable-terminal"></a>Escritura de un terminal conectable

Normalmente, un proveedor de servicios multimedia (MSP) implementa la creación del terminal. A partir Windows 2000 SP1, TAPI 3 incluye terminales conectables para permitir que una aplicación implemente la creación de terminales. Consulte la información general sobre [la implementación de terminales conectables](implementing-pluggable-terminals.md) para obtener información adicional sobre el uso de estos terminales.

No debe usar terminales conectables de forma rutinaria porque las funcionalidades completas de un terminal solo estarán disponibles cuando un MSP sea totalmente consciente de ello. Además, no debe intentar implementar terminales conectables a menos que ya esté familiarizado con la escritura de proveedores de servicios multimedia. Las técnicas y los posibles problemas implicados son bastante similares.

Actualmente existe el aprovisionamiento de un caso especial de terminal conectable para la situación de un servidor de conferencias que necesita agregar clientes H.323 que no son de Windows 2000 SP1 o H.323 sin multidifusión a conferencias de multidifusión SDP/IP de TAPI 3.

 

 



