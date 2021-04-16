---
title: IWMPDVD. isAvailable (VB y C)
description: La propiedad isAvailable (el \_ método get isavailable en C \) obtiene un valor que indica si un tipo de información especificado está disponible o se puede realizar una acción especificada.
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- IWMPDVD. isAvailable (VB y C) Windows Media Player
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
ms.openlocfilehash: 2e3409da619f337b61606baaf546cebbb438087c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690688"
---
# <a name="iwmpdvdisavailable-vb-and-c"></a>IWMPDVD. isAvailable (VB y C#)

La propiedad **isavailable** (el método **Get \_ isavailable** en C#) obtiene un valor que indica si un tipo de información especificado está disponible o se puede realizar una acción especificada.


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

System. String que es uno de los valores siguientes.



| Value      | Descripción                                                                                   |
|------------|-----------------------------------------------------------------------------------------------|
| atrás       | Detecta si el método **IWMPDVD. back** está disponible.                                   |
| discos        | Detecta si el DVD está cargado.                                                          |
| dvdDecoder | Detecta si el descodificador de DVD está instalado en el sistema.                                     |
| resume     | Detecta si el método **IWMPDVD. resume** está disponible.                                 |
| titleMenu  | Detecta si el método **IWMPDVD. titleMenu** está disponible.                              |
| Menú de menús    | Detecta si el método **IWMPDVD. webmenu** está disponible. Normalmente denominado menú raíz. |



 

## <a name="property-value"></a>Valor de propiedad

**System.Boolean**

**System. Boolean** que indica si un tipo de información especificado está disponible o se puede realizar una acción especificada.

## <a name="remarks"></a>Observaciones

Las características de DVD de Windows Media Player no funcionarán en equipos que no tengan instalado un descodificador de DVD. Puede determinar si un descodificador está disponible llamando a la propiedad **isavailable** (el método **Get \_ isavailable** en C#) y pasando el valor **System. String** "dvdDecoder".

Cada DVD se crea de forma diferente. Los métodos disponibles durante la reproducción y la navegación por DVD dependen de cómo se cree el DVD.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPDVD (VB y C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. back (VB y C#)**](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. resume (VB y C#)**](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. titleMenu (VB y C#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. webmenu (VB y C#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





