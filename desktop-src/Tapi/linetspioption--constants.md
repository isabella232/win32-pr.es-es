---
description: Las \_ constantes LINETSPIOPTION describe los proveedores de servicios de pedidos a los que se debe llamar.
ms.assetid: af91f466-d87e-4767-a2c6-d882b9108f21
title: Constantes de LINETSPIOPTION_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e8fa13047dcbad60472fac371b255f7533809c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691046"
---
# <a name="linetspioption_-constants"></a>Constantes de LINETSPIOPTION \_

Las **\_ constantes LINETSPIOPTION** describe los proveedores de servicios de pedidos a los que se debe llamar.

<dl> <dt>

<span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**LINETSPIOPTION \_ NONREENTRANT**
</dt> <dd> <dl> <dt>



TAPI debe llamar a las funciones de este proveedor de servicios de una en una; debe esperar de cada función para que devuelva (pero no para que se completen las funciones asincrónicas) antes de llamar a la misma función u otra, ya sea en el mismo subproceso o en otro diferente, en el mismo procesador o en otro diferente.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



 

 




