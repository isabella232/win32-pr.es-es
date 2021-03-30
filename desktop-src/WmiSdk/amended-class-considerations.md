---
description: No se pueden crear instancias de las clases modificadas en el espacio de nombres localizado. Las clases modificadas en el espacio de nombres localizado se tratan como si fueran abstractas, aunque no contienen el calificador abstracto.
ms.assetid: a0583153-f5d2-4f4c-ab2e-6ec468e665c7
ms.tgt_platform: multiple
title: Consideraciones de la clase modificada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f77a2caa315ab4878fe619c13c69bd5d2e1a2610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279622"
---
# <a name="amended-class-considerations"></a>Consideraciones de la clase modificada

No se pueden crear instancias de las clases modificadas en el espacio de nombres localizado. Las clases modificadas en el espacio de nombres localizado se tratan como si fueran abstractas, aunque no contienen el calificador [**abstracto**](standard-qualifiers.md) .

Si recupera una clase modificada de un espacio de nombres localizado mediante la marca WBEM \_ \_ usar el indicador de \_ \_ calificadores modificados y genera una instancia a partir de ella, la instancia contiene todos los calificadores modificados de la clase modificada. No se puede almacenar esta nueva clase en el espacio de nombres que contiene la definición de clase básica a menos que realice la operación **Put** con la marca WBEM \_ use la marca de \_ \_ \_ calificadores modificados. Esta marca indica a WMI que elimine todos los calificadores modificados antes de guardar el objeto. Si no especifica \_ la marca WBEM \_ usar \_ \_ calificadores modificados, se produce un error en la operación **Put** con un \_ error de objeto modificado por WBEM E \_ \_ .

 

 



