---
description: Representa un identificador de objeto (OID) que se usa en varias propiedades de CAPICOM.
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671786"
---
# <a name="oid-object"></a>Objeto OID

\[El objeto **OID** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase OID**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

El objeto **OID** representa un [*identificador de objeto*](../secgloss/o-gly.md) (OID) que se usa en varias propiedades de CAPICOM.

## <a name="when-to-use"></a>Cuándo se usa

El objeto **OID** se usa para realizar las siguientes tareas:

-   Establezca o recupere un nombre de CAPICOM y un nombre para mostrar para el OID.
-   Establece o recupera el número de puntos del OID.

## <a name="members"></a>Miembros

El objeto **OID** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **OID** tiene estas propiedades.



| Propiedad                                            | Tipo de acceso           | Descripción                                                                                      |
|:----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**FriendlyName**](oid-friendlyname.md)<br/> | Lectura/escritura<br/> | Establece o recupera el nombre para mostrar del OID.<br/>                                       |
| [**Name**](oid-name.md)<br/>                 | Lectura/escritura<br/> | Establece o recupera el nombre definido por CAPICOM para el OID. Esta es la propiedad predeterminada.<br/> |
| [**Value**](oid-value.md)<br/>               | Lectura/escritura<br/> | Establece o recupera el valor del número de puntos OID del OID.<br/>                      |



 

## <a name="remarks"></a>Observaciones

Se puede crear el objeto **OID** y es seguro para el scripting. El ProgID del objeto **OID** es CAPICOM. OID. 1.

Las siguientes propiedades de objeto de CAPICOM devuelven un objeto **OID** :

-   [**PolicyInformation. OID**](policyinformation-oid.md)
-   [**Calificador. OID**](qualifier-oid.md)
-   [**Extensión. OID**](extension-oid.md)
-   [**Plantilla. OID**](template-oid.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
