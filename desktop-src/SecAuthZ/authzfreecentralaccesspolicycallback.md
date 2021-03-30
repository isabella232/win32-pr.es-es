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
ms.openlocfilehash: d2139c9fa106b6070a3c043d417bdbf23379084b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279640"
---
# <a name="authzfreecentralaccesspolicycallback-callback-function"></a>Función de devolución de llamada AuthzFreeCentralAccessPolicyCallback

La función *AuthzFreeCentralAccessPolicyCallback* es una función definida por la aplicación que libera la memoria asignada por la función [*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md) . *AuthzFreeCentralAccessPolicyCallback* es un marcador de posición para el nombre de la función definida por la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CALLBACK AuthzFreeCentralAccessPolicyCallback(
  _In_ PVOID pCentralAccessPolicy
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCentralAccessPolicy* \[ de\]
</dt> <dd>

Puntero a la Directiva de acceso central que se va a liberar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve **true**.

Si la función no puede realizar la evaluación, devuelve **false**. Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para devolver un error a la función de comprobación de acceso.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**AUTHZ \_ init \_ info**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md)
</dt> </dl>

 

 
