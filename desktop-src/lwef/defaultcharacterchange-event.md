---
title: Evento DefaultCharacterChange
description: Evento DefaultCharacterChange
ms.assetid: 14b86a44-8fd2-4719-b7b5-cdcc618d27cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed166608d3f3b874e975ff58f600d24b73b50e293333b841039b2240780b4de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963135"
---
# <a name="defaultcharacterchange-event"></a>Evento DefaultCharacterChange

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando el usuario cambia el carácter predeterminado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent.:DefaultCharacterChange* *  **(Guid de ByVal))** *



| Parte   | Descripción                                      |
|--------|--------------------------------------------------|
| *GUID* | Devuelve el identificador único del carácter. |



 

</dd> </dl>

### <a name="remarks"></a>Comentarios

Este evento indica cuándo el usuario ha cambiado el carácter asignado como carácter predeterminado del usuario. El servidor envía esto solo a los clientes que han cargado el carácter predeterminado.

Cuando aparece el nuevo carácter, asume el mismo tamaño que cualquier instancia ya cargada del carácter o el carácter predeterminado anterior (en ese orden).

### <a name="see-also"></a>Consulte también

[**Método ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md), [ **Método Load**](load-method.md)


 

 




