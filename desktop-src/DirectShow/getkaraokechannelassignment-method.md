---
description: El método GetKaraokeChannelAssignment recupera un valor que indica cómo se asignan los canales de canal a los hablantes.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: GetKaraokeChannelAssignment (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafe1217e08f3dc4f55aeec42424b1ebf9d86d22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061124"
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
| 3           | La secuencia se asigna a los altavoces izquierdo, derecho e intermedio.         |
| 4           | La secuencia se asigna a los altavoces izquierdo, derecho y audio1.         |
| 5           | La secuencia se asigna a los altavoces left, right, middle y audio1. |
| 6           | La secuencia se asigna a los altavoces izquierdo, derecho y audio2.         |
| 7           | La secuencia se asigna a los altavoces left, right, middle y audio2. |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**AudioPresentationMode**](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



