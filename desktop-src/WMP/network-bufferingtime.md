---
title: Network.bufferingTime
description: La propiedad bufferingTime especifica o recupera la cantidad de tiempo en milisegundos asignada para almacenar en búfer los datos entrantes antes de que comience la reproducción.
ms.assetid: b52b7f44-6be1-4299-94da-c37d758795af
keywords:
- Network.bufferingTime Reproductor de Windows Media
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
ms.openlocfilehash: afe4a68a7ad1ae8a1444f1e2f31ad09461e05d221e8fceae52960bd5927aac0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901735"
---
# <a name="networkbufferingtime"></a>Network.bufferingTime

La **propiedad bufferingTime** especifica o recupera la cantidad de tiempo en milisegundos asignada para almacenar en búfer los datos entrantes antes de que comience la reproducción.

## <a name="syntax"></a>Syntax

*player*. *network*. **bufferingTime**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de lectura y **escritura** **(long)** que va de cero a 60 000 con un valor predeterminado de 5000.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **bufferingTime para** especificar el número de segundos asignados para almacenar en búfer los datos entrantes. La información se recupera de un elemento HTML TEXT INPUT creado con id. = "bufText". El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> </dl>

 

 





