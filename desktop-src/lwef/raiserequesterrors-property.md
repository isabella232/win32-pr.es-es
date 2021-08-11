---
title: Propiedad RaiseRequestErrors
description: Propiedad RaiseRequestErrors
ms.assetid: 60eb4478-526e-492a-8fb3-d1e54eff9868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081a47eef17378c24df5bdbcb0f5141b0dece45ec9933f289d0b3da9193793d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246618"
---
# <a name="raiserequesterrors-property"></a>Propiedad RaiseRequestErrors

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece si se producen errores para las solicitudes.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent!". RaiseRequestErrors* *  \[  =  *booleano*\]



| Parte      | Descripción                                                                                                                                                                                            |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Valor booleano que determina si se producen errores en las solicitudes.<br/> **True**    (valor predeterminado) Se producen errores de solicitud. <br/> **False**     No se producen errores de solicitud.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta propiedad permite determinar si el servidor genera errores que se producen con métodos que admiten [**objetos Request.**](/windows/desktop/lwef/the-request-object) Por ejemplo, si especifica un nombre de animación que no existe en un método [**Play,**](play-method.md)el servidor genera un error (que muestra el mensaje de error) a menos que establezca esta propiedad en **False.**

Puede ser útil para los lenguajes de programación que no proporcionan recuperación cuando se genera un error. Sin embargo, tenga cuidado al establecer esta propiedad en **False,** ya que puede ser más difícil encontrar errores en el código.

 

