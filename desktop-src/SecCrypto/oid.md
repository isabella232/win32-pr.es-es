---
description: Representa un identificador de objeto (OID) utilizado por varias propiedades CAPICOM.
ms.assetid: d9dc2a9a-920b-41e1-91fb-da1628df577d
title: Objeto OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a524bfd8d2eb2edcf3c97919129dd694414d5ace
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173149"
---
# <a name="oid-object"></a>Objeto OID

\[El **objeto OID** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase Oid en**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) el espacio de nombres [**System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **objeto OID** representa un [*identificador de*](../secgloss/o-gly.md) objeto (OID) que usan varias propiedades CAPICOM.

## <a name="when-to-use"></a>Cuándo se usa

El **objeto OID** se usa para realizar las siguientes tareas:

-   Establezca o recupere un nombre CAPICOM y un nombre para mostrar para el OID.
-   Establezca o recupere el número de puntos para el OID.

## <a name="members"></a>Members

El **objeto OID** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto OID** tiene estas propiedades.



| Propiedad                                            | Tipo de acceso           | Descripción                                                                                      |
|:----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**FriendlyName**](oid-friendlyname.md)<br/> | Lectura y escritura<br/> | Establece o recupera el nombre para mostrar del OID.<br/>                                       |
| [**Nombre**](oid-name.md)<br/>                 | Lectura y escritura<br/> | Establece o recupera el nombre definido por CAPICOM para el OID. Esta es la propiedad predeterminada.<br/> |
| [**Value**](oid-value.md)<br/>               | Lectura y escritura<br/> | Establece o recupera el valor del número de puntos de OID del OID.<br/>                      |



 

## <a name="remarks"></a>Observaciones

Se puede crear el objeto **OID** y es seguro para el scripting. El ProgID del **objeto OID** es CAPICOM. OID.1.

Las siguientes propiedades de objeto CAPICOM devuelven un **objeto OID:**

-   [**PolicyInformation.OID**](policyinformation-oid.md)
-   [**Qualifier.OID**](qualifier-oid.md)
-   [**Extension.OID**](extension-oid.md)
-   [**Template.OID**](template-oid.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
