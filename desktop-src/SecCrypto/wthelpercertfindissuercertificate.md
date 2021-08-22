---
description: Busca un certificado de emisor de los almacenes de certificados especificados que coincidan con el certificado de firmante especificado.
ms.assetid: c724f602-fc73-4857-941f-0f22a9e472d1
title: Función WTHelperCertFindIssuerCertificate
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
ms.openlocfilehash: 3c6c7957e969d04eaf65014e023a5f64e0826b6285fb878d9afefbd7cda25721
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895837"
---
# <a name="wthelpercertfindissuercertificate-function"></a>Función WTHelperCertFindIssuerCertificate

\[La **función WTHelperCertFindIssuerCertificate** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

La **función WTHelperCertFindIssuerCertificate** busca un certificado de emisor de los almacenes de certificados especificados que coincidan con el certificado de sujeto especificado.

> [!Note]  
> Esta función no tiene ninguna biblioteca de importación asociada. Debe usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Wintrust.dll.

 

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

*pChildContext* \[ En\]
</dt> <dd>

Certificado del firmante para el que se va a buscar un certificado de emisor correspondiente.

</dd> <dt>

*chStores* \[ En\]
</dt> <dd>

Número de elementos de la matriz *pahStores.*

</dd> <dt>

*pahStores* \[ En\]
</dt> <dd>

Matriz de almacenes de certificados en los que se va a buscar.

</dd> <dt>

*psftVerifyAsOf* \[ En\]
</dt> <dd>

Hora de comprobación.

</dd> <dt>

*dwEncoding* \[ En\]
</dt> <dd>

Valor **DWORD** que especifica los tipos de codificación del certificado que se comprobará. Para obtener información sobre los posibles tipos de codificación, vea [Tipos de codificación de certificados y mensajes.](certificate-and-message-encoding-types.md)

</dd> <dt>

*pdwConfidence* \[ out, opcional\]
</dt> <dd>

Este parámetro puede ser una combinación bit a bit de cero o más de los siguientes valores de confianza.



| Valor                                                                                                                                                                                                                                                                 | Significado                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="CERT_CONFIDENCE_SIG"></span><span id="cert_confidence_sig"></span><dl> <dt>**CERT \_ Confidence \_ SIG**</dt> <dt> 0x10000000</dt> </dl>                     | La firma del certificado es válida.<br/>                                           |
| <span id="CERT_CONFIDENCE_TIME"></span><span id="cert_confidence_time"></span><dl> <dt>**CERT \_ Tiempo \_ de confianza**</dt> <dt> 0x01000000</dt> </dl>                  | La hora del emisor del certificado es válida.<br/>                                         |
| <span id="_CERT_CONFIDENCE_TIMENEST"></span><span id="_cert_confidence_timenest"></span><dl> <dt> **CERT \_ CONFIDENCE \_ TIMENEST**</dt> <dt>0x00100000</dt> </dl>    | La hora del certificado es válida.<br/>                                                |
| <span id="_CERT_CONFIDENCE_AUTHIDEXT"></span><span id="_cert_confidence_authidext"></span><dl> <dt> **CERTIFICADO \_ DE CONFIANZA \_ AUTHIDEXT**</dt> <dt>0x00010000</dt> </dl> | La extensión de identificador de autoridad es válida.<br/>                                                 |
| <span id="_CERT_CONFIDENCE_HYGIENE"></span><span id="_cert_confidence_hygiene"></span><dl> <dt> **PROTECCIÓN \_ DE LA CONFIANZA \_ DE**</dt> <dt>0X00001000</dt> </dl>       | Como mínimo, la firma de la extensión de certificado y de identificador de entidad es válida.<br/> |
| <span id="_CERT_CONFIDENCE_HIGHEST"></span><span id="_cert_confidence_highest"></span><dl> <dt> **CERT \_ CONFIDENCE \_ HIGHEST**</dt> <dt>0x11111000</dt> </dl>       | Combinación de todos los demás valores de confianza.<br/>                                 |



 

</dd> <dt>

*dwError* \[ out\]
</dt> <dd>

Puntero a una variable **DWORD** que contiene el valor de error de este certificado, si procede.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Certificado de emisor que coincide con el certificado de sujeto especificado por el *parámetro pChildContext.*

## <a name="remarks"></a>Comentarios

Para encontrar correctamente un certificado de emisor que coincida, se deben cumplir los siguientes requisitos:

-   La firma del certificado de sujeto especificado por el *parámetro pChildContext* debe ser válida.
-   El **miembro rgExtension** del miembro **pCertInfo** del parámetro *pChildContext* debe contener una [**estructura CERT AUTHORITY KEY ID \_ \_ \_ \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) Los **miembros CertIssuer** y **CertSerialMember** de esta estructura coinciden mucho con los miembros correspondientes para el certificado del emisor.
-   El valor del *parámetro psftVerifyAsOf* debe estar dentro del período de validez del certificado de sujeto.
-   El período de validez del certificado del firmante debe estar dentro del período de validez del certificado del emisor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



 

 
