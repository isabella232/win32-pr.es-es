---
title: Evento de tamaño
description: Evento de tamaño
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a896d2dcbf8b925c0ca13fa429f6dfd95bc21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903393"
---
# <a name="size-event"></a>Evento de tamaño

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando cambia el tamaño de un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

Tamaño de **Sub** *Agent* \_ **(ByVal** *CharacterID*, **ByVal** *width*, **ByVal** *height*)



| Parte          | Descripción                                                         |
|---------------|---------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter que se ha despasado.                         |
| *Width*       | Devuelve el nuevo ancho (en píxeles) del marco de caracteres como un entero.  |
| *Height*      | Devuelve el nuevo alto (en píxeles) del marco de caracteres como un entero. |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Este evento se produce cuando una aplicación cambia el tamaño de un carácter. Este evento solo se envía a los clientes del carácter (aplicaciones que han cargado el carácter).

### <a name="see-also"></a>Consulte también

[**Evento de movimiento**](move-event.md)


 

 




