---
title: Active (propiedad)
description: Active (propiedad)
ms.assetid: 76ada073-782a-4355-b4e8-42dd84d0139b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fe5fea7d94586c9f9d5c12b3a3b11ffbd7c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268769"
---
# <a name="active-property"></a>Active (propiedad)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve si la aplicación es el cliente activo del carácter y si el carácter es superior.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente. ***Caracteres * * * * ("*** CharacterID * * *").* *  \[  =  *Estado* activo\]



| Parte    | Descripción                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *state* | Expresión de tipo entero que especifica el estado de la aplicación cliente. 0 no es el cliente activo.<br/> 1 el cliente activo. <br/> 2 el cliente de entrada-activo. (El carácter superior).<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando varias aplicaciones cliente comparten el mismo carácter, el cliente activo del carácter recibe la entrada del mouse (por ejemplo, eventos [**click**](click-event.md) o [DragStart](dragstart-event.md) de control de Microsoft Agent). Del mismo modo, cuando se muestran varios caracteres, el cliente activo del carácter superior (también conocido como cliente de entrada-activo) recibe eventos de comando.

Puede usar el método [**Activate**](activate-method.md)para establecer si la aplicación es el cliente activo del carácter o para convertir la aplicación en el cliente activo de entrada (que también hace que el carácter sea más alto).

## <a name="see-also"></a>Consulte también

[Activar * * método * *](activate-method.md)


 

 





