---
title: Propiedad invokeURLs de IWMPSettings
description: La propiedad invokeURLs obtiene o establece un valor que indica si los eventos de dirección URL deben iniciar un explorador Web.
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- propiedades de invokeURLs Media Player de Windows
- propiedad invokeURLs de Windows Media Player, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, propiedad invokeURLs
topic_type:
- apiref
api_name:
- IWMPSettings.invokeURLs
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbdd68d797b54f4e9365f381b2b5c705dffc419b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105719026"
---
# <a name="iwmpsettingsinvokeurls-property"></a>IWMPSettings:: invokeURLs (propiedad)

La propiedad **invokeURLs** obtiene o establece un valor que indica si los eventos de dirección URL deben iniciar un explorador Web.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Boolean invokeURLs {get; set;}
```


```VB

Public Property invokeURLs As System.Boolean
```





## <a name="property-value"></a>Valor de propiedad

Un valor **System. Boolean** que indica si los eventos de dirección URL deben iniciar un explorador Web. El valor predeterminado es **true**.

## <a name="remarks"></a>Observaciones

Los archivos multimedia digitales y las secuencias pueden contener comandos de script de dirección URL. Cuando se envía un comando de script de dirección URL al control Media Player de Windows, se pasa primero al controlador de eventos **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** , independientemente del valor recuperado por **invokeURLs**. Después de que **\_ WMPOCXEvents \_ ScriptCommandEvent** se cierre, Windows Media Player comprueba **invokeURLs** para determinar si se debe iniciar el explorador Web predeterminado con la dirección URL. Puede mostrar las direcciones URL de forma selectiva al comprobarlas en **\_ WMPOCXEvents \_ ScriptCommandEvent** y establecer **invokeURLs** como desee.

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

 

 





