---
description: Las constantes LINEPROXYSTATUS \_ indican el estado del proxy en una línea que la aplicación tiene abierta actualmente.
ms.assetid: a5cf3512-ee42-4f64-8fe3-73a14589f78c
title: LINEPROXYSTATUS_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b49c3e787451024254a25959cdf2e0a8240cba4453c8b888665d14a2aa220e93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003033"
---
# <a name="lineproxystatus_-constants"></a>LinePROXYSTATUS \_ (constantes)

Las **constantes LINEPROXYSTATUS \_ indican** el estado del proxy en una línea que la aplicación tiene abierta actualmente.

Consulte [**LINEPROXYREQUEST \_ Constants (Constantes LINEPROXYREQUEST)**](lineproxyrequest--constants.md) para obtener una lista y una descripción de todos los valores de solicitud de proxy posibles.

<dl> <dt>

<span id="LINEPROXYSTATUS_ALLOPENFORACD"></span><span id="lineproxystatus_allopenforacd"></span>**LINEPROXYSTATUS \_ ALLOPENFORACD**
</dt> <dd> <dl> <dt>



La línea ahora tiene servidores proxy abiertos para todos los tipos de solicitud de proxy necesarios para las operaciones de ACD mediante TAPI versión 3.0 y posteriores.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYSTATUS_CLOSE"></span><span id="lineproxystatus_close"></span>**LINEPROXYSTATUS \_ CLOSE**
</dt> <dd> <dl> <dt>



Se ha cerrado un proxy.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYSTATUS_OPEN"></span><span id="lineproxystatus_open"></span>**LINEPROXYSTATUS \_ OPEN**
</dt> <dd> <dl> <dt>



Se ha abierto un nuevo proxy.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




