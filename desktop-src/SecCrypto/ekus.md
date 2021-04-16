---
description: Representa una colección de objetos EKU.
ms.assetid: 04b9f0bf-e1d4-4a2c-be5d-bae7c1090bdb
title: EKU (objeto)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671431"
---
# <a name="ekus-object"></a>EKU (objeto)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El objeto **EKU** representa una colección de objetos [**EKU**](eku.md) . Cada objeto [**EKU**](eku.md) representa una única propiedad de uso de clave extendida (EKU) de un certificado.

## <a name="when-to-use"></a>Cuándo se usa

La colección **EKU** se usa para realizar las siguientes tareas:

-   Recupere el número de propiedades EKU de la colección.
-   Recupera un objeto [**EKU**](eku.md) específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Miembros

El objeto **EKU** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **EKU** tiene estas propiedades.



| Propiedad                                     | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ekus-newenum.md)<br/> | Solo lectura<br/> | Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contabiliza**](ekus-count.md)<br/>       | Solo lectura<br/> | Recupera el número de objetos [**EKU**](eku.md) de la colección.<br/>                                                                                                                                                |
| [**Elemento**](ekus-item.md)<br/>         | Solo lectura<br/> | Recupera el objeto [**EKU**](eku.md) que representa la propiedad de EKU indizado. Esta es la propiedad predeterminada.<br/>                                                                                                      |



 

## <a name="remarks"></a>Observaciones

La propiedad [**ExtendedKeyUsage. EKU**](extendedkeyusage-ekus.md) recupera esta colección.

No se puede crear el objeto **EKU** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
