---
description: La función AuthzFreeCentralAccessPolicyCallback es una función definida por la aplicación que libera la memoria asignada por la función AuthzGetCentralAccessPolicyCallback.
ms.assetid: F0859A67-4D20-4189-8F35-A78034E41E6A
title: Función de devolución de llamada AuthzFreeCentralAccessPolicyCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: f51903708bd3993e2837d65107798b1ff546c5857eff3bbed028ed4d6dda47f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783759"
---
# <a name="authzfreecentralaccesspolicycallback-callback-function"></a>Función de devolución de llamada AuthzFreeCentralAccessPolicyCallback

La *función AuthzFreeCentralAccessPolicyCallback* es una función definida por la aplicación que libera la memoria asignada por la función [*AuthzGetCentralAccessPolicyCallback.*](authzgetcentralaccesspolicycallback-.md) *AuthzFreeCentralAccessPolicyCallback es* un marcador de posición para el nombre de la función definida por la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CALLBACK AuthzFreeCentralAccessPolicyCallback(
  _In_ PVOID pCentralAccessPolicy
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCentralAccessPolicy* \[ En\]
</dt> <dd>

Puntero a la directiva de acceso central que se va a liberar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve **TRUE**.

Si la función no puede realizar la evaluación, devuelve **FALSE.** Use [**SetLastError para**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) devolver un error a la función de comprobación de acceso.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INFORMACIÓN DE \_ AUTHZ INIT \_**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md)
</dt> </dl>

 

 
