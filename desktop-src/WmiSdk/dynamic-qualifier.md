---
description: El calificador Dinámico indica una clase cuyas instancias se crean dinámicamente. El valor de este calificador debe establecerse en TRUE.
ms.assetid: 63286687-abbf-49f0-8061-3b47fba75806
ms.tgt_platform: multiple
title: Calificador dinámico
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dynamic
api_type:
- NA
api_location: ''
ms.openlocfilehash: f6530942859c8c3de571ba9ddb94e9b1ce78cc0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575344"
---
# <a name="dynamic-qualifier"></a>Calificador dinámico

El **calificador** Dinámico indica una clase cuyas instancias se crean dinámicamente. El valor de este calificador debe establecerse en **TRUE.**

El **calificador** dinámico debe especificarse en todas las clases que contienen datos y para qué instancias se crean dinámicamente. [**Normalmente,**](/windows/desktop/api/Provider/nl-provider-provider) el calificador Provider también se especifica para identificar el proveedor responsable de proporcionar los datos.

Las clases que contienen solo métodos que necesitan implementación no requieren el **calificador Dinámico.** Solo el [**calificador Provider**](/windows/desktop/api/Provider/nl-provider-provider) es necesario para especificar el nombre del proveedor para proporcionar la implementación.

Todas las clases derivadas de una clase dinámica deben ser dinámicas. No se puede derivar una clase estática de una clase dinámica.

Cuando **se** especifica Dynamic en una propiedad de una instancia de , también se debe especificar el calificador **PropertyContext.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Calificadores WMI estándar**](standard-wmi-qualifiers.md)
</dt> <dt>

[Calificadores WMI](wmi-qualifiers.md)
</dt> <dt>

[Agregar un calificador](adding-a-qualifier.md)
</dt> </dl>

 

 




