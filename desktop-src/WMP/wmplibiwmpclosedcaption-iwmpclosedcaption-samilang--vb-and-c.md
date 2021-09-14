---
title: Propiedad IWMPClosedCaption SAMILang
description: La propiedad SAMILang obtiene o establece el idioma que se muestra para los subtítulos.
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- Propiedad SAMILang Reproductor de Windows Media
- Propiedad SAMILang Reproductor de Windows Media , interfaz IWMPClosedCaption
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
ms.openlocfilehash: a9577f7d9030a12a12596fe2cdc2a999922658ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359434"
---
# <a name="iwmpclosedcaptionsamilang-property"></a>Propiedad IWMPClosedCaption::SAMILang

La **propiedad SAMILang** obtiene o establece el idioma que se muestra para los subtítulos.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System.String que** es el nombre especificado en el identificador de idioma de un archivo SAMI.

## <a name="remarks"></a>Observaciones

Un archivo SAMI puede contener texto para uno o varios idiomas. Los idiomas disponibles para los subtítulos se definen entre &lt; style &gt; y </STYLE> etiquetas en el archivo SAMI. Un identificador de idioma se especifica con una cadena alfanumérica única precedida de un punto (.). El nombre especificado para un idioma puede ser cualquier cadena. Por ejemplo, se podría usar lo siguiente para definir el inglés de EE. UU.:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



Si no se especifica ningún lenguaje SAMI, se usa de forma predeterminada el primer idioma definido en el archivo SAMI.

La cadena que establezca mediante **SAMILang** debe coincidir con el **atributo Name** del especificador de lenguaje.

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

 

 





