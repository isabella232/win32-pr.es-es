---
description: Proporciona acceso de solo lectura a las propiedades de uso extendido de claves (EKU) de un certificado.
ms.assetid: 636d7f65-d286-4800-a576-a23e6e9811b2
title: Objeto ExtendedKeyUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a93be1f6fe75559d0284ca955ca5b6e9c516eed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168929"
---
# <a name="extendedkeyusage-object"></a>Objeto ExtendedKeyUsage

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la clase [**X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **objeto ExtendedKeyUsage** proporciona acceso de solo lectura a las propiedades de uso extendido de claves (EKU) de un certificado.

## <a name="members"></a>Members

El **objeto ExtendedKeyUsage** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto ExtendedKeyUsage** tiene estas propiedades.



| Propiedad                                                     | Tipo de acceso          | Descripción                                                                                                                             |
|:-------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**EKUs**](extendedkeyusage-ekus.md)<br/>             | Solo lectura<br/> | [**Colección de EKU**](ekus.md) que contiene los [**objetos EKU**](eku.md) del certificado.<br/>                            |
| [**IsCritical**](extendedkeyusage-iscritical.md)<br/> | Solo lectura<br/> | Recupera un valor **booleano** que indica si la extensión EKU está marcada como crítica.<br/>                                   |
| [**IsPresent**](extendedkeyusage-ispresent.md)<br/>   | Solo lectura<br/> | Recupera un valor **booleano** que indica si la extensión EKU está presente.<br/> Esta es la propiedad predeterminada. <br/> |



 

## <a name="remarks"></a>Observaciones

No **se puede crear el objeto ExtendedKeyUsage.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
