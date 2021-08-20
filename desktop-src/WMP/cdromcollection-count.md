---
title: CdromCollection.count
description: La propiedad count recupera el número de unidades de CD y DVD disponibles en el sistema.
ms.assetid: 98d24713-6a55-409f-af9a-fc941ad6d8f5
keywords:
- CdromCollection.count Reproductor de Windows Media
topic_type:
- apiref
api_name:
- CdromCollection.count
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db279f746640d09fac8b3852773afc27330fc9ca48d59a1470de7d42709e60f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864105"
---
# <a name="cdromcollectioncount"></a>CdromCollection.count

La **propiedad count** recupera el número de unidades de CD y DVD disponibles en el sistema.

``` syntax
player.cdromCollection.count
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Comentarios

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

Las unidades de DVD-ROM se cuentan exactamente igual que las unidades de CD. Sin embargo, el control Reproductor de Windows Media solo admite la funcionalidad de DVD para Windows XP o sistemas operativos posteriores. Normalmente, las unidades de DVD pueden reproducir medios de CD, pero las unidades de CD no pueden reproducir medios de DVD.

**Reproductor de Windows Media 10 Mobile:** Este método siempre devuelve 0.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se *usa CdromCollection*. **count** para mostrar el número de unidades de CD y DVD disponibles en el equipo del usuario. El objeto player se creó con id. = "Player".


```JScript
// Store the count of drives found on the computer.
var numCDROMS = Player.cdromCollection.count;

// Build the string to display to the user.
var displayString = numCDROMS + " drive(s) found.";

// Show a message box with the count information.
alert(displayString);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/>                               |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CdromCollection (objeto)**](cdromcollection-object.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





