---
description: Los calificadores meta refinan la definición de las meta-construcciones en el modelo CIM aclarando el uso real de una declaración de clase o propiedad dentro de la sintaxis MOF.
ms.assetid: 3674a051-3756-4d09-a70e-46a57b442104
ms.tgt_platform: multiple
title: Meta (Calificadores)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8618ef8258f403a43e08be54b3acbd5bb1e923c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659916"
---
# <a name="meta-qualifiers"></a>Meta (Calificadores)

Los calificadores meta refinan la definición de las meta-construcciones en el modelo CIM aclarando el uso real de una declaración de clase o propiedad dentro de la sintaxis MOF.

<dt>

<span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Asociación**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases

Indica si la clase es una clase de asociación que se utiliza para describir una relación entre otras dos clases. La ausencia de este calificador indica que la clase no es una clase de asociación. Este calificador es mutuamente excluyente con **indicación**. Para obtener más información, vea [declarar una clase de asociación](declaring-an-association-class.md).

</dd> <dt>

<span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Señala**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases

Indica si la clase de objeto define una indicación. Este calificador es mutuamente excluyente con la **Asociación**. El valor predeterminado es **false**.

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

[Adición de un calificador](adding-a-qualifier.md)
</dt> </dl>

 

 




