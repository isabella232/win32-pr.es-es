---
title: Atributos vinculados (AD DS)
description: Los atributos vinculados son pares de atributos en los que el sistema calcula los valores de un atributo (el vínculo hacia atrás) en función de los valores establecidos en el otro atributo (el vínculo hacia delante) en todo el bosque.
ms.assetid: 31b7e8f5-e46d-4aff-9b17-c8dec7f19bae
ms.tgt_platform: multiple
keywords:
- Atributos vinculados ad
- Atributos de AD ,linked
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2167169d6a9d2f8eabe69323054767ae66823d8e1fe954a232ed63fd31a9b845
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186998"
---
# <a name="linked-attributes-ad-ds"></a>Atributos vinculados (AD DS)

Los atributos vinculados son pares de atributos en los que el sistema calcula los valores de un atributo (el vínculo hacia atrás) en función de los valores establecidos en el otro atributo (el vínculo hacia delante) en todo el bosque. Un valor de vínculo hacia atrás en cualquier instancia de objeto consta de los DN de todos los objetos que tienen el DN del objeto establecido en el vínculo hacia delante correspondiente. Por ejemplo, "Manager" e "Reports" son un par de atributos vinculados, donde Manager es el vínculo hacia delante y Reports es el vínculo hacia atrás. Ahora supongamos que Bill es el administrador de Joe. Si almacena el DN del objeto de usuario de Bill en el atributo "Manager" del objeto de usuario de Joe, el DN del objeto de usuario de Joe se mostrará en el atributo "Reports" del objeto de usuario de Bill.

Los valores [**linkID**](/windows/desktop/ADSchema/a-linkid) de dos definiciones de [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) identifican un par de vínculos hacia delante y hacia atrás. El **linkID del** vínculo hacia delante es un valor par, positivo, distinto de cero y el **id.** de vínculo del vínculo hacia atrás asociado es el id. de vínculo hacia delante **más** uno. Por ejemplo, **el linkID de** "Manager" es 42 y el **linkID** para "Reports" es 43.

A continuación se muestra una lista de directrices para definir un nuevo par de atributos vinculados:

-   Los [**valores linkID**](/windows/desktop/ADSchema/a-linkid) deben ser únicos entre todos los [**objetos attributeSchema.**](/windows/desktop/ADSchema/c-attributeschema) Para evitar conflictos, debe generar automáticamente el **identificador** de vínculo siguiendo las instrucciones del tema [Obtención de un identificador de vínculo](obtaining-a-link-id.md).
-   Un vínculo hacia atrás debe tener un vínculo hacia delante correspondiente, es decir, el vínculo hacia delante debe existir antes de que se pueda crear un atributo de vínculo posterior correspondiente.
-   Un vínculo atrás siempre es un atributo con varios valores. Un vínculo hacia delante puede ser de un solo valor o de varios valores. Use un vínculo hacia delante de varios valores cuando haya una relación de varios a varios.
-   El [**valor attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de un vínculo hacia delante debe ser 2.5.5.1, 2.5.5.7 o 2.5.5.14. Estos valores corresponden a sintaxis que contienen un nombre distintivo, como la sintaxis [**Object(DS-DN).**](/windows/desktop/ADSchema/s-object-ds-dn)
-   El [**valor attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de un vínculo atrás debe ser 2.5.5.1, que es la sintaxis [**de Object(DS-DN).**](/windows/desktop/ADSchema/s-object-ds-dn)
-   Por convención, los atributos de vínculo atrás se agregan al [**valor mayContain**](/windows/desktop/ADSchema/a-maycontain) de la [**clase**](/windows/desktop/ADSchema/c-top) abstracta superior. Esto permite leer el atributo de vínculo posterior de los objetos de cualquier clase porque no se almacenan realmente con el objeto , pero se calculan en función de los valores de vínculo hacia delante.

 

 