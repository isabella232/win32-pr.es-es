---
title: ClosedCaption.SAMIFileName
description: La propiedad SAMIFileName especifica o recupera el nombre del archivo que contiene la información necesaria para los subtítulos (CC).
ms.assetid: f2090500-6c9f-4d2d-9855-a9c193b00a41
keywords:
- ClosedCaption. SAMIFileName Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIFileName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd748076eec80b5b7d97e7c041f454c4f9193f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699538"
---
# <a name="closedcaptionsamifilename"></a>ClosedCaption.SAMIFileName

La propiedad **SAMIFileName** especifica o recupera el nombre del archivo que contiene la información necesaria para los subtítulos (CC).

``` syntax
player.closedCaption.SAMIFileName
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de lectura/escritura.

## <a name="remarks"></a>Observaciones

El archivo de intercambio multimedia accesible sincronizado (SAMI) debe utilizar una extensión de nombre de archivo. SMI o. Sami.

Si no especifica un valor para **SAMIFileName**, esta propiedad recupera una cadena que contiene el nombre de archivo o la dirección URL asociada al elemento multimedia actual. Esta asociación puede producirse cuando se especifica un archivo SAMI mediante el parámetro de dirección URL *Sami* , o de forma automática cuando el archivo Sami tiene el mismo nombre que el archivo multimedia digital (excepto la extensión de nombre de archivo). Si no hay ningún archivo SAMI asociado al medio actual, esta propiedad recupera una cadena vacía ("").

Una vez que se especifica un valor para **SAMIFileName**, ese valor se conserva hasta que se especifique un nuevo valor (o hasta que se abra un nuevo elemento multimedia mediante el parámetro de dirección URL de *Sami* ). Por lo tanto, debe especificar un nuevo valor para esta propiedad antes de reproducir cada nuevo elemento multimedia. De este modo, el nuevo valor de **SAMIFileName** tendrá efecto cuando se abra el siguiente elemento multimedia (o cuando el *reproductor*.**** se llama a Close). Especificar un nuevo valor para **SAMIFileName** no tiene ningún efecto en el medio actual.

Para hacer que Windows Media Player vuelva a usar el archivo SAMI asociado a un elemento multimedia determinado, especifique un valor para **SAMIFileName** igual a una cadena vacía ("") antes de reproducir el siguiente elemento multimedia.

**Windows Media Player 10 Mobile:** Esta propiedad es de solo lectura y siempre devuelve una cadena vacía.

## <a name="examples"></a>Ejemplos

En los siguientes tres ejemplos de JScript se usa *ClosedCaption*. **SAMIFileName** para especificar el nombre de un archivo de texto de subtítulos. El objeto **Player** se creó con ID = "Player".


```JScript
// Display the closed captions from a website.
Player.closedCaption.SAMIFileName="https://www.proseware.com/ccsample.smi";

// Display the closed captions from a local network.
// You must add an escape sequence of a backslash for every original backslash.
Player.closedCaption.SAMIFileName="\\\\yourservername\\Public\\ccsample.smi";

// Display the closed captions from a file on a local drive.
// Be sure to add the appropriate escape sequences.
Player.closedCaption.SAMIFileName="C:\\WMSDK\\WMPSDK9\\samples\\media\\ccsample.smi";

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Agregar subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objeto ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**Player. Close**](player-close.md)
</dt> </dl>

 

 





