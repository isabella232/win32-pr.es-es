---
title: Evento Player.DomainChange
description: El evento DomainChange tiene lugar cuando cambia el dominio de DVD. | Evento Player.DomainChange
ms.assetid: 01965492-276e-4d30-99eb-767e0776b423
keywords:
- DomainChange event Reproductor de Windows Media
- DomainChange event Reproductor de Windows Media , Player (Clase)
- Player class Reproductor de Windows Media , DomainChange event
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070994"
---
# <a name="playerdomainchange-event"></a>Evento Player.DomainChange

El **evento DomainChange** tiene lugar cuando cambia el dominio de DVD.

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
| primera reproducción         | Realizar la inicialización predeterminada de un disco de DVD.                     |
| videoManagerMenu  | Mostrar menús para todo el disco. También se conoce como menú raíz o topMenu. |
| videoTitleSetMenu | Mostrar menús para el conjunto de títulos actual. También se conoce como titleMenu.     |
| title             | Mostrar el título actual.                                        |
| stop              | El navegador de DVD está en el dominio DE DEtenerse de DVD.                         |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede acceder a un método o pasarlo a un método en un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la mayúscula.

**Reproductor de Windows Media 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior.<br/>                           |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dvd (objeto)**](dvd-object.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





