---
description: ICE46 busca propiedades personalizadas en condiciones, texto con formato y otras ubicaciones que difieren de una propiedad definida por el sistema solo por el caso de uno o varios caracteres.
ms.assetid: 892d7462-0222-4fa0-b14c-17742a266c0a
title: ICE46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e24a76560b02a3a0ce3afa681c7ba74fcc7a2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074598"
---
# <a name="ice46"></a>ICE46

ICE46 busca propiedades personalizadas en condiciones, texto con formato y otras ubicaciones que difieren de una propiedad definida por el sistema solo por el caso de uno o varios caracteres.

## <a name="result"></a>Resultado

ICE46 publica un mensaje informativo si hay una propiedad personalizada en una condición, texto con formato y otra ubicación que difiere de las propiedades definidas por el sistema solo en el caso de uno o varios caracteres.

## <a name="example"></a>Ejemplo

ICE46 notifica los siguientes errores para el ejemplo mostrado.



| Error ICE46                                                                                                                                            | Descripción                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La propiedad ReinstallMode definida en la tabla de propiedades difiere de otra propiedad definida solo por mayúsculas y minúsculas.                                                   | El nombre de propiedad definido por el sistema **REINSTALLMODE** difiere de la propiedad personalizada solo por mayúsculas y minúsculas. Las propiedades distinguen mayúsculas de minúsculas, por lo que la propiedad personalizada no es la misma que la propiedad del sistema. Se trata de una causa común de errores. |
| Propiedad "Myproperty" a la que se hace referencia en la columna "InstallExecuteSequence"." La condición" de la fila "InstallFinalize" difiere de una propiedad definida solo por mayúsculas y minúsculas. | La tabla de propiedades define la tabla MyProperty, pero la propiedad a la que se hace referencia es Myproperty. Las propiedades distinguen mayúsculas de minúsculas, por lo que las dos propiedades NO son iguales. Se trata de una causa común de errores.                          |



 

[Tabla de propiedades](property-table.md)



| Propiedad.      | Value   |
|---------------|---------|
| ReinstallMode | omus    |
| Myproperty    | un valor |



 

[InstallExecuteSequence Table](installexecutesequence-table.md) (parcial)



| Acción          | Condición  |
|-----------------|------------|
| InstallFinalize | Myproperty |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



