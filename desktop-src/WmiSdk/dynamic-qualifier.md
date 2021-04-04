---
description: El calificador dinámico indica una clase cuyas instancias se crean dinámicamente. El valor de este calificador debe establecerse en TRUE.
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908677"
---
# <a name="dynamic-qualifier"></a>Calificador dinámico

El calificador **dinámico** indica una clase cuyas instancias se crean dinámicamente. El valor de este calificador debe establecerse en **true**.

El calificador **dinámico** debe especificarse en todas las clases que contienen datos y cuyas instancias se crean dinámicamente. El calificador de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) se suele especificar también para identificar el proveedor responsable de proporcionar los datos.

Las clases que solo contienen métodos que necesitan implementación no requieren el calificador **dinámico** . Solo se requiere el calificador de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) para especificar el nombre del proveedor para proporcionar la implementación.

Todas las clases derivadas de una clase dinámica deben ser dinámicas. No se puede derivar una clase estática de una clase dinámica.

Cuando se especifica **Dynamic** en una propiedad de una instancia de, también se debe especificar el calificador **PropertyContext** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Calificadores WMI estándar**](standard-wmi-qualifiers.md)
</dt> <dt>

[Calificadores WMI](wmi-qualifiers.md)
</dt> <dt>

[Adición de un calificador](adding-a-qualifier.md)
</dt> </dl>

 

 




