---
description: Función definida por la aplicación que controla las entradas de control de acceso (ACE) de devolución de llamada durante una comprobación de acceso.
ms.assetid: e8a510e6-0739-4765-ad07-3bcb1b9c905c
title: Función de devolución de llamada AuthzAccessCheckCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzAccessCheckCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 82e100092dd7c59e9cc689aa8723365fae8bed29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250436"
---
# <a name="authzaccesscheckcallback-callback-function"></a>Función de devolución de llamada AuthzAccessCheckCallback

La **función AuthzAccessCheckCallback** es una función definida por la aplicación que controla las entradas de [*control*](/windows/desktop/SecGloss/a-gly) de acceso (ACE) de devolución de llamada durante una comprobación de acceso. **AuthzAccessCheckCallback es** un marcador de posición para el nombre de la función definida por la aplicación. La aplicación registra esta devolución de llamada mediante una [**llamada a AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).

## <a name="syntax"></a>Sintaxis


```C++
BOOL CALLBACK AuthzAccessCheckCallback(
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PACE_HEADER                 pAce,
  _In_opt_ PVOID                       pArgs,
  _Inout_  PBOOL                       pbAceApplicable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hAuthzClientContext* \[ En\]
</dt> <dd>

Identificador de un contexto de cliente.

</dd> <dt>

*pAce* \[ En\]
</dt> <dd>

Puntero a la ACE para evaluar la inclusión en la llamada a la [**función AuthzAccessCheck.**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)

</dd> <dt>

*pArgs* \[ en, opcional\]
</dt> <dd>

Datos pasados en *el parámetro DynamicGroupArgs* de la llamada a [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) o [**AuthzCachedAccessCheck.**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)

</dd> <dt>

*pbAceApplicable* \[ in, out\]
</dt> <dd>

Puntero a una variable booleana que recibe los resultados de la evaluación de la lógica definida por la aplicación.

Los resultados **son TRUE** si la lógica determina que la ACE es aplicable y se incluirá en la llamada a [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck); De lo contrario, los resultados son **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve **TRUE.**

Si la función no puede realizar la evaluación, devuelve **FALSE**. Use [**SetLastError para**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) devolver un error a la función de comprobación de acceso.

## <a name="remarks"></a>Observaciones

Las variables de atributo de seguridad deben estar presentes en el contexto del cliente si se hace referencia a en una expresión condicional; de lo contrario, el término de expresión condicional que hace referencia a ellas se evaluará como desconocido.

Para obtener más información, vea [Las introduccións a AccessCheck y](how-dacls-control-access-to-an-object.md) a la directiva [de autorización](centralized-authorization-policy.md) centralizada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                   |
| Redistribuible<br/>          | Windows Paquete de herramientas de administración de Server 2003 en Windows XP<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones Access Control básicas](authorization-functions.md)
</dt> <dt>

[Directiva de autorización centralizada](centralized-authorization-policy.md)
</dt> <dt>

[Funcionamiento de AccessCheck](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> <dt>

[**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

