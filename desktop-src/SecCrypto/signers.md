---
description: Representa una colección de objetos Signer.
ms.assetid: 72e86acd-eb87-4eff-bd4e-327630ebbfc4
title: Objeto Signers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 62c5f59fc90d0d34226b4442b8fa443ad734d474e8077bf210df8bfdf752b1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898338"
---
# <a name="signers-object"></a>Objeto Signers

\[El **objeto Signers** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use una colección de objetos CmsSigner. Para obtener más información, vea [**cmsSigner (clase)**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **objeto Signers** representa una colección de [**objetos Signer.**](signer.md)

## <a name="when-to-use"></a>Cuándo se usa

El **objeto Signers** se usa para realizar las siguientes tareas:

-   Recupere el número de certificados de la colección.
-   Recupera un objeto **Signers** específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Miembros

El **objeto Signers** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto Signers** tiene estas propiedades.



| Propiedad                                        | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](signers-newenum.md)<br/> | Solo lectura<br/> | Recupera una [**interfaz IEnumVARIANT en**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un objeto que se puede usar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contar**](signers-count.md)<br/>       | Solo lectura<br/> | Número de [**objetos Signer**](signer.md) de la colección.<br/>                                                                                                                                                        |
| [**Elemento**](signers-item.md)<br/>         | Solo lectura<br/> | Recupera el objeto [**Signer**](signer.md) que representa el firmante indizado. Esta es la propiedad predeterminada.<br/>                                                                                                      |



 

## <a name="remarks"></a>Comentarios

No se puede crear el objeto **Signers.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
