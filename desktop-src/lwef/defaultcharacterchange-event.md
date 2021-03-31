---
title: Evento DefaultCharacterChange
description: Evento DefaultCharacterChange
ms.assetid: 14b86a44-8fd2-4719-b7b5-cdcc618d27cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab92fe04f9c42466d559e9b4610eafc8490556d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418896"
---
# <a name="defaultcharacterchange-event"></a>Evento DefaultCharacterChange

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando el usuario cambia el carácter predeterminado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**Sub** *Agent. * * * DefaultCharacterChange* *  **(ByVal** *GUID * * *)**



| Parte   | Descripción                                      |
|--------|--------------------------------------------------|
| *GUID* | Devuelve el identificador único del carácter. |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Este evento indica que el usuario ha cambiado el carácter asignado como el carácter predeterminado del usuario. El servidor solo lo envía a los clientes que han cargado el carácter predeterminado.

Cuando aparece el nuevo carácter, se da por supuesto que tiene el mismo tamaño que cualquier instancia ya cargada del carácter o el carácter predeterminado anterior (en ese orden).

### <a name="see-also"></a>Consulte también

[**Método ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md), [ **Load (método** )](load-method.md)


 

 




