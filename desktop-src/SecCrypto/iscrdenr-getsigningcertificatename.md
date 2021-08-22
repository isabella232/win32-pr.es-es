---
description: Recupera el nombre del firmantes del certificado de firma.
ms.assetid: e50b1e12-ec89-4d58-aa57-dc24aa2409ef
title: Método ISCrdEnr::getSigningCertificateName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getSigningCertificateName
- SCrdEnr.getSigningCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 29933856eb644e638e9e58c8da0b0e3d6234e4f0175925c8a1fb5b48b126e3ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622405"
---
# <a name="iscrdenrgetsigningcertificatename-method"></a>Método ISCrdEnr::getSigningCertificateName

El **método getSigningCertificateName** recupera el nombre del firmante del certificado de firma.

Este método también se puede usar para mostrar el certificado en un cuadro de diálogo. Este método llama a la función [**CertGetNameString de**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) [*CryptoAPI.*](../secgloss/c-gly.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT getSigningCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrSigningCertName
);
```


```VB

SCrdEnr.getSigningCertificateName( _
  ByVal dwFlags, _
  ByRef pbstrSigningCertName _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Valor que determina si el certificado se muestra en un cuadro de diálogo. Si este valor es SCARD ENROLL NO DISPLAY CERT (definido como 0x01), no se muestra el certificado de firma; cualquier otro valor hace que el certificado de firma se muestre en el cuadro de diálogo \_ \_ \_ \_ Certificado. 

</dd> <dt>

*pbstrSigningCertName* \[ out\]
</dt> <dd>

Puntero a una cadena que devuelve el nombre del certificado de firma. El certificado de firma se usará para firmar la solicitud [*de certificado*](../secgloss/c-gly.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se realiza correctamente, el método devuelve S \_ OK.

Si se produce un error en el método , devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

### <a name="vb"></a>VB

Cadena que representa el nombre del certificado de firma. El certificado de firma se usará para firmar la solicitud [*de certificado*](../secgloss/c-gly.md).

## <a name="remarks"></a>Comentarios

El **método getSigningCertificateName** devuelve el nombre del firmante del certificado que ha seleccionado (u otro administrador) en una llamada correcta anterior a [**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) o [**ISCrdEnr::setSigningCertificate**](iscrdenr-setsigningcertificate.md). Este método llama a la [**función CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) para recuperar el nombre del sujeto según la secuencia descrita para el valor CERT NAME SIMPLE DISPLAY TYPE del parámetro dwType de \_ \_ \_ \_ **CertGetNameString.** 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID ISCrdEnr se define como \_ 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)
</dt> </dl>

 

 
