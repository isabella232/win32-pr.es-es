---
title: Método ClosedCaption.getSAMILangID
description: El método getSAMILangID recupera el identificador de configuración regional (LCID) de un idioma admitido por el archivo SAMI actual.
ms.assetid: 35f8379a-a2f5-4b22-b1ad-3c5cc5bc5e3d
keywords:
- Método getSAMILangID Reproductor de Windows Media
- Método getSAMILangID Reproductor de Windows Media , clase ClosedCaption
- Clase ClosedCaption Reproductor de Windows Media , método getSAMILangID
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd543c9cb9d884022d78a875a2f8de078c479b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126885268"
---
# <a name="closedcaptiongetsamilangid-method"></a>Método ClosedCaption.getSAMILangID

El **método getSAMILangID** recupera el identificador de configuración regional (LCID) de un idioma admitido por el archivo SAMI actual.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = ClosedCaption.getSAMILangID(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

**Number** (**long**) que especifica el índice del LCID que se recuperará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor Number** (**long**) que contiene el LCID del lenguaje con el índice especificado.

## <a name="remarks"></a>Observaciones

Los idiomas de un archivo SAMI se indexa en el orden que se muestra en el archivo, empezando por cero.

Este método no se puede usar hasta que se abra un archivo multimedia digital *(Reproductor de*.**openState** es igual a 13).

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption (objeto)**](closedcaption-object.md)
</dt> </dl>

 

 





