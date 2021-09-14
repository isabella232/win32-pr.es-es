---
description: Recupera el nombre del certificado resultante de una llamada correcta anterior a ISCrdEnr::enroll.
ms.assetid: e33b217a-b717-49bd-b0f3-3ba9229a0696
title: Método ISCrdEnr::getEnrolledCertificateName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getEnrolledCertificateName
- SCrdEnr.getEnrolledCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3c9640e7719d2b5ac0e576384246cda5e1b2bfe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361834"
---
# <a name="iscrdenrgetenrolledcertificatename-method"></a>Método ISCrdEnr::getEnrolledCertificateName

El **método getEnrolledCertificateName** recupera el nombre del certificado resultante de una llamada correcta anterior a [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)).

Este método también se puede usar para mostrar el certificado en un cuadro de diálogo. Este método llama a la función [**CertGetNameString de**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) [*CryptoAPI.*](../secgloss/c-gly.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT getEnrolledCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pBstrCertName
);
```


```VB

SCrdEnr.getEnrolledCertificateName( _
  ByVal dwFlags, _
  ByRef pBstrCertName _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Valor que determina si el certificado se muestra en un cuadro de diálogo. Si este valor es SCARD ENROLL NO DISPLAY CERT (definido como 0x01), no se muestra el certificado inscrito; cualquier otro valor hace que el certificado inscrito se muestre en el cuadro de diálogo \_ \_ \_ \_ Certificado. 

</dd> <dt>

*pBstrCertName* \[ out\]
</dt> <dd>

Puntero a una cadena que devuelve el nombre del certificado recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se realiza correctamente, el método devuelve S \_ OK.

Si se produce un error en el método , devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

### <a name="vb"></a>VB

Cadena que representa el nombre del certificado recuperado.

## <a name="remarks"></a>Observaciones

Dado que este método funciona en un certificado existente, debe haber llamado correctamente a [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) para poder llamar a **getEnrolledCertificateName**.

El **método getEnrolledCertificateName** llama a la función [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) para recuperar el nombre del certificado según la secuencia descrita para el valor CERT NAME SIMPLE DISPLAY TYPE del parámetro dwType de \_ \_ \_ \_ **CertGetNameString.** 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID ISCrdEnr se define como \_ 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))
</dt> </dl>

 

 
