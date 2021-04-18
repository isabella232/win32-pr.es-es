---
title: Evento Player. DomainChange
description: El evento DomainChange se produce cuando cambia el dominio del DVD. | Evento Player. DomainChange
ms.assetid: 01965492-276e-4d30-99eb-767e0776b423
keywords:
- Media Player DomainChange de eventos de Windows
- Evento DomainChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento DomainChange
topic_type:
- apiref
api_name:
- Player.DomainChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9637913451aa5bba937906130899c46e0bd34d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708966"
---
# <a name="playerdomainchange-event"></a>Evento Player. DomainChange

El evento **DomainChange** se produce cuando cambia el dominio del DVD.

## <a name="syntax"></a>Sintaxis


```JScript
Player.DomainChange(
  strDomain
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strDomain* 
</dt> <dd>

**Cadena** que indica el nuevo dominio. Contiene uno de los valores siguientes.



| String            | Descripción                                                          |
|-------------------|----------------------------------------------------------------------|
| firstplay         | Realizar la inicialización predeterminada de un disco DVD.                     |
| videoManagerMenu  | Mostrando menús para todo el disco. También se conoce como menú o menú raíz. |
| videoTitleSetMenu | Mostrar menús para el conjunto de títulos actual. También se conoce como titleMenu.     |
| title             | Mostrar el título actual.                                        |
| stop              | El navegador de DVD está en el dominio de detención de DVD.                         |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.

**Windows Media Player 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player para Windows XP o posterior.<br/>                           |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de DVD**](dvd-object.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





