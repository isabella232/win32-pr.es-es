---
description: Una función definida por la aplicación que controla las entradas de control de acceso (ACE) de devolución de llamada durante una comprobación de acceso.
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279642"
---
# <a name="authzaccesscheckcallback-callback-function"></a>Función de devolución de llamada AuthzAccessCheckCallback

La función **AuthzAccessCheckCallback** es una función definida por la aplicación que controla [*las entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) de devolución de llamada durante una comprobación de acceso. **AuthzAccessCheckCallback** es un marcador de posición para el nombre de la función definida por la aplicación. La aplicación registra esta devolución de llamada mediante una llamada a [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).

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

*hAuthzClientContext* \[ de\]
</dt> <dd>

Identificador de un contexto de cliente.

</dd> <dt>

*pAce* \[ de\]
</dt> <dd>

Puntero a la ACE que se va a evaluar para su inclusión en la llamada a la función [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .

</dd> <dt>

*pArgs* \[ en, opcional\]
</dt> <dd>

Datos pasados en el parámetro *DynamicGroupArgs* de la llamada a [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) o [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck).

</dd> <dt>

*pbAceApplicable* \[ in, out\]
</dt> <dd>

Puntero a una variable booleana que recibe los resultados de la evaluación de la lógica definida por la aplicación.

Los resultados son **verdaderos** si la lógica determina que la ACE es aplicable y se incluirá en la llamada a [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck); de lo contrario, los resultados son **false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve **true**.

Si la función no puede realizar la evaluación, devuelve **false**. Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para devolver un error a la función de comprobación de acceso.

## <a name="remarks"></a>Observaciones

Las variables de atributo de seguridad deben estar presentes en el contexto del cliente si se hace referencia a en una expresión condicional; de lo contrario, el término de la expresión condicional que hace referencia a ellos se evaluará como desconocido.

Para obtener más información, consulte la información general [sobre el funcionamiento de AccessCheck](how-dacls-control-access-to-an-object.md) y la Directiva de [autorización centralizada](centralized-authorization-policy.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                   |
| Redistribuible<br/>          | Paquete de herramientas de administración de Windows Server 2003 en Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones básicas de Access Control](authorization-functions.md)
</dt> <dt>

[Directiva de autorización centralizada](centralized-authorization-policy.md)
</dt> <dt>

[Cómo funciona AccessCheck](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> <dt>

[**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

