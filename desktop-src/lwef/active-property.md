---
title: Propiedad activa
description: Propiedad activa
ms.assetid: 76ada073-782a-4355-b4e8-42dd84d0139b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac75a83724c793f2a7aba01718d57e47b25a0dd6b467ca7797ad6f0e4ced018e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753174"
---
# <a name="active-property"></a>Propiedad activa

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve si la aplicación es el cliente activo del carácter y si el carácter es superior.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.***Characters*"("**_CharacterID_*_"). Estado_ *  \[  =  *activo*\]



| Parte    | Descripción                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *state* | Expresión de entero que especifica el estado de la aplicación cliente. 0 No es el cliente activo.<br/> 1 Cliente activo. <br/> 2 El cliente activo de entrada. (El carácter superior).<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando varias aplicaciones cliente comparten el mismo carácter, el cliente activo del carácter recibe la entrada del mouse (por ejemplo, eventos [**Click**](click-event.md) o [DragStart](dragstart-event.md) del control Microsoft Agent). De forma similar, cuando se muestran varios caracteres, el cliente activo del carácter superior (también conocido como cliente activo de entrada) recibe eventos Command.

Puede usar el [**método Activate**](activate-method.md)para establecer si la aplicación es el cliente activo del carácter o para convertir la aplicación en el cliente activo de entrada (lo que también hace que el carácter sea el más alto).

## <a name="see-also"></a>Consulte también

[Activate** (método) **](activate-method.md)


 

 





