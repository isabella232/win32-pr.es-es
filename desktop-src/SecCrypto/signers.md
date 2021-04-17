---
description: Representa una colección de objetos de firmante.
ms.assetid: 72e86acd-eb87-4eff-bd4e-327630ebbfc4
title: Objeto signers
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
ms.openlocfilehash: 75eba0ecb2592bf7efc27ecdd63288179e306651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670525"
---
# <a name="signers-object"></a>Objeto signers

\[El objeto **signers** está disponible para su uso en los sistemas operativos especificados en la sección requirements. En su lugar, use una colección de objetos CmsSigner. Para obtener más información, vea la [**clase CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

El objeto de **firma** representa una colección de objetos de [**firmante**](signer.md) .

## <a name="when-to-use"></a>Cuándo se usa

El objeto **signers** se usa para realizar las siguientes tareas:

-   Recupere el número de certificados de la colección.
-   Recupera un objeto de **firma** específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Miembros

El objeto **signers** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **signers** tiene estas propiedades.



| Propiedad                                        | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](signers-newenum.md)<br/> | Solo lectura<br/> | Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contabiliza**](signers-count.md)<br/>       | Solo lectura<br/> | Número de objetos de [**firmante**](signer.md) en la colección.<br/>                                                                                                                                                        |
| [**Elemento**](signers-item.md)<br/>         | Solo lectura<br/> | Recupera el objeto de [**firmante**](signer.md) que representa el firmante indizado. Esta es la propiedad predeterminada.<br/>                                                                                                      |



 

## <a name="remarks"></a>Observaciones

No se puede crear el objeto **signers** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
