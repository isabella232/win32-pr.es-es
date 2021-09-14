---
title: ClosedCaption.captioningID
description: La propiedad captioningID especifica o recupera el nombre del elemento que muestra los subtítulos.
ms.assetid: 99d4aae3-485f-4c86-9130-101b1ca968e9
keywords:
- ClosedCaption.captioningID Reproductor de Windows Media
topic_type:
- apiref
api_name:
- ClosedCaption.captioningID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faadae626dd5ac0314c4140e3f9d82ab645ef9b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126885305"
---
# <a name="closedcaptioncaptioningid"></a>ClosedCaption.captioningID

La **propiedad captioningID** especifica o recupera el nombre del elemento que muestra los subtítulos.

``` syntax
player.closedCaption.captioningID
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de lectura y **escritura.**

## <a name="remarks"></a>Observaciones

El nombre del elemento especificado puede ser cualquier elemento HTML de la página web, siempre que admita el atributo innerHTML. Si la página web contiene varios fotogramas, el nombre del elemento solo puede hacer referencia a un elemento en el mismo marco que el control Player.

**Reproductor de Windows Media 10 Mobile:** Esta propiedad es de solo lectura y siempre devuelve una cadena vacía.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo JScript de Microsoft se *usa ClosedCaption*. **captioningID para** elegir el área de una página web que se usa para mostrar subtítulos. Se crearon dos elementos DIV HTML, con ID = CC1 e ID = CC2, respectivamente. El **objeto Player** se creó con id. = "Player".


```JScript
<!-- Create two HTML BUTTON elements to allow the user to choose a display region. -->
<INPUT TYPE = "BUTTON"  NAME = "SET1"  VALUE = "Move Caption to CC1"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC2.innerHTML = 'This is the CC2 DIV';

           /* Show the captions in the DIV named CC1. */ 
           Player.ClosedCaption.captioningID = 'CC1';
          ">

<INPUT TYPE = "BUTTON" NAME = "SET2" VALUE = "Move Caption to CC2"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC1.innerHTML = 'This is the CC1 DIV';

           /* Show the captions in the DIV named CC2. */
           Player.ClosedCaption.captioningID = 'CC2';
          ">

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption (objeto)**](closedcaption-object.md)
</dt> </dl>

 

 





