---
description: Después de determinar cómo organizar el filtro a través de una estructura CAPTUREFILTER, debe asignar y rellenar la estructura , que luego se pasa al controlador Monitor de red a través de un BLOB de configuración.
ms.assetid: c2709da6-4d70-4abe-bab5-941053217e57
title: Implementar el código de filtro de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c407f3208a1c7720655667f78e4422b57882de6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169301"
---
# <a name="implementing-the-capture-filter-code"></a>Implementar el código de filtro de captura

Después de determinar cómo organizar el filtro a través de una estructura [**CAPTUREFILTER,**](capturefilter.md) debe asignar y rellenar la estructura , que luego se pasa al controlador Monitor de red a través de un BLOB de configuración.

Los usuarios de NPP directos agregan el filtro de captura al BLOB de configuración que se **pasa a Conectar**, [**Configurar**](configure.md)o ambos. Para obtener una lista de interfaces COM que puede usar para comunicarse con el NPP, vea [Interfaces de NPP](npp-interfaces.md).

 

 



