---
title: Propiedad HasOtherClients
description: Propiedad HasOtherClients
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7bb91240ade815c00fb2e36adf1466dcb30ba4240be038342906be49e6ff2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479010"
---
# <a name="hasotherclients-property"></a>Propiedad HasOtherClients

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve si otras aplicaciones usan el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agente*. **Characters("**_CharacterID_*_"). HasOtherClients_*



| Valor     | Descripción                                |
|-----------|--------------------------------------------|
| **True**  | El carácter tiene otros clientes.           |
| **False** | El carácter no tiene otros clientes. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Puede usar esta propiedad para determinar si la aplicación es el único o último cliente del carácter, cuando más de una aplicación comparte (ha cargado) el mismo carácter.

 

 




