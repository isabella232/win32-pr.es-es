---
title: IWMPClosedCaption SAMIFileName, propiedad
description: La propiedad SAMIFileName obtiene o establece el nombre de un archivo que contiene la información necesaria para el subtítulo.
ms.assetid: c3162c5f-9d66-41d4-920c-ed9840742d9d
keywords:
- Propiedad SAMIFileName Reproductor de Windows Media
- Propiedad SAMIFileName Reproductor de Windows Media , interfaz IWMPClosedCaption
- Interfaz IWMPClosedCaption Reproductor de Windows Media , propiedad SAMIFileName
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIFileName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251f2bbf0c8839ab9a0005c69e1869c47af16ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242978"
---
# <a name="iwmpclosedcaptionsamifilename-property"></a>IWMPClosedCaption::SAMIFileName, propiedad

La **propiedad SAMIFileName** obtiene o establece el nombre de un archivo que contiene la información necesaria para el subtítulo.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String SAMIFileName {get; set;}
```


```VB

Public Property SAMIFileName As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System.String que** es el nombre del archivo synchronized Accessible Media Interchange (SAMI).

## <a name="remarks"></a>Observaciones

El archivo SAMI debe usar una extensión de nombre de archivo .smi o .sami.

Si no establece un valor mediante **SAMIFileName**  , esta propiedad obtiene una cadena que contiene el nombre de archivo predeterminado o la dirección URL asociada al elemento multimedia actual. Esta asociación puede producirse cuando se especifica un archivo SAMI mediante el parámetro *sami* URL o automáticamente cuando el archivo SAMI tiene el mismo nombre que el archivo multimedia digital (excepto para la extensión de nombre de archivo). Si no hay ningún archivo SAMI predeterminado asociado al medio actual, esta propiedad obtiene una cadena de longitud cero ("").

Una vez establecido un valor mediante **SAMIFileName**, ese valor se conserva hasta que se establece un nuevo valor (o hasta que se abre un nuevo elemento multimedia mediante el parámetro sami URL). Por lo tanto, debe establecer un nuevo valor para esta propiedad antes de reproducir cada nuevo elemento multimedia. De este modo, el nuevo valor de **SAMIFileName** se hará efectivo cuando se abra el siguiente elemento multimedia (o cuando se llame a **AxWindowsMediaPlayer.close).** Especificar un nuevo valor para **SAMIFileName** no tiene ningún efecto para el medio actual.

Para hacer Reproductor de Windows Media el archivo SAMI predeterminado asociado a un elemento multimedia determinado, establezca **SAMIFileName** en una cadena de longitud cero ("") antes de reproducir el siguiente elemento multimedia.

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

[**AxWindowsMediaPlayer.close**](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption (VB y C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption2 (VB y C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





