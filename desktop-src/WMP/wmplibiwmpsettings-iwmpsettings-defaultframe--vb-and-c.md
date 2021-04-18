---
title: Propiedad defaultFrame de IWMPSettings
description: La propiedad defaultFrame obtiene o establece el nombre del marco que se usa para mostrar una dirección URL que se recibe en \_ un \_ evento AxWindowsMediaPlayer WMPOCXEvents ScriptCommandEvent.
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- propiedades de defaultFrame Media Player de Windows
- propiedad defaultFrame de Windows Media Player, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, propiedad defaultFrame
topic_type:
- apiref
api_name:
- IWMPSettings.defaultFrame
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28539640214165ab5b2808762ed854b19b434311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718698"
---
# <a name="iwmpsettingsdefaultframe-property"></a>IWMPSettings::d propiedad efaultFrame

La propiedad **defaultFrame** obtiene o establece el nombre del marco que se usa para mostrar una dirección URL que se recibe en un evento **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** .

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String defaultFrame {get; set;}
```


```VB

Public Property defaultFrame As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System. String** que es el valor del atributo name del elemento de **marco** de destino.

## <a name="remarks"></a>Observaciones

Si se especifica un marco de destino en el propio evento **\_ WMPOCXEvents \_ ScriptCommandEvent** , esta propiedad se omite.

Esta propiedad se omite cuando se usa el applet Java de Netscape Navigator. En Netscape Navigator, cada comando de script de dirección URL recibido mostrará la dirección URL en una nueva ventana del explorador, independientemente del valor de **defaultFrame**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Evento AxWindowsMediaPlayer. comando (VB y C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





