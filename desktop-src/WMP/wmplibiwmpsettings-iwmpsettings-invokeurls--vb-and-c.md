---
title: Propiedad invokeURLs de IWMPSettings
description: La propiedad invokeURLs obtiene o establece un valor que indica si los eventos de dirección URL deben iniciar un explorador web.
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- Propiedades invokeURLs Reproductor de Windows Media
- Propiedades invokeURLs Reproductor de Windows Media , interfaz IWMPSettings
- Interfaz IWMPSettings Reproductor de Windows Media , propiedad invokeURLs
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
ms.openlocfilehash: dba44af7e6ec700f9df810486acb57af24a14c9e5d4966fddbfe4b242d346a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053433"
---
# <a name="iwmpsettingsinvokeurls-property"></a>Propiedad IWMPSettings::invokeURLs

La **propiedad invokeURLs** obtiene o establece un valor que indica si los eventos de dirección URL deben iniciar un explorador web.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean invokeURLs {get; set;}
```


```VB

Public Property invokeURLs As System.Boolean
```





## <a name="property-value"></a>Valor de propiedad

Valor **System.Boolean** que indica si los eventos de dirección URL deben iniciar un explorador web. El valor predeterminado es **true**.

## <a name="remarks"></a>Comentarios

Los archivos multimedia digitales y las secuencias pueden contener comandos de script de dirección URL. Cuando se envía un comando de script de dirección URL al control Reproductor de Windows Media, se pasa primero al controlador de eventos **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** independientemente del valor recuperado por **invokeURLs**. Una vez que se cierra **\_ WMPOCXEvents \_ ScriptCommandEvent,** Reproductor de Windows Media comprueba **invokeURLs** para determinar si se debe iniciar el explorador web predeterminado con la dirección URL. Puede mostrar las direcciones URL de forma selectiva si las comprueba en **\_ \_ ScriptCommandEvents WMPOCXEvents** y establece **invokeURLs según** sea necesario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Evento AxWindowsMediaPlayer.ScriptCommand (VB y C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





