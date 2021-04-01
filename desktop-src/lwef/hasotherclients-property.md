---
title: Propiedad HasOtherClients
description: Propiedad HasOtherClients
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3434cec191d2bec93d501847df064a8dbbf3e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075752"
---
# <a name="hasotherclients-property"></a>Propiedad HasOtherClients

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve si otras aplicaciones están usando el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente*. **Caracteres ("***CharacterID***"). HasOtherClients**



| Value     | Descripción                                |
|-----------|--------------------------------------------|
| **True**  | El carácter tiene otros clientes.           |
| **False** | El carácter no tiene otros clientes. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede usar esta propiedad para determinar si la aplicación es el único o el último cliente del carácter, cuando más de una aplicación comparte (ha cargado) el mismo carácter.

 

 




