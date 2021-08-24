---
title: Método ClosedCaption.getSAMILangName
description: El método getSAMILangName recupera el nombre de un idioma admitido por el archivo SAMI actual.
ms.assetid: 20cf8faf-3a8c-4d7b-9bd1-2366672f0e67
keywords:
- Método getSAMILangName Reproductor de Windows Media
- Método getSAMILangName Reproductor de Windows Media , clase ClosedCaption
- Clase ClosedCaption Reproductor de Windows Media método , getSAMILangName
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d4150289eb7637d1772443a5437c6d245993ea0825a37d11bd7ec5accae918
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764035"
---
# <a name="closedcaptiongetsamilangname-method"></a>Método ClosedCaption.getSAMILangName

El **método getSAMILangName** recupera el nombre de un idioma admitido por el archivo SAMI actual.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = ClosedCaption.getSAMILangName(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

**Number** (**long**) que especifica el índice del nombre de idioma que se recuperará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena** que contiene el nombre del idioma tal y como se especifica en el archivo SAMI.

## <a name="remarks"></a>Comentarios

Los idiomas de un archivo SAMI se indexa en el orden que se muestra en el archivo, empezando por cero.

Este método no se puede usar hasta que se abra un archivo multimedia digital *(Reproductor de*.**openState** es igual a 13).

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption (objeto)**](closedcaption-object.md)
</dt> <dt>

[**ClosedCaption.SAMILang**](closedcaption-samilang.md)
</dt> </dl>

 

 





