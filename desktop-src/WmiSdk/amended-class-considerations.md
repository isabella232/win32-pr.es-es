---
description: No se pueden crear instancias de las clases modificadas en el espacio de nombres localizado. Las clases modificadas en el espacio de nombres localizado se tratan como si fuera abstractas, aunque no contienen el calificador Abstract.
ms.assetid: a0583153-f5d2-4f4c-ab2e-6ec468e665c7
ms.tgt_platform: multiple
title: Consideraciones de clase modificadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30cd38bc6134c4fd3596cc36e8a7638eaa1fd6ed264c90302d921a391982e5d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320261"
---
# <a name="amended-class-considerations"></a>Consideraciones de clase modificadas

No se pueden crear instancias de las clases modificadas en el espacio de nombres localizado. Las clases modificadas en el espacio de nombres localizado se tratan como si fuera abstractas, aunque no contienen el [**calificador Abstract.**](standard-qualifiers.md)

Si recupera una clase modificada de un espacio de nombres localizado mediante la marca WBEM \_ FLAG \_ USE \_ AMENDED QUALIFIERS y genera una instancia a partir de ella, la instancia contiene todos los calificadores modificados de la \_ clase modificada. No se puede almacenar esta nueva clase en el espacio de nombres que contiene la definición de clase básica a menos que realice la operación **put** con la marca WBEM \_ FLAG USE \_ \_ AMENDED \_ QUALIFIERS. Esta marca indica a WMI que se desasoyen los calificadores modificados antes de guardar el objeto. Si no especifica WBEM FLAG USE AMENDED QUALIFIERS, la operación put produce un \_ \_ error \_ \_ WBEM E  \_ \_ AMENDED \_ OBJECT.

 

 



