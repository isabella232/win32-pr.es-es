---
description: Representa una única propiedad de uso de clave extendida (EKU) de un certificado.
ms.assetid: 08eb7c77-0224-4ab5-99e7-edf18eb23c60
title: Objeto EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bd887204abc31583e596e94c25b64addcfe8109e6432845d25d939fd8e79e2d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875145"
---
# <a name="eku-object"></a>Objeto EKU

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la clase [**X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **objeto EKU** representa una única propiedad de uso de clave extendida (EKU) de un certificado.

## <a name="members"></a>Miembros

El **objeto EKU** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto EKU** tiene estas propiedades.



| Propiedad                            | Tipo de acceso           | Descripción                                                                                                                                                                                                   |
|:------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nombre**](eku-name.md)<br/> | Lectura/escritura<br/> | Establece o recupera un valor de enumeración que especifica el nombre CAPICOM del EKU. Esta es la propiedad predeterminada.<br/>                                                                                   |
| [**Oid**](eku-oid.md)<br/>   | Lectura/escritura<br/> | Establece o recupera una cadena que contiene un valor de cadena de identificador de objeto [*EKU*](../secgloss/o-gly.md) (OID), tal como se define en Wincrypt.h.<br/> |



 

## <a name="remarks"></a>Comentarios

La colección y la propiedad siguientes usan el objeto **EKU:**

-   [**Colección de EKUs**](ekus.md)
-   [**Propiedad CertificateStatus.EKU**](certificatestatus-eku.md)

No se puede crear el objeto **EKU.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
