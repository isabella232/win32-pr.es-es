---
description: Después de determinar cómo organizar el filtro a través de una estructura CAPTUREFILTER, debe asignar y rellenar la estructura , que luego se pasa al controlador Monitor de red a través de un BLOB de configuración.
ms.assetid: c2709da6-4d70-4abe-bab5-941053217e57
title: Implementar el código de filtro de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c36998daef73c7c7683693ee4f5458339dc5b5c99366caad76f5f6b4283197cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890465"
---
# <a name="implementing-the-capture-filter-code"></a>Implementar el código de filtro de captura

Después de determinar cómo organizar el filtro a través de una estructura [**CAPTUREFILTER,**](capturefilter.md) debe asignar y rellenar la estructura , que luego se pasa al controlador Monitor de red a través de un BLOB de configuración.

Los usuarios de NPP directos agregan el filtro de captura al BLOB de configuración que se **pasa a Conectar,** [**Configure**](configure.md)o ambos. Para obtener una lista de interfaces COM que puede usar para comunicarse con el NPP, vea [Interfaces de NPP](npp-interfaces.md).

 

 



