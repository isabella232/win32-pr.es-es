---
description: Establece o recupera la opción de certificado del firmante.
ms.assetid: 2362b9d4-d4d8-46fb-8791-7e856827fb31
title: Propiedad Signer.Options
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Options
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7b4a787524e967b5356ed7fb5531a3ec7d7dbfb99d57fc75217a82f220468db7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898841"
---
# <a name="signeroptions-property"></a>Propiedad Signer.Options

\[La **propiedad Options** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase CmsSigner en**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **propiedad Options** establece o recupera la opción de certificado del firmante.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
Signer.Options As CAPICOM_CERTIFICATE_INCLUDE_OPTION
```



## <a name="property-value"></a>Valor de propiedad

Valor de la [**enumeración CAPICOM \_ CERTIFICATE INCLUDE \_ \_ OPTION**](capicom-certificate-include-option.md) que especifica la opción de certificado del firmante. El valor predeterminado es CAPICOM \_ CERTIFICATE INCLUDE CHAIN EXCEPT \_ \_ \_ \_ ROOT. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                                             | Significado                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ INCLUDE \_ CHAIN \_ EXCEPT \_ ROOT**</dt> </dl> | Guarda todos los certificados de la cadena con la excepción de la entidad raíz.<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**EL CERTIFICADO CAPICOM \_ \_ INCLUYE CADENA \_ \_ COMPLETA**</dt> </dl>                    | Guarda la cadena de certificados completa.<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**CERTIFICADO CAPICOM \_ INCLUIR \_ SOLO ENTIDAD \_ \_ \_ FINAL**</dt> </dl>       | Guarda solo el certificado de entidad final.<br/>                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Firmante**](signer.md)
</dt> </dl>

 

 
