---
description: Representa una colección de objetos EKU.
ms.assetid: 04b9f0bf-e1d4-4a2c-be5d-bae7c1090bdb
title: Objeto EKUs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 56fd6eaeb5a00549cbb4ee659b99ece391e0ebed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476462"
---
# <a name="ekus-object"></a>Objeto EKUs

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **objeto EKUs** representa una colección de [**objetos EKU.**](eku.md) Cada [**objeto EKU**](eku.md) representa una única propiedad de uso de clave extendida (EKU) de un certificado.

## <a name="when-to-use"></a>Cuándo se usa

La **colección EKUs** se usa para realizar las siguientes tareas:

-   Recupere el número de propiedades EKU de la colección.
-   Recuperar un objeto [**EKU específico**](eku.md) de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Members

El **objeto EKUs** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto EKUs** tiene estas propiedades.



| Propiedad.                                     | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ekus-newenum.md)<br/> | Solo lectura<br/> | Recupera una [**interfaz IEnumVARIANT en**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un objeto que se puede usar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Count**](ekus-count.md)<br/>       | Solo lectura<br/> | Recupera el número de objetos [**EKU**](eku.md) de la colección.<br/>                                                                                                                                                |
| [**Artículo**](ekus-item.md)<br/>         | Solo lectura<br/> | Recupera el objeto [**EKU**](eku.md) que representa la propiedad EKU indizada. Esta es la propiedad predeterminada.<br/>                                                                                                      |



 

## <a name="remarks"></a>Observaciones

La propiedad [**ExtendedKeyUsage.EKUs**](extendedkeyusage-ekus.md) recupera esta colección.

No se puede crear el objeto **EKUs.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
