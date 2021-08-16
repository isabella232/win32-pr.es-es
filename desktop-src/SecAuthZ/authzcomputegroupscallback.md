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
ms.openlocfilehash: 7c30194e4131cbd375192723e23308e1ad5ead69d849ab73857f72ef1d4b0790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784083"
---
# <a name="authzcomputegroupscallback-callback-function"></a>Función de devolución de llamada AuthzComputeGroupsCallback

La **función AuthzComputeGroupsCallback** es una función definida por la aplicación que crea una lista de identificadores de seguridad (SID) que se aplican a un cliente. [](/windows/desktop/SecGloss/s-gly) **AuthzComputeGroupsCallback es** un marcador de posición para el nombre de la función definida por la aplicación.

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

*hAuthzClientContext* \[ En\]
</dt> <dd>

Identificador de un contexto de cliente.

</dd> <dt>

*Args* \[ En\]
</dt> <dd>

Datos pasados en el parámetro *DynamicGroupArgs* de una llamada a la función [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext), [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)o [**AuthzInitializeContextFromToken.**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)

</dd> <dt>

*pSidAttrArray* \[ out\]
</dt> <dd>

Puntero a una variable de puntero que recibe la dirección de una matriz de [**estructuras SID \_ Y \_ ATTRIBUTES.**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) Estas estructuras representan los grupos a los que pertenece el cliente.

</dd> <dt>

*pSidCount* \[ out\]
</dt> <dd>

Número de estructuras de *pSidAttrArray.*

</dd> <dt>

*pRestrictedSidAttrArray* \[ out\]
</dt> <dd>

Puntero a una variable de puntero que recibe la dirección de una matriz de [**estructuras SID \_ Y \_ ATTRIBUTES.**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) Estas estructuras representan los grupos desde los que el cliente está restringido.

</dd> <dt>

*pRestrictedSidCount* \[ out\]
</dt> <dd>

Número de estructuras de *pSidRestrictedAttrArray.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función devuelve correctamente una lista de SID, el valor devuelto es **TRUE.**

Si se produce un error en la función, el valor devuelto es **FALSE.**

## <a name="remarks"></a>Comentarios

Las aplicaciones también pueden agregar SID al contexto de cliente llamando a [**AuthzAddSidsToContext.**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)

Las variables de atributo deben tener el formato de una expresión cuando se usan con operadores lógicos; De lo contrario, se evalúan como desconocidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                   |
| Redistribuible<br/>          | Windows Paquete de herramientas de administración de Server 2003 en Windows XP<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones Access Control básicas](authorization-functions.md)
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

[**SID \_ Y \_ ATRIBUTOS**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes)
</dt> </dl>

 

