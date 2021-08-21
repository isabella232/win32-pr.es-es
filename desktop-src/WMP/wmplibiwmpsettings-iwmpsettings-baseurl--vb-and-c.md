---
title: IWMPSettings baseURL, propiedad
description: La propiedad baseURL obtiene o establece la dirección URL base usada para la resolución de rutas de acceso relativas con comandos de script de dirección URL insertados en el contenido multimedia digital.
ms.assetid: e136303f-ba08-434f-ad7e-9fffa66785c4
keywords:
- baseURL, propiedad Reproductor de Windows Media
- BaseURL property Reproductor de Windows Media , IWMPSettings (interfaz)
- Interfaz IWMPSettings Reproductor de Windows Media , propiedad baseURL
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
ms.openlocfilehash: a3224a43a2689fd49dee2b2a66cc768250b1a829e61863d8cfbd029e3cdf783c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568438"
---
# <a name="iwmpsettingsbaseurl-property"></a>Propiedad IWMPSettings::baseURL

La **propiedad baseURL** obtiene o establece la dirección URL base usada para la resolución de rutas de acceso relativas con comandos de script de dirección URL insertados en el contenido multimedia digital.

## <a name="syntax"></a>Syntax


```CSharp
public System.String baseURL {get; set;}
```


```VB

Public Property baseURL As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System.String que** es la dirección URL base.

## <a name="remarks"></a>Comentarios

Esta propiedad especifica la dirección URL HTTP base que el evento **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent pasa** como parámetro de comando. La dirección URL base se concatena con la dirección URL relativa como se muestra a continuación:

1.  Se agrega una barra diagonal final (/) al valor recuperado por la **propiedad baseURL.**
2.  Se elimina un punto inicial, una barra diagonal o un carácter de barra diagonal (., \\ y /) de la dirección URL relativa.
3.  La dirección URL relativa se agrega al final de la dirección URL base.
4.  Todos los caracteres de barra diagonal de la dirección URL completa resultante apuntan en la misma dirección (convertida a barras diagonales o hacia atrás) en función de la dirección del primer carácter de barra diagonal encontrado en la nueva dirección URL.

**Nota**

El Reproductor de Windows Media control no admite el uso de dos puntos (..) en la dirección URL relativa para indicar el elemento primario de la ubicación actual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Evento AxWindowsMediaPlayer.ScriptCommand (VB y C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





