---
description: Disponibilidad de la SKU de los controles parentales
ms.assetid: 5fbf6c4a-3897-4a12-bef6-19478fdb48aa
title: Disponibilidad de la SKU de los controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21184a383a28e3ae06198f203475c1c03334e5d678278bbb3b4988b52971e79e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461205"
---
# <a name="parental-controls-sku-availability"></a>Disponibilidad de la SKU de los controles parentales

Las interfaces de usuario, las características y las API de Parental Controls que se describen en esta sección están actualmente planeadas para estar disponibles solo en SKU centradas en el consumidor, como:

-   Windows Vista Starter
-   Windows Vista Home Basic
-   Windows Vista Home Premium
-   Windows Vista Ultimate

Los controles parentales solo se instalan en estas SKU. Las soluciones que tengan un requisito para implementarse en LAS SKU empresariales tendrán que:

-   Detecte y no proporcione la funcionalidad de controles parentales en las SKU empresariales.
-   Detecte y proporcione un medio alternativo de configuración, registro y restricciones.

Se recomienda que las soluciones detecten la disponibilidad de la infraestructura de controles parentales mediante la comprobación del éxito de COM CoCreateInstance en la API de cumplimiento.

Las aplicaciones compatibles con los controles parentales en función de la infraestructura de Windows Vista también pueden querer suprimir cualquier interfaz de usuario propia que exponga la configuración u otra funcionalidad cuando se suprima la interfaz de usuario de controles parentales en una SKU compatible. Se proporciona una función para determinar la visibilidad que cubre casos como la supresión unida a un dominio.

 

 



