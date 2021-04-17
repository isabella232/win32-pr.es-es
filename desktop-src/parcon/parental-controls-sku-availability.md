---
description: Disponibilidad de SKU de controles parentales
ms.assetid: 5fbf6c4a-3897-4a12-bef6-19478fdb48aa
title: Disponibilidad de SKU de controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b858bc62e8f10a3b06313befd99d67e497b8d442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697140"
---
# <a name="parental-controls-sku-availability"></a>Disponibilidad de SKU de controles parentales

En la actualidad, las interfaces de usuario, las características y las API de control parental que se describen en esta sección están previstas para que solo estén disponibles en SKU centradas en el consumidor, como:

-   Windows Vista Starter
-   Windows Vista Home Basic
-   Windows Vista Home Premium
-   Windows Vista Ultimate

El control parental solo se instala en estas SKU. Las soluciones que tienen un requisito para implementar en las SKU de negocio deberán:

-   Detectar y no proporcionar la funcionalidad de controles parentales en las SKU de negocio.
-   Detecte y proporcione un medio alternativo de configuración, registro y restricciones.

Se recomienda que las soluciones detecten la disponibilidad de la infraestructura de controles parentales comprobando si COM CoCreateInstance se ha ejecutado correctamente en la API de cumplimiento.

Las aplicaciones basadas en controles parentales que dependen de la infraestructura de Windows Vista también pueden querer suprimir sus propias opciones de configuración de la interfaz de usuario u otra funcionalidad cuando se suprime la interfaz de usuario de controles parentales en una SKU compatible. Se proporciona una función para la determinación de la visibilidad que abarca casos como la supresión unida a un dominio.

 

 



