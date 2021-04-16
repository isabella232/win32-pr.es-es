---
title: Evento Player. AudioLanguageChange
description: El evento AudioLanguageChange se produce cuando cambia el idioma de audio actual. | Evento Player. AudioLanguageChange
ms.assetid: 29006a51-1b72-4fab-9906-8a0af3d92560
keywords:
- Media Player AudioLanguageChange de eventos de Windows
- Evento AudioLanguageChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento AudioLanguageChange
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708767"
---
# <a name="playeraudiolanguagechange-event"></a>Evento Player. AudioLanguageChange

El evento **AudioLanguageChange** se produce cuando cambia el idioma de audio actual.

## <a name="syntax"></a>Sintaxis


```JScript
Player.AudioLanguageChange(
  LangID
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ididioma* 
</dt> <dd>

**Número** (**largo**) que especifica el nuevo identificador de configuración regional (LCID).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Un LCID identifica de forma única un dialecto de lenguaje determinado, denominado configuración regional.

El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo de Microsoft JScript importado mediante el nombre de parámetro dado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.

**Windows Media Player 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls. currentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





