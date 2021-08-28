---
title: IdleOn( Propiedad)
description: IdleOn( Propiedad)
ms.assetid: ba436dec-c7b4-42e8-99d6-c6ff93afd73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e08ada4d48197e3090b5fc821b0c5b9f532f47074985218019bb14be8881e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749512"
---
# <a name="idleon-property"></a>IdleOn( Propiedad)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece un valor booleano que determina si el servidor administra las animaciones de estado de **idling** del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Valor_ *  \[  =  *booleano* IdleOn\]

</dd> </dl> 

| Parte      | Descripción                                                                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expresión booleana que especifica si el servidor administra el modo inactivo. **True** (valor predeterminado) El control del servidor del estado de inactividad está habilitado. <br/> **False** El control del servidor del estado de inactividad está deshabilitado. <br/> |



 

## <a name="remarks"></a>Comentarios

El servidor establece automáticamente un tiempo de espera después de la última animación que se reproduce para un carácter. Cuando se completa el intervalo de este temporizador, el servidor comienza el estado **de idling** de un carácter, reproduciendo sus animaciones de **Idling** asociadas a intervalos regulares. Si desea deshabilitar que el servidor reprodígue automáticamente las animaciones de estado **idling,** establezca la propiedad en **False** y reprodíguela o llame al [**método Stop.**](stop-method.md) Establecer este valor no afecta al estado de animación actual del carácter.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

 

 





