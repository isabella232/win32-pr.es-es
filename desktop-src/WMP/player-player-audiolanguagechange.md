---
title: Evento Player.AudioLanguageChange
description: El evento AudioLanguageChange tiene lugar cuando cambia el idioma de audio actual. | Evento Player.AudioLanguageChange
ms.assetid: 29006a51-1b72-4fab-9906-8a0af3d92560
keywords:
- Eventos AudioLanguageChange Reproductor de Windows Media
- Evento AudioLanguageChange Reproductor de Windows Media , clase Player
- Player class Reproductor de Windows Media , AudioLanguageChange event
topic_type:
- apiref
api_name:
- Player.AudioLanguageChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84809a966280c379f7051e500b4e385d640f890
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466011"
---
# <a name="playeraudiolanguagechange-event"></a>Evento Player.AudioLanguageChange

El **evento AudioLanguageChange** tiene lugar cuando cambia el idioma de audio actual.

## <a name="syntax"></a>Sintaxis


```JScript
Player.AudioLanguageChange(
  LangID
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LangID* 
</dt> <dd>

**Number** (**long**) que especifica el nuevo identificador de configuración regional (LCID).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Un LCID identifica de forma única un dialecto de idioma determinado, denominado configuración regional.

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede acceder a un método o pasarlo a un método en un archivo de Microsoft JScript importado mediante el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la mayúscula.

**Reproductor de Windows Media 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls.currentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





