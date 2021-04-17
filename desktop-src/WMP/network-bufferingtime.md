---
title: Network. bufferingTime
description: La propiedad bufferingTime especifica o recupera la cantidad de tiempo en milisegundos asignados para almacenar en búfer los datos entrantes antes de comenzar la reproducción.
ms.assetid: b52b7f44-6be1-4299-94da-c37d758795af
keywords:
- Windows Media Player de red. bufferingTime
topic_type:
- apiref
api_name:
- Network.bufferingTime
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b805173403268afff473db427b58193382afe6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708306"
---
# <a name="networkbufferingtime"></a>Network. bufferingTime

La propiedad **bufferingTime** especifica o recupera la cantidad de tiempo en milisegundos asignados para almacenar en búfer los datos entrantes antes de comenzar la reproducción.

## <a name="syntax"></a>Sintaxis

*reproductor*. *red*. **bufferingTime**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de lectura y escritura (**Long**) que va desde cero hasta 60.000 con un valor predeterminado de 5.000.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *Network*. **bufferingTime** para especificar el número de segundos asignados para almacenar en búfer los datos entrantes. La información se recupera de un elemento de entrada de texto HTML creado con ID = "bufText". El objeto **Player** se creó con ID = "Player".


```JScript
<!-- Create a BUTTON element to change the bufferingTime value. -->
<INPUT TYPE = "BUTTON" NAME = "bufTime" ID = "bufTime" 
       VALUE = "Change Buffer Time"

    onClick = "
       /* Test whether the user entered a valid value. */
       if (bufText.value >= 0 & bufText.value <= 60) 
           Player.network.bufferingTime = bufText.value * 1000;
       else
           alert('Buffering time must be between 0 and 60.');
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> </dl>

 

 





