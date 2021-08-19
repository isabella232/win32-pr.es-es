---
title: IWMPClosedCaption, propiedad SAMILang
description: La propiedad SAMILang obtiene o establece el idioma que se muestra para los subtítulos.
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- Propiedad SAMILang Reproductor de Windows Media
- Propiedad SAMILang Reproductor de Windows Media interfaz , IWMPClosedCaption
- Interfaz IWMPClosedCaption Reproductor de Windows Media , propiedad SAMILang
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMILang
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98354d5e1e4f796442dd0347a4ed2796cafdf7297d3829af9b8839d48df00c3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930318"
---
# <a name="iwmpclosedcaptionsamilang-property"></a>IWMPClosedCaption::SAMILang, propiedad

La **propiedad SAMILang** obtiene o establece el idioma que se muestra para los subtítulos.

## <a name="syntax"></a>Syntax


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System.String que** es el nombre especificado en el identificador de idioma de un archivo SAMI.

## <a name="remarks"></a>Comentarios

Un archivo SAMI puede contener texto para uno o varios idiomas. Los idiomas disponibles para subtítulos se definen entre las <STYLE> etiquetas y </STYLE> del archivo SAMI. Un identificador de idioma se especifica con una cadena alfanumérica única precedida de un punto (.). El nombre especificado para un idioma puede ser cualquier cadena. Por ejemplo, se podría usar lo siguiente para definir el inglés de EE. UU.:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



Si no se especifica ningún lenguaje SAMI, se usa el primer idioma definido en el archivo SAMI de forma predeterminada.

La cadena que establezca mediante **SAMILang** debe coincidir con el **atributo Name** del especificador de lenguaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





