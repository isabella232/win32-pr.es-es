---
title: Propiedad RaiseRequestErrors
description: Propiedad RaiseRequestErrors
ms.assetid: 60eb4478-526e-492a-8fb3-d1e54eff9868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9e559f999db663a8a9f5874f6d16a10e1e78ac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104271204"
---
# <a name="raiserequesterrors-property"></a>Propiedad RaiseRequestErrors

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece si se producen errores en las solicitudes.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente * * *. RaiseRequestErrors* *  \[  =  *booleano*\]



| Parte      | Descripción                                                                                                                                                                                            |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Valor booleano que determina si se producen errores en las solicitudes.<br/> Se generan errores de solicitud **true** (valor predeterminado). <br/> **False**     No se generan errores de solicitud.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta propiedad le permite determinar si el servidor genera errores que se producen con métodos que admiten objetos de [**solicitud**](/windows/desktop/lwef/the-request-object) . Por ejemplo, si especifica un nombre de animación que no existe en un método [**Play**](play-method.md), el servidor genera un error (mostrando el mensaje de error) a menos que establezca esta propiedad en **false**.

Puede ser útil para los lenguajes de programación que no proporcionan recuperación cuando se produce un error. Sin embargo, tenga cuidado al establecer esta propiedad en **false**, ya que podría ser más difícil encontrar errores en el código.

 

