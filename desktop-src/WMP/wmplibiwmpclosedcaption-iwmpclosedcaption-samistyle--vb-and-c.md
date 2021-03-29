---
title: Propiedad SAMIStyle de IWMPClosedCaption
description: La propiedad SAMIStyle obtiene o establece el estilo de subtítulos (CC).
ms.assetid: 0b1f92c6-b659-4ade-90c8-62a06e475f5c
keywords:
- Propiedades de SAMIStyle Media Player de Windows
- Propiedad SAMIStyle de Windows Media Player, interfaz IWMPClosedCaption
- Interfaz IWMPClosedCaption Windows Media Player, propiedad SAMIStyle
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
ms.openlocfilehash: 9bd0b48fc1807d6ca1854651c7f222183a845be3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650147"
---
# <a name="iwmpclosedcaptionsamistyle-property"></a>IWMPClosedCaption:: SAMIStyle (propiedad)

La propiedad **SAMIStyle** obtiene o establece el estilo de subtítulos (CC).

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String SAMIStyle {get; set;}
```


```VB

Public Property SAMIStyle As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System. String** que es el nombre especificado en el identificador de estilo de un archivo Sami.

## <a name="remarks"></a>Observaciones

Un archivo SAMI puede contener varias definiciones de estilo de formato. Los estilos SAMI se definen entre las etiquetas <STYLE> y </STYLE> del archivo Sami. Un estilo se define con una cadena de texto precedida por un \# carácter. Por ejemplo:


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}
```



Especifica un estilo que genera una fuente determinada.

Si no se especifica ningún estilo SAMI, se usa de forma predeterminada el primer estilo definido en el archivo SAMI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Agregar subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption (VB y C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption2 (VB y C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





