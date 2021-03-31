---
description: Función definida por la aplicación que crea una lista de identificadores de seguridad (SID) que se aplican a un cliente. AuthzComputeGroupsCallback es un marcador de posición para el nombre de la función definida por la aplicación.
ms.assetid: c20a02a0-5303-4433-a484-5a89999b32b9
title: Función de devolución de llamada AuthzComputeGroupsCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzComputeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 3728f8114d87d07ddb33dd77a6fda5db30d07cf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819462"
---
# <a name="authzcomputegroupscallback-callback-function"></a>Función de devolución de llamada AuthzComputeGroupsCallback

La función **AuthzComputeGroupsCallback** es una función definida por la aplicación que crea una lista de [*identificadores de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) que se aplican a un cliente. **AuthzComputeGroupsCallback** es un marcador de posición para el nombre de la función definida por la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CALLBACK AuthzComputeGroupsCallback(
  _In_  AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_  PVOID                       Args,
  _Out_ PSID_AND_ATTRIBUTES         *pSidAttrArray,
  _Out_ PDWORD                      pSidCount,
  _Out_ PSID_AND_ATTRIBUTES         *pRestrictedSidAttrArray,
  _Out_ PDWORD                      pRestrictedSidCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hAuthzClientContext* \[ de\]
</dt> <dd>

Identificador de un contexto de cliente.

</dd> <dt>

*Argumentos* \[ de\]
</dt> <dd>

Datos pasados en el parámetro *DynamicGroupArgs* de una llamada a la función [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext), [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)o [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) .

</dd> <dt>

*pSidAttrArray* \[ enuncia\]
</dt> <dd>

Puntero a una variable de puntero que recibe la dirección de una matriz de estructuras de [**SID \_ y \_ atributos**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) . Estas estructuras representan los grupos a los que pertenece el cliente.

</dd> <dt>

*pSidCount* \[ enuncia\]
</dt> <dd>

El número de estructuras en *pSidAttrArray*.

</dd> <dt>

*pRestrictedSidAttrArray* \[ enuncia\]
</dt> <dd>

Puntero a una variable de puntero que recibe la dirección de una matriz de estructuras de [**SID \_ y \_ atributos**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) . Estas estructuras representan los grupos de los que el cliente está restringido.

</dd> <dt>

*pRestrictedSidCount* \[ enuncia\]
</dt> <dd>

El número de estructuras en *pSidRestrictedAttrArray*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función devuelve correctamente una lista de SID, el valor devuelto es **true**.

Si se produce un error en la función, el valor devuelto es **false**.

## <a name="remarks"></a>Observaciones

Las aplicaciones también pueden agregar SID al contexto del cliente mediante una llamada a [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext).

Las variables de atributo deben tener el formato de una expresión cuando se utilizan con operadores lógicos; de lo contrario, se evalúan como Unknown.

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

[**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)
</dt> <dt>

[**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)
</dt> <dt>

[**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)
</dt> <dt>

[**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> <dt>

[**SID \_ y \_ atributos**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes)
</dt> </dl>

 

