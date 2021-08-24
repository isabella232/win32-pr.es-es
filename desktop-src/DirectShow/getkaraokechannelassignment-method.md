---
description: El método GetKaraokeChannelAssignment recupera un valor que indica cómo se asignan los canales de canal a los hablantes.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: GetKaraokeChannelAssignment (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 010e8112ece9b3fc66831055995ebf46657d4216942ac3b9dee05b1b68d18761
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812555"
---
# <a name="getkaraokechannelassignment-method"></a>GetKaraokeChannelAssignment (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El método recupera un valor que indica cómo se asignan los `GetKaraokeChannelAssignment` canales de canal a los hablantes.

``` syntax
[ iAssignment = ] MSWebDVD.GetKaraokeChannelAssignment(iStream)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Especifica la secuencia de audio como un entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un entero que indica la asignación del hablante para la secuencia especificada.



| Código devuelto | Descripción                                                             |
|-------------|-------------------------------------------------------------------------|
| 2           | La secuencia se asigna a los altavoces izquierdo y derecho.                  |
| 3           | La secuencia se asigna a los altavoces izquierdo, derecho y central.         |
| 4           | La secuencia se asigna a los altavoces izquierdo, derecho y audio1.         |
| 5           | La secuencia se asigna a los altavoces left, right, middle y audio1. |
| 6           | La secuencia se asigna a los altavoces izquierdo, derecho y audio2.         |
| 7           | La secuencia se asigna a los altavoces left, right, middle y audio2. |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**AudioAudioPresentationMode**](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



