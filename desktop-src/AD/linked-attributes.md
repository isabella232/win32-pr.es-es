---
title: Atributos vinculados (AD DS)
description: Los atributos vinculados son pares de atributos en los que el sistema calcula los valores de un atributo (el vínculo de retroceso) en función de los valores establecidos en el otro atributo (el vínculo hacia delante) en todo el bosque.
ms.assetid: 31b7e8f5-e46d-4aff-9b17-c8dec7f19bae
ms.tgt_platform: multiple
keywords:
- Atributos vinculados AD
- Attributes AD, linked
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0e3f6706c797497fb1bb25ea82805385f9897e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104420520"
---
# <a name="linked-attributes-ad-ds"></a>Atributos vinculados (AD DS)

Los atributos vinculados son pares de atributos en los que el sistema calcula los valores de un atributo (el vínculo de retroceso) en función de los valores establecidos en el otro atributo (el vínculo hacia delante) en todo el bosque. Un valor de vínculo de reserva en cualquier instancia de objeto se compone del DNs de todos los objetos que tienen el DN del objeto establecido en el vínculo de reenvío correspondiente. Por ejemplo, "Manager" y "Reports" son un par de atributos vinculados, donde Manager es el vínculo hacia delante e informes es el vínculo de retroceso. Supongamos ahora que Bill es el administrador de Joe. Si almacena el DN del objeto de usuario de la factura en el atributo "Manager" del objeto de usuario de Joe, se mostrará el DN del objeto de usuario de Joe en el atributo "Reports" del objeto de usuario de la factura.

Un par de vínculos hacia delante y vínculo hacia atrás se identifica mediante los valores [**LinkId**](/windows/desktop/ADSchema/a-linkid) de dos definiciones [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) . El **LinkId** del vínculo hacia delante es un valor par, positivo y distinto de cero, y el **LinkId** del vínculo de retroceso asociado es el **LinkId** de reenvío más uno. Por ejemplo, el **LinkId** para "Manager" es 42 y el **LinkId** para "Reports" es 43.

A continuación se muestra una lista de instrucciones para definir un nuevo par de atributos vinculados:

-   Los valores [**LinkId**](/windows/desktop/ADSchema/a-linkid) deben ser únicos entre todos los objetos [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) . Para evitar conflictos, debe generar automáticamente el **LinkId** siguiendo las instrucciones del tema [obtener un identificador de vínculo](obtaining-a-link-id.md).
-   Un vínculo hacia atrás debe tener un vínculo de reenvío correspondiente, es decir, el vínculo hacia delante debe existir antes de que se pueda crear un atributo de vínculo hacia atrás correspondiente.
-   Un vínculo hacia atrás siempre es un atributo con varios valores. Un vínculo hacia delante puede ser de un solo valor o de varios valores. Use un vínculo de avance con varios valores cuando haya una relación de varios a varios.
-   El valor [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de un vínculo hacia delante debe ser 2.5.5.1, 2.5.5.7 o 2.5.5.14. Estos valores corresponden a las sintaxis que contienen un nombre distintivo, como la sintaxis [**Object (DS-DN)**](/windows/desktop/ADSchema/s-object-ds-dn) .
-   El valor [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de un vínculo de retroceso debe ser 2.5.5.1, que es la sintaxis del [**objeto (DS-DN)**](/windows/desktop/ADSchema/s-object-ds-dn) .
-   Por Convención, los atributos de vínculo hacia atrás se agregan al valor [**mayContain**](/windows/desktop/ADSchema/a-maycontain) de la clase abstracta [**Top**](/windows/desktop/ADSchema/c-top) . Esto permite que el atributo de vínculo de retroceso se lea desde objetos de cualquier clase porque no se almacenan realmente con el objeto, sino que se calculan en función de los valores de vínculo hacia delante.

 

 