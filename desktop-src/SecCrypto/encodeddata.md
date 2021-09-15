---
description: Representa un bloque de datos codificados de ASN.1.
ms.assetid: af7acc5f-da0a-4235-8496-05db94664ea5
title: Objeto EncodedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d05fce31ad4ef08bf9f573c0158a683bdbeba739
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476452"
---
# <a name="encodeddata-object"></a>Objeto EncodedData

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase AsnEncodedData en**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) el espacio de nombres [**System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **objeto EncodedData** representa un bloque de datos codificados asn.1.

## <a name="when-to-use"></a>Cuándo se usa

Varias propiedades del objeto CAPICOM devuelven el objeto **EncodedData.** Cuando se devuelve, este objeto se usa para realizar las siguientes tareas:

-   Obtenga una representación de cadena de los datos codificados.
-   Obtenga el objeto descodificador, si existe, que está asociado a los datos codificados.
-   Determine el tipo de datos codificados.

## <a name="members"></a>Members

El **objeto EncodedData** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto EncodedData** tiene estos métodos.



| Método                                 | Descripción                                                     |
|:---------------------------------------|:----------------------------------------------------------------|
| [**Descodificador**](encodeddata-decoder.md) | Obtiene un objeto descodificador, si existe uno.<br/>             |
| [**Formato**](encodeddata-format.md)   | Devuelve una representación de cadena de los datos codificados.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto EncodedData** tiene estas propiedades.



| Propiedad.                                      | Tipo de acceso          | Descripción                                                          |
|:----------------------------------------------|:---------------------|:---------------------------------------------------------------------|
| [**Value**](encodeddata-value.md)<br/> | Solo lectura<br/> | Recupera los datos codificados. Esta es la propiedad predeterminada.<br/> |



 

## <a name="remarks"></a>Observaciones

El único tipo admitido de datos codificados [**es CertificatePolicies.**](certificatepolicies.md)

No se puede crear el objeto **EncodedData.**

Las siguientes propiedades de objeto CAPICOM devuelven **un objeto EncodedData:**

-   **PublicKey.EncodedKey**
-   **PublicKey.EncodedParameters**
-   **Extension.EncodedData**
-   **Policy.EncodedData**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
