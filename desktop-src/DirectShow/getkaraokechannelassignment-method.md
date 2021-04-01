---
description: El método GetKaraokeChannelAssignment recupera un valor que indica cómo se asignan los canales de karaoke a los altavoces.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: Método GetKaraokeChannelAssignment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafe1217e08f3dc4f55aeec42424b1ebf9d86d22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906896"
---
# <a name="getkaraokechannelassignment-method"></a>Método GetKaraokeChannelAssignment

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `GetKaraokeChannelAssignment` método recupera un valor que indica cómo se asignan los canales de karaoke a los altavoces.

``` syntax
[ iAssignment = ] MSWebDVD.GetKaraokeChannelAssignment(iStream)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Especifica la secuencia de audio como un entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un entero que indica la asignación de altavoz para la secuencia especificada.



| Código devuelto | Descripción                                                             |
|-------------|-------------------------------------------------------------------------|
| 2           | La secuencia se asigna a los altavoces izquierdo y derecho.                  |
| 3           | La secuencia se asigna a los altavoces izquierdo, derecho y medio.         |
| 4           | La secuencia se asigna a los altavoces izquierdo, derecho y AUDIO1.         |
| 5           | La secuencia se asigna a los altavoces izquierdo, derecho, medio y AUDIO1. |
| 6           | La secuencia se asigna a los altavoces izquierdo, derecho y Audio2.         |
| 7           | La secuencia se asigna a los altavoces izquierdo, derecho, medio y Audio2. |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



