---
description: Los meta calificadores refinan la definición de meta construcciones en el modelo CIM aclarando el uso real de una declaración de clase o propiedad dentro de la sintaxis MOF.
ms.assetid: 3674a051-3756-4d09-a70e-46a57b442104
ms.tgt_platform: multiple
title: Meta calificadores
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8618ef8258f403a43e08be54b3acbd5bb1e923c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967143"
---
# <a name="meta-qualifiers"></a>Meta calificadores

Los meta calificadores refinan la definición de meta construcciones en el modelo CIM aclarando el uso real de una declaración de clase o propiedad dentro de la sintaxis MOF.

<dt>

<span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Asociación**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases

Indica si la clase es una clase de asociación utilizada para describir una relación entre otras dos clases. La ausencia de este calificador indica que la clase no es una clase de asociación. Este calificador es mutuamente excluyente con **indicación**. Para obtener más información, vea [Declarar una clase de asociación](declaring-an-association-class.md).

</dd> <dt>

<span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Indicación**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases

Indica si la clase de objeto define una indicación. Este calificador es mutuamente excluyente con **association**. El valor predeterminado es **FALSE.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Calificadores WMI](wmi-qualifiers.md)
</dt> <dt>

[Agregar un calificador](adding-a-qualifier.md)
</dt> </dl>

 

 




