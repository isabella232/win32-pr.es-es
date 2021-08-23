---
title: Ensamblado de cadenas de consulta
description: En Active Directory, el uso de criterios de filtrado específicos puede mejorar el rendimiento de la búsqueda. Esto se debe a Active Directory evalúa todos los predicados, identifica los índices y, a continuación, selecciona un índice con probabilidad de producir el conjunto más pequeño de valores devueltos.
ms.assetid: 4139eedb-1383-4654-9b40-5e294a71be24
ms.tgt_platform: multiple
keywords:
- Ensamblado de cadenas de consulta ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 610ba78d6536d9cfe12f296fcbfa46d04cd572ae05cdb7d3bb8b0e1e7b5d32a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962212"
---
# <a name="assembling-query-strings"></a>Ensamblado de cadenas de consulta

En Active Directory, el uso de criterios de filtrado específicos puede mejorar el rendimiento de la búsqueda. Esto se debe a Active Directory evalúa todos los predicados, identifica los índices y, a continuación, selecciona un índice con probabilidad de producir el conjunto más pequeño de valores devueltos.

Evite buscar texto en el centro o el final de una cadena, por ejemplo, "cn= \* montés" o \* "cn= \* larouse".

Cuando sea posible, busque atributos indexados. Los atributos indexados se almacenan en todos los controladores de dominio, por lo que lo más probable es que la consulta sea más rápida que buscar un atributo no indexado.

 

 




