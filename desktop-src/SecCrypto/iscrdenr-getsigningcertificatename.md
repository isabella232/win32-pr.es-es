---
description: Recupera el nombre del firmante del certificado de firma.
ms.assetid: e50b1e12-ec89-4d58-aa57-dc24aa2409ef
title: 'ISCrdEnr:: getSigningCertificateName (método)'
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
ms.openlocfilehash: 8d9a8a84067e82a18e5066721f3e7f39d075c339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423960"
---
# <a name="iscrdenrgetsigningcertificatename-method"></a>ISCrdEnr:: getSigningCertificateName (método)

El método **getSigningCertificateName** recupera el nombre del firmante del certificado de firma.

Este método también se puede utilizar para mostrar el certificado en un cuadro de diálogo. Este método llama a la función [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)de [*CryptoAPI*](../secgloss/c-gly.md) .

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

*dwFlags* \[ de\]
</dt> <dd>

Valor que determina si el certificado se muestra en un cuadro de diálogo. Si este valor es PPAC \_ inscribir \_ no \_ Mostrar \_ certificado (definido como 0x01), no se muestra el certificado de firma; cualquier otro valor da lugar a que el certificado de firma se muestre en el cuadro de diálogo **certificado** .

</dd> <dt>

*pbstrSigningCertName* \[ enuncia\]
</dt> <dd>

Puntero a una cadena que devuelve el nombre del certificado de firma. El certificado de firma se usará para firmar la [*solicitud de certificado*](../secgloss/c-gly.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se ejecuta correctamente, el método devuelve S \_ correcto.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

### <a name="vb"></a>VB

Cadena que representa el nombre del certificado de firma. El certificado de firma se usará para firmar la [*solicitud de certificado*](../secgloss/c-gly.md).

## <a name="remarks"></a>Observaciones

El método **getSigningCertificateName** devuelve el nombre de sujeto del certificado que ha seleccionado (u otro administrador) en una llamada correcta anterior a [**ISCrdEnr:: selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) o [**ISCrdEnr:: setSigningCertificate**](iscrdenr-setsigningcertificate.md). Este método llama a la función [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) para recuperar el nombre de sujeto según la secuencia descrita para el \_ \_ \_ \_ valor de tipo de presentación simple de nombre de certificado del parámetro *dwType* de **CertGetNameString**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)
</dt> </dl>

 

 
