---
description: ICE46 comprueba si hay propiedades personalizadas en condiciones, texto con formato y otras ubicaciones que difieren de una propiedad definida por el sistema solo en el caso de uno o más caracteres.
ms.assetid: 892d7462-0222-4fa0-b14c-17742a266c0a
title: ICE46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e24a76560b02a3a0ce3afa681c7ba74fcc7a2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813323"
---
# <a name="ice46"></a>ICE46

ICE46 comprueba si hay propiedades personalizadas en condiciones, texto con formato y otras ubicaciones que difieren de una propiedad definida por el sistema solo en el caso de uno o más caracteres.

## <a name="result"></a>Resultado

ICE46 envía un mensaje informativo si hay una propiedad personalizada en una condición, texto con formato y otra ubicación que difiere de las propiedades definidas por el sistema solo en el caso de uno o más caracteres.

## <a name="example"></a>Ejemplo

ICE46 notifica los siguientes errores para el ejemplo que se muestra.



| Error ICE46                                                                                                                                            | Descripción                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La propiedad ReinstallMode definida en la tabla de propiedades solo se diferencia de otra propiedad definida por el uso de mayúsculas o minúsculas.                                                   | El nombre de propiedad de System Defined **REINSTALLMODE** solo se diferencia de la propiedad personalizada por el uso de mayúsculas y minúsculas. Las propiedades distinguen mayúsculas de minúsculas, por lo que la propiedad personalizada no es igual que la propiedad del sistema. Se trata de una causa común de los errores. |
| Se hace referencia a la propiedad ' propiedad ' en la columna ' InstallExecuteSequence '. ' La condición ' de la fila ' InstallFinalize ' es distinta de una propiedad definida por el uso de mayúsculas y minúsculas. | La tabla de propiedades define la propiedad de la tabla, pero la propiedad a la que se hace referencia es propiedad. Las propiedades distinguen mayúsculas de minúsculas, por lo que las dos propiedades no son iguales. Se trata de una causa común de los errores.                          |



 

[Tabla de propiedades](property-table.md)



| Propiedad      | Value   |
|---------------|---------|
| ReinstallMode | OMUs    |
| MyProperty    | un valor |



 

[Tabla InstallExecuteSequence](installexecutesequence-table.md) (parcial)



| Acción          | Condición  |
|-----------------|------------|
| InstallFinalize | MyProperty |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



