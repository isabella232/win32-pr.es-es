---
title: Evento BalloonShow
description: Evento BalloonShow
ms.assetid: 8a73e883-c003-480b-8a0a-e699caffe54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10aa8ab2c556fdf603a3972033a7440041fef6a45f828115c649a8a42810eb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726151"
---
# <a name="balloonshow-event"></a>Evento BalloonShow

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando se muestra el globo de palabras de un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent* \_ **BalloonShow** **(ByVal** *CharacterID...))**



| Parte          | Descripción                                                       |
|---------------|-------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter asociado al globo de palabras. |



 

</dd> </dl>

### <a name="remarks"></a>Comentarios

El servidor envía este evento solo a los clientes del carácter (aplicaciones que han cargado el carácter) que usa la palabra globo.

### <a name="see-also"></a>Consulte también

[**Evento BalloonHide**](balloonhide-event.md)


 

 




