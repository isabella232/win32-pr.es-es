---
title: Tipo de inicio de BITS
description: El tipo de inicio para BITS se retrasa el inicio automático. Antes de Windows Vista, el tipo de inicio para BITS es Manual. Cuando se crea un trabajo de BITS, el tipo de inicio cambia a Automático. El tipo de inicio vuelve a Manual cuando se completan o cancelan todos los trabajos.
ms.assetid: 0d9ec60f-3488-4eb2-a6a2-22932fd74caf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: defafff5b3dd0a9b03e18b61b84fa6c32022035ce58913599151ee526fd52d0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579435"
---
# <a name="bits-startup-type"></a>Tipo de inicio de BITS

El **tipo de inicio** para BITS se retrasa el inicio automático (si hay trabajos de BITS activos) o el inicio de la demanda (si no hay ningún trabajo activo). Las versiones de Windows anteriores a la actualización de noviembre solo usaban el tipo de inicio automático retrasado; las versiones anteriores a Vista usaban el tipo de inicio manual.

No debe establecer el Tipo **de inicio** en Deshabilitado. Deshabilitar BITS puede interrumpir las aplicaciones que se basan en BITS para transferir archivos.

 

 




