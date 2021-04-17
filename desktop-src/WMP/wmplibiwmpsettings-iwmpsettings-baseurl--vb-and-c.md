---
title: IWMPSettings baseURL (propiedad)
description: La propiedad baseURL obtiene o establece la dirección URL base que se usa para la resolución de la ruta de acceso relativa con comandos de script de dirección URL que se incrustan en contenido multimedia digital.
ms.assetid: e136303f-ba08-434f-ad7e-9fffa66785c4
keywords:
- propiedad baseURL Media Player de Windows
- propiedad baseURL Windows Media Player, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, propiedad baseURL
topic_type:
- apiref
api_name:
- IWMPSettings.baseURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 393575a93bf904f6fe312b13647ad5a7557b15bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718621"
---
# <a name="iwmpsettingsbaseurl-property"></a>IWMPSettings:: baseURL (propiedad)

La propiedad **baseurl** obtiene o establece la dirección URL base que se usa para la resolución de la ruta de acceso relativa con comandos de script de dirección URL que se incrustan en contenido multimedia digital.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String baseURL {get; set;}
```


```VB

Public Property baseURL As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System. String** que es la dirección URL base.

## <a name="remarks"></a>Observaciones

Esta propiedad especifica la dirección URL HTTP base que se pasa como parámetro de comando por el evento **\_ \_ ScriptCommandEvent de WMPOCXEvents de AxWindowsMediaPlayer** . La dirección URL base se concatena con la dirección URL relativa como se indica a continuación:

1.  Se agrega una barra diagonal final (/) al valor recuperado por la propiedad **baseurl** .
2.  Un punto inicial, una barra diagonal inversa o un carácter de barra diagonal (., \\ , y/) se eliminan de la dirección URL relativa.
3.  La dirección URL relativa se agrega al final de la dirección URL base.
4.  Todos los caracteres de barra diagonal en la dirección URL completa resultante se señalan en la misma dirección (convertida en barras diagonales o hacia atrás) en función de la dirección del primer carácter de barra diagonal que se encuentre en la nueva dirección URL.

**Note**

El control Media Player de Windows no admite el uso de dos puntos (..) en la dirección URL relativa para indicar el elemento primario de la ubicación actual.

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

 

 





