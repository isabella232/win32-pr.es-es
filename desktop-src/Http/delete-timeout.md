---
title: delete timeout
description: Elimina un tiempo de espera global y hace que el servicio HTTP.sys vuelva a los valores predeterminados.
ms.assetid: 5fcd5df4-023e-486d-b41a-639e210a128f
keywords:
- tiempo de espera de eliminación HTTP
topic_type:
- apiref
api_name:
- delete timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6ee436e1eb7f545a74aa56f6c146afbd1c57066
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "105665765"
---
# <a name="delete-timeout"></a>delete timeout

Elimina un tiempo de espera global y hace que el servicio HTTP.sys vuelva a los valores predeterminados.

``` syntax
delete timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype = \] {idleconnectiontimeout, \| HeaderWaitTimeout}**
</dt> <dd>

Especifica el tipo de opción de tiempo de espera.

</dd> </dl>

## <a name="examples"></a>Ejemplos

**delete timeout timeouttype=idleconnectiontimeout**

**delete timeout timeouttype=headerwaittimeout**

 

 




