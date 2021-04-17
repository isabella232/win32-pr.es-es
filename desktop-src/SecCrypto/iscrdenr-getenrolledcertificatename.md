---
description: 'Recupera el nombre del certificado resultante de una llamada correcta anterior a ISCrdEnr:: ENROLL.'
ms.assetid: e33b217a-b717-49bd-b0f3-3ba9229a0696
title: 'ISCrdEnr:: getEnrolledCertificateName (método)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688189"
---
# <a name="iscrdenrgetenrolledcertificatename-method"></a>ISCrdEnr:: getEnrolledCertificateName (método)

El método **getEnrolledCertificateName** recupera el nombre del certificado resultante de una llamada correcta anterior a [**ISCrdEnr:: ENROLL**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)).

Este método también se puede utilizar para mostrar el certificado en un cuadro de diálogo. Este método llama a la función [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)de [*CryptoAPI*](../secgloss/c-gly.md) .

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

*dwFlags* \[ de\]
</dt> <dd>

Valor que determina si el certificado se muestra en un cuadro de diálogo. Si este valor es PPAC \_ inscribir \_ no \_ Mostrar \_ certificado (definido como 0x01), no se muestra el certificado inscrito; cualquier otro valor hace que el certificado inscrito se muestre en el cuadro de diálogo **certificado** .

</dd> <dt>

*pBstrCertName* \[ enuncia\]
</dt> <dd>

Puntero a una cadena que devuelve el nombre del certificado recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se ejecuta correctamente, el método devuelve S \_ correcto.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

### <a name="vb"></a>VB

Cadena que representa el nombre del certificado recuperado.

## <a name="remarks"></a>Observaciones

Dado que este método funciona en un certificado existente, debe haber llamado correctamente a [**ISCrdEnr:: ENROLL**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) antes de poder llamar a **getEnrolledCertificateName**.

El método **getEnrolledCertificateName** llama a la función [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) para recuperar el nombre del certificado según la secuencia descrita para el \_ \_ \_ \_ valor de tipo de presentación simple de nombre de certificado del parámetro *dwType* de **CertGetNameString**.

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

[**ISCrdEnr:: ENROLL**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))
</dt> </dl>

 

 
