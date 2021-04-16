---
title: Propiedad SAMIFileName de IWMPClosedCaption
description: La propiedad SAMIFileName obtiene o establece el nombre de un archivo que contiene la información necesaria para los subtítulos (CC).
ms.assetid: c3162c5f-9d66-41d4-920c-ed9840742d9d
keywords:
- Propiedades de SAMIFileName Media Player de Windows
- Propiedad SAMIFileName de Windows Media Player, interfaz IWMPClosedCaption
- Interfaz IWMPClosedCaption Windows Media Player, propiedad SAMIFileName
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649909"
---
# <a name="iwmpclosedcaptionsamifilename-property"></a>IWMPClosedCaption:: SAMIFileName (propiedad)

La propiedad **SAMIFileName** obtiene o establece el nombre de un archivo que contiene la información necesaria para los subtítulos (CC).

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String SAMIFileName {get; set;}
```


```VB

Public Property SAMIFileName As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System. String** que es el nombre del archivo de intercambio multimedia accesible (Sami) sincronizado.

## <a name="remarks"></a>Observaciones

El archivo SAMI debe utilizar una extensión de nombre de archivo. SMI o. Sami.

Si no establece un valor mediante **SAMIFileName**, esta propiedad obtiene una **cadena** que contiene el nombre de archivo o la dirección URL predeterminados asociados al elemento multimedia actual. Esta asociación puede producirse cuando se especifica un archivo SAMI mediante el parámetro de dirección URL *Sami* , o automáticamente cuando el archivo Sami tiene el mismo nombre que el archivo multimedia digital (excepto la extensión de nombre de archivo). Si no hay ningún archivo SAMI predeterminado asociado al medio actual, esta propiedad obtiene una cadena de longitud cero ("").

Una vez que se establece un valor mediante **SAMIFileName**, ese valor se conserva hasta que se establece un nuevo valor (o hasta que se abre un nuevo elemento multimedia mediante el parámetro de dirección URL de Sami). Por lo tanto, debe establecer un nuevo valor para esta propiedad antes de reproducir cada nuevo elemento multimedia. De este modo, el nuevo valor de **SAMIFileName** tendrá efecto cuando se abra el siguiente elemento multimedia (o cuando se llame a **AxWindowsMediaPlayer. Close** ). Especificar un nuevo valor para **SAMIFileName** no tiene ningún efecto en el medio actual.

Para hacer que Windows Media Player use el archivo SAMI predeterminado asociado a un elemento multimedia determinado, establezca **SAMIFileName** en una cadena de longitud cero ("") antes de reproducir el siguiente elemento multimedia.

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

[**AxWindowsMediaPlayer. Close**](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption (VB y C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption2 (VB y C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





