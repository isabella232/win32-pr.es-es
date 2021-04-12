---
description: Busca un certificado de emisor de los almacenes de certificados especificados que coincide con el certificado de sujeto especificado.
ms.assetid: c724f602-fc73-4857-941f-0f22a9e472d1
title: WTHelperCertFindIssuerCertificate función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperCertFindIssuerCertificate
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 99135ac22509b288726732ca4a16248b304f294b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277003"
---
# <a name="wthelpercertfindissuercertificate-function"></a>WTHelperCertFindIssuerCertificate función)

\[La función **WTHelperCertFindIssuerCertificate** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

La función **WTHelperCertFindIssuerCertificate** busca un certificado de emisor de los almacenes de certificados especificados que coincide con el certificado de sujeto especificado.

> [!Note]  
> Esta función no tiene ninguna biblioteca de importación asociada. Debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Wintrust.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
PCCERT_CONTEXT WINAPI WTHelperCertFindIssuerCertificate(
  _In_      PCCERT_CONTEXT pChildContext,
  _In_      DWORD          chStores,
  _In_      HCERTSTORE     *pahStores,
  _In_      FILETIME       *psftVerifyAsOf,
  _In_      DWORD          dwEncoding,
  _Out_opt_ DWORD          *pdwConfidence,
  _Out_     DWORD          *dwError
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pChildContext* \[ de\]
</dt> <dd>

Certificado del firmante para el que se va a buscar un certificado de emisor coincidente.

</dd> <dt>

*chStores* \[ de\]
</dt> <dd>

Número de elementos de la matriz *pahStores* .

</dd> <dt>

*pahStores* \[ de\]
</dt> <dd>

Matriz de almacenes de certificados en los que se va a buscar.

</dd> <dt>

*psftVerifyAsOf* \[ de\]
</dt> <dd>

Hora de comprobación.

</dd> <dt>

*dwEncoding* \[ de\]
</dt> <dd>

Valor **DWORD** que especifica los tipos de codificación del certificado que se va a comprobar. Para obtener información sobre los posibles tipos de codificación, consulte [certificados y tipos de codificación de mensajes](certificate-and-message-encoding-types.md).

</dd> <dt>

*pdwConfidence* \[ out, opcional\]
</dt> <dd>

Este parámetro puede ser una combinación bit a bit de cero o más de los siguientes valores de confianza.



| Value                                                                                                                                                                                                                                                                 | Significado                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="CERT_CONFIDENCE_SIG"></span><span id="cert_confidence_sig"></span><dl> <dt>**Certificado \_ de \_Firma de confianza**</dt> <dt> 0x10000000</dt> </dl>                     | La firma del certificado es válida.<br/>                                           |
| <span id="CERT_CONFIDENCE_TIME"></span><span id="cert_confidence_time"></span><dl> <dt>**Certificado \_ de 0x01000000 de \_ tiempo de confianza**</dt> <dt></dt> </dl>                  | La hora del emisor del certificado es válida.<br/>                                         |
| <span id="_CERT_CONFIDENCE_TIMENEST"></span><span id="_cert_confidence_timenest"></span><dl> <dt> **Confianza de CERT \_ \_ TIMENEST**</dt> <dt>0x00100000</dt> </dl>    | La hora del certificado es válida.<br/>                                                |
| <span id="_CERT_CONFIDENCE_AUTHIDEXT"></span><span id="_cert_confidence_authidext"></span><dl> <dt> **Confianza de CERT \_ \_ AUTHIDEXT**</dt> <dt>0x00010000</dt> </dl> | La extensión de ID. de entidad es válida.<br/>                                                 |
| <span id="_CERT_CONFIDENCE_HYGIENE"></span><span id="_cert_confidence_hygiene"></span><dl> <dt>0x00001000</dt> de <dt> **\_ \_ higiene de confianza de certificados**</dt> </dl>       | Como mínimo, la firma de la extensión de identificador de entidad y certificado es válida.<br/> |
| <span id="_CERT_CONFIDENCE_HIGHEST"></span><span id="_cert_confidence_highest"></span><dl> <dt> **Confianza de certificado \_ \_ más alta**</dt> <dt>0x11111000</dt> </dl>       | Una combinación de todos los demás valores de confianza.<br/>                                 |



 

</dd> <dt>

*dwError* \[ enuncia\]
</dt> <dd>

Un puntero a una variable **DWORD** que contiene el valor de error de este certificado, si procede.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Un certificado de emisor que coincida con el certificado de firmante especificado por el parámetro *pChildContext* .

## <a name="remarks"></a>Observaciones

Para encontrar correctamente un certificado de emisor coincidente, deben cumplirse los siguientes requisitos:

-   La firma del certificado de sujeto especificado por el parámetro *pChildContext* debe ser válida.
-   El miembro **rgExtension** del miembro **PCertInfo** del parámetro *pChildContext* debe contener una estructura de [**\_ \_ \_ \_ información de identificador de clave de entidad emisora de certificados**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) . Los miembros **CertIssuer** y **CertSerialMember** de esta estructura coinciden mucho con los miembros correspondientes del certificado del emisor.
-   El valor del parámetro *psftVerifyAsOf* debe estar dentro del período de validez del certificado del firmante.
-   El período de validez del certificado del firmante debe estar dentro del período de validez del certificado del emisor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



 

 
