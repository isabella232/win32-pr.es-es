---
title: Propiedad IWMPClosedCaption SAMIStyle
description: La propiedad SAMIStyle obtiene o establece el estilo de subtítulos.
ms.assetid: 0b1f92c6-b659-4ade-90c8-62a06e475f5c
keywords:
- Propiedad SAMIStyle Reproductor de Windows Media
- Propiedad SAMIStyle Reproductor de Windows Media , interfaz IWMPClosedCaption
- Interfaz IWMPClosedCaption Reproductor de Windows Media , propiedad SAMIStyle
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIStyle
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e147b48ffb80e1114133b59018cef514eefd2ae7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242972"
---
# <a name="iwmpclosedcaptionsamistyle-property"></a>Propiedad IWMPClosedCaption::SAMIStyle

La **propiedad SAMIStyle** obtiene o establece el estilo de subtítulos.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String SAMIStyle {get; set;}
```


```VB

Public Property SAMIStyle As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System.String que** es el nombre especificado en el identificador de estilo de un archivo SAMI.

## <a name="remarks"></a>Observaciones

Un archivo SAMI puede contener varias definiciones de estilo de formato. Los estilos SAMI se definen entre &lt; style &gt; y </STYLE> etiquetas en el archivo SAMI. Un estilo se define con una cadena de texto precedida de un \# carácter. Por ejemplo:


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}
```



Especifica un estilo que genera una fuente determinada.

Si no se especifica ningún estilo SAMI, el primer estilo definido en el archivo SAMI se usa de forma predeterminada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption (VB y C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption2 (VB y C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





