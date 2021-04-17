---
title: Propiedad SAMILang de IWMPClosedCaption
description: La propiedad SAMILang obtiene o establece el idioma que se muestra para los subtítulos (CC).
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- Propiedades de SAMILang Media Player de Windows
- Propiedad SAMILang de Windows Media Player, interfaz IWMPClosedCaption
- Interfaz IWMPClosedCaption Windows Media Player, propiedad SAMILang
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
ms.openlocfilehash: fe29defa3736795c88613ee7ab2ef11a914a3f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709196"
---
# <a name="iwmpclosedcaptionsamilang-property"></a>IWMPClosedCaption:: SAMILang (propiedad)

La propiedad **SAMILang** obtiene o establece el idioma que se muestra para los subtítulos (CC).

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System. String** que es el nombre especificado en el identificador de idioma de un archivo Sami.

## <a name="remarks"></a>Observaciones

Un archivo SAMI puede contener texto para uno o varios idiomas. Los idiomas disponibles para subtítulos (CC) se definen entre las etiquetas <STYLE> y </STYLE> del archivo Sami. Un identificador de idioma se especifica con una cadena alfanumérica única precedida de un punto (.). El nombre especificado para un idioma puede ser cualquier cadena. Por ejemplo, se puede utilizar lo siguiente para definir el Inglés de EE. UU.:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



Si no se especifica ningún idioma SAMI, se usa de forma predeterminada el primer idioma definido en el archivo SAMI.

La cadena que establezca mediante **SAMILang** debe coincidir con el atributo **Name** del especificador de idioma.

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

 

 





