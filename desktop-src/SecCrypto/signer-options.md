---
description: Establece o recupera la opción de certificado del firmante.
ms.assetid: 2362b9d4-d4d8-46fb-8791-7e856827fb31
title: Propiedad Signer. Options
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
ms.openlocfilehash: c22cf7b9d9ebe7e98e534d62b0a2771391c6cacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671234"
---
# <a name="signeroptions-property"></a>Propiedad Signer. Options

\[La propiedad **Opciones** está disponible para su uso en los sistemas operativos especificados en la sección requisitos. En su lugar, use la [**clase CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propiedad **Options** establece o recupera la opción de certificado del firmante.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Signer.Options As CAPICOM_CERTIFICATE_INCLUDE_OPTION
```



## <a name="property-value"></a>Valor de propiedad

Un valor de la enumeración de la [**\_ \_ \_ opción incluir certificado de CAPICOM**](capicom-certificate-include-option.md) que especifica la opción de certificado del firmante. El valor predeterminado es el \_ certificado de CAPICOM \_ incluir \_ cadena \_ excepto \_ raíz. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                                             | Significado                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**el \_ certificado de CAPICOM \_ incluye una \_ cadena excepto la \_ \_ raíz**</dt> </dl> | Guarda todos los certificados de la cadena con la excepción de la entidad raíz.<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**el \_ certificado de CAPICOM \_ incluye una \_ \_ cadena entera**</dt> </dl>                    | Guarda la cadena de certificados completa.<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**el \_ certificado de CAPICOM \_ incluye \_ \_ solo la entidad final \_**</dt> </dl>       | Guarda solo el certificado de entidad final.<br/>                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Firmante**](signer.md)
</dt> </dl>

 

 
