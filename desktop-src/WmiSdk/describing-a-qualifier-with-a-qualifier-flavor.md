---
description: Un calificador es una marca que describe más información sobre un calificador.
ms.assetid: a7d9d1c0-9386-4c90-9788-993b35ed12db
ms.tgt_platform: multiple
title: Describir un calificador con un calificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a55cc3cf31a7ac554ed927b9c6a3dd9aec3384c1f81c4d06347895b6249228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117925133"
---
# <a name="describing-a-qualifier-with-a-qualifier-flavor"></a>Describir un calificador con un calificador

Un [*calificador es*](gloss-q.md) una marca que describe más información sobre un calificador. Por ejemplo, el tipo de calificador restringido indica que WMI no debe propagar el calificador asociado a ninguna clase o instancia derivada. Puede establecer los formatos mediante código MOF o mediante programación. Aunque puede describir una variedad de efectos con tipos, el propósito principal de las marcas de tipo es definir cómo WMI propaga los calificadores a través de la herencia.

WMI define varios tipos de calificador que puede asociar a cualquier calificador, independientemente del origen del calificador. Sin embargo, algunos tipos no son adecuados para todos los tipos de calificador. El **tipo ToSubClass,** por ejemplo, solo es adecuado para calificadores definidos para una clase. No se puede **asociar ToSubClass** a un calificador usado para describir una instancia.

Puede usar tipos para describir una variedad de efectos diferentes para calificadores. Por ejemplo, flavor puede indicar si se puede localizar un calificador. Sin embargo, uno de los propósitos principales de un tipo de calificador es describir si una clase primaria puede pasar calificadores a una subclase o instancia de clase. También puede usar tipos para determinar si una propiedad de clase pasa un calificador a una propiedad de instancia. Por último, use tipos para especificar si una subclase puede invalidar el valor original de un calificador heredado. Sin embargo, los calificadores que se declaran para una clase o instancia no se propagan a las propiedades de esa clase o instancia. Además, los flavors que establecen permisos de invalidación solo son válidos si también se establecen los formatos **ToInstance** o **ToSubClass.**

Un tipo se puede asignar globalmente a un calificador para un archivo MOF completo mediante la sintaxis siguiente en la que el espacio en blanco actúa como delimitador cuando se especifican varios tipos.

``` syntax
Qualifier QualifierName : flavor1 <flavor2...>;
```

Los tipos globales se aplican a todos los usos posteriores del calificador en el archivo MOF. Las instrucciones de tipo global pueden producirse en cualquier parte del archivo fuera de un bloque de declaración de objeto. Los tipos redefinidos en el nivel de clase, instancia o propiedad invalidan las declaraciones de tipo global para el ámbito de ese objeto.

No se puede definir un nuevo tipo. Aunque puede crear un nuevo calificador, use solo los [calificadores existentes](qualifier-flavors.md) para describir el nuevo calificador.

**Para definir tipos de calificador en MOF**

-   Declare los flavors que describen un calificador determinado después del nombre del calificador, entre los corchetes de calificador. Use el espacio en blanco como delimitador entre varios tipos.

    En el ejemplo siguiente se muestra el patrón para adjuntar calificadores predefinidos.

    ``` syntax
    [qualifier1 : flavor1 flavor2 flavor3, qualifier2 : flavor1]
    ```

Puede agregar tipos de calificador mediante programación solo en C++. Esta operación no está disponible en [scripting API para WMI,](scripting-api-for-wmi.md)aunque puede agregar un nuevo calificador llamando a [**SWbemQualifierSet.Add**](swbemqualifierset-add.md).

**Para asignar un tipo mediante C++**

-   Llame al [**método IWbemQualifierSet::P ut**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) con el parámetro *lFlavor* establecido en una de las constantes definidas para el método .

 

 



