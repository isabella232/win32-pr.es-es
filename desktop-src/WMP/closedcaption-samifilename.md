---
title: ClosedCaption.SAMIFileName
description: La propiedad SAMIFileName especifica o recupera el nombre del archivo que contiene la información necesaria para el subtítulo.
ms.assetid: f2090500-6c9f-4d2d-9855-a9c193b00a41
keywords:
- ClosedCaption.SAMIFileName Reproductor de Windows Media
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
ms.openlocfilehash: 22ba314208db3cb5529042011f269f026a4cf2bd4d4b01d1b8d64719b96a5f90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119516"
---
# <a name="closedcaptionsamifilename"></a>ClosedCaption.SAMIFileName

La **propiedad SAMIFileName** especifica o recupera el nombre del archivo que contiene la información necesaria para el subtítulo.

``` syntax
player.closedCaption.SAMIFileName
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de lectura y **escritura.**

## <a name="remarks"></a>Comentarios

El archivo synchronized Accessible Media Interchange (SAMI) debe usar una extensión de nombre de archivo .smi o .sami.

Si no especifica un valor para **SAMIFileName**, esta propiedad recupera una cadena que contiene el nombre de archivo o la dirección URL asociada al elemento multimedia actual. Esta asociación puede producirse cuando se especifica un archivo SAMI mediante el parámetro *sami* URL o automáticamente cuando el archivo SAMI tiene el mismo nombre que el nombre del archivo multimedia digital (excepto para la extensión de nombre de archivo). Si no hay ningún archivo SAMI asociado al medio actual, esta propiedad recupera una cadena vacía ("").

Una vez que se especifica un valor para **SAMIFileName**, ese valor se conserva hasta que se especifica un nuevo valor (o hasta que se abre un nuevo elemento multimedia mediante el parámetro *sami* URL). Por lo tanto, debe especificar un nuevo valor para esta propiedad antes de reproducir cada nuevo elemento multimedia. De este modo, el nuevo valor de **SAMIFileName** tendrá efecto cuando se abra el siguiente elemento multimedia (o cuando el *Reproductor de*.**se** llama a close). Especificar un nuevo valor para **SAMIFileName** no tiene ningún efecto para el medio actual.

Para que Reproductor de Windows Media vuelva a usar el archivo SAMI asociado a un elemento multimedia determinado, especifique un valor para **SAMIFileName** igual a una cadena vacía ("") antes de reproducir el siguiente elemento multimedia.

**Reproductor de Windows Media 10 Mobile:** Esta propiedad es de solo lectura y siempre devuelve una cadena vacía.

## <a name="examples"></a>Ejemplos

En los tres ejemplos JScript siguientes se *usa ClosedCaption*. **SAMIFileName para** especificar el nombre de un archivo de texto de título cerrado. El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption (objeto)**](closedcaption-object.md)
</dt> <dt>

[**Player.close**](player-close.md)
</dt> </dl>

 

 





