---
description: Un tipo de calificador es una marca que describe más información sobre un calificador.
ms.assetid: a7d9d1c0-9386-4c90-9788-993b35ed12db
ms.tgt_platform: multiple
title: Describir un calificador con un tipo de calificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cfc2c590ec8916e2e9538b3e8224e97b3b5dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276261"
---
# <a name="describing-a-qualifier-with-a-qualifier-flavor"></a>Describir un calificador con un tipo de calificador

Un [*tipo de calificador*](gloss-q.md) es una marca que describe más información sobre un calificador. Por ejemplo, el tipo de calificador restringido indica que WMI no debe propagar el calificador asociado a ninguna clase o instancia derivada. Puede establecer sabores mediante código MOF o mediante programación. Aunque puede describir una variedad de efectos con sabores, los principales propósitos de las marcas de sabor consisten en definir cómo WMI propaga los calificadores a través de la herencia.

WMI define varios tipos de calificador que se pueden adjuntar a cualquier calificador, independientemente del origen del calificador. Sin embargo, algunas versiones no son adecuadas para todos los tipos de calificador. Por ejemplo, el tipo **ToSubClass** solo es adecuado para los calificadores definidos para una clase. No se puede adjuntar **ToSubClass** a un calificador usado para describir una instancia.

Puede usar tipos para describir diferentes efectos para los calificadores. Por ejemplo, Flavor puede indicar si se puede localizar un calificador. Sin embargo, uno de los principales propósitos de un tipo de calificador es describir si una clase primaria puede pasar calificadores a una subclase o instancia de clase. También puede usar tipos para determinar si una propiedad de clase pasa un calificador a una propiedad de instancia. Por último, use sabores para indicar si una subclase puede reemplazar el valor original de un calificador heredado. Sin embargo, los calificadores que se declaran para una clase o instancia no se propagan a las propiedades de esa clase o instancia. Además, los tipos que establecen permisos de invalidación solo son válidos si también se establecen los tipos **ToInstance** o **ToSubClass** .

Un tipo se puede asignar globalmente a un calificador para un archivo MOF completo utilizando la sintaxis siguiente en la que el espacio en blanco actúa como delimitador cuando se especifican varios tipos.

``` syntax
Qualifier QualifierName : flavor1 <flavor2...>;
```

Los tipos globales se aplican a todos los usos subsiguientes del calificador en el archivo MOF. Las instrucciones de tipo global pueden aparecer en cualquier parte del archivo fuera de un bloque de declaración de objeto. Los tipos redefinidos en el nivel de clase, instancia o propiedad reemplazan las declaraciones de tipo globales para el ámbito de ese objeto.

No se puede definir un nuevo tipo. Aunque puede crear un nuevo calificador, use solo los [tipos de calificador](qualifier-flavors.md) existentes para describir el nuevo calificador.

**Para definir los tipos de calificador en MOF**

-   Declare los tipos que describen un calificador determinado después del nombre del calificador, entre los corchetes del calificador. Use el espacio en blanco como delimitador entre varias versiones.

    En el ejemplo siguiente se muestra el patrón para adjuntar calificadores predefinidos.

    ``` syntax
    [qualifier1 : flavor1 flavor2 flavor3, qualifier2 : flavor1]
    ```

Puede agregar tipos de calificador mediante programación solo en C++. Esta operación no está disponible en la [API de scripting para WMI](scripting-api-for-wmi.md), aunque puede Agregar un nuevo calificador mediante una llamada a [**SWbemQualifierSet. Add**](swbemqualifierset-add.md).

**Para asignar un tipo mediante C++**

-   Llame al método [**IWbemQualifierSet::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) con el parámetro *lFlavor* establecido en una de las constantes definidas para el método.

 

 



