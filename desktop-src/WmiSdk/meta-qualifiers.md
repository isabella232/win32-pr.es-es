---
description: Los metaclasifiquen la definición de meta constructos en el modelo CIM aclarando el uso real de una declaración de clase o propiedad dentro de la sintaxis de MOF.
ms.assetid: 3674a051-3756-4d09-a70e-46a57b442104
ms.tgt_platform: multiple
title: Meta calificadores
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76609fecca3e3831372ea813e7210cd449c2e1e4fc527df605bc523efd4c1be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131186"
---
# <a name="meta-qualifiers"></a>Meta calificadores

Los metaclasifiquen la definición de meta constructos en el modelo CIM aclarando el uso real de una declaración de clase o propiedad dentro de la sintaxis de MOF.

<dt>

<span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Asociación**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases

Indica si la clase es una clase de asociación que se usa para describir una relación entre otras dos clases. La ausencia de este calificador indica que la clase no es una clase de asociación. Este calificador es mutuamente excluyente con **Indicación**. Para obtener más información, vea [Declarar una clase de asociación](declaring-an-association-class.md).

</dd> <dt>

<span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Indicación**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases

Indica si la clase de objeto define una indicación. Este calificador es mutuamente excluyente con **Association**. El valor predeterminado es **FALSE.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Calificadores WMI](wmi-qualifiers.md)
</dt> <dt>

[Agregar un calificador](adding-a-qualifier.md)
</dt> </dl>

 

 




