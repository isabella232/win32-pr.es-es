---
title: IWMPDVD.isAvailable (VB y C )
description: La propiedad isAvailable (el método get isAvailable en C\) obtiene un valor que indica si un tipo de información especificado está disponible o si se puede realizar una \_ acción especificada.
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- IWMPDVD.isAvailable (VB y C ) Reproductor de Windows Media
topic_type:
- apiref
api_name:
- IWMPDVD.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78c9dda7bff764752dc55524000ccd3695863afe69dcf45c2ed971c9c0373fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415933"
---
# <a name="iwmpdvdisavailable-vb-and-c"></a>IWMPDVD.isAvailable (VB y C#)

La **propiedad isAvailable** (el método **get \_ isAvailable** en C#) obtiene un valor que indica si un tipo especificado de información está disponible o si se puede realizar una acción especificada.


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
)
```



## <a name="parameters"></a>Parámetros

*bstrItem*

System.String que es uno de los valores siguientes.



| Value      | Descripción                                                                                   |
|------------|-----------------------------------------------------------------------------------------------|
| atrás       | Detecta si el **método IWMPDVD.back** está disponible.                                   |
| Dvd        | Detecta si el DVD está cargado.                                                          |
| dvdDecoder | Detecta si el descodificador de DVD está instalado en el sistema.                                     |
| resume     | Detecta si el **método IWMPDVD.resume** está disponible.                                 |
| titleMenu  | Detecta si el **método IWMPDVD.titleMenu** está disponible.                              |
| topMenu    | Detecta si el **método IWMPDVD.topMenu** está disponible. Normalmente se denomina menú raíz. |



 

## <a name="property-value"></a>Valor de propiedad

**System.Boolean**

**System.Boolean que** indica si un tipo de información especificado está disponible o se puede realizar una acción especificada.

## <a name="remarks"></a>Observaciones

Las características de DVD Reproductor de Windows Media no funcionarán en equipos que no tengan instalado un descodificador de DVD. Puede determinar si un descodificador está disponible llamando a la propiedad **isAvailable** (el método **get \_ isAvailable** en C#) y pasando el valor **System.String** "dvdDecoder".

Cada DVD se ha escrito de forma diferente. Los métodos disponibles durante la reproducción y navegación de DVD dependen de cómo se cree el DVD.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPDVD (VB y C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPDVD.back (VB y C#)**](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)
</dt> <dt>

[**IWMPDVD.resume (VB y C#)**](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)
</dt> <dt>

[**IWMPDVD.titleMenu (VB y C#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> <dt>

[**IWMPDVD.topMenu (VB y C#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





