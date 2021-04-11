---
description: Muestra un cuadro de diálogo que permite al usuario seleccionar un certificado.
ms.assetid: 242c19a7-179b-4fc0-a050-a1b598566a6b
title: Función CryptUIDlgSelectCertificate
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 65d9993cd1e035473e731056d33b7a391ef47b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278993"
---
# <a name="cryptuidlgselectcertificate-function"></a>Función CryptUIDlgSelectCertificate

La función **CryptUIDlgSelectCertificate** muestra un cuadro de diálogo que permite al usuario seleccionar un certificado.

## <a name="syntax"></a>Sintaxis


```C++
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PCSC* \[ de\]
</dt> <dd>

Puntero a una estructura de estructura [**CRYPTUI \_ SELECTCERTIFICATE \_**](cryptui-selectcertificate-struct.md) que contiene información sobre el cuadro de diálogo que se va a mostrar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Puntero a una estructura [**de \_ contexto de certificado**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) que representa el certificado seleccionado por el usuario. Cuando haya terminado de utilizar este certificado, debe pasar este puntero a la función [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) para reducir el recuento de referencias del contexto de certificado.

Si el miembro **dwFlags** de la estructura *PCSC* no contiene el marcador **de \_ \_ selección MultiSelect CRYPTUI SELECTCERT** , un valor devuelto de **null** significa que el usuario ha cerrado el cuadro de diálogo sin seleccionar ningún certificado.

Si el miembro **dwFlags** de la estructura *PCSC* contiene el marcador **de \_ \_ selección MultiSelect CRYPTUI SELECTCERT** , esta función siempre devuelve **null**. Los certificados seleccionados se incluirán en el almacén de certificados representado por el miembro **hSelectedCertStore** de *PCSC*. Si el número de certificados en el almacén es el mismo antes y después de llamar a **CryptUIDlgSelectCertificate**, el usuario ha cerrado el cuadro de diálogo sin seleccionar ningún certificado.

## <a name="remarks"></a>Observaciones

Si el miembro **dwFlags** de la estructura de [**\_ \_ struct Cryptui SELECTCERTIFICATE**](cryptui-selectcertificate-struct.md) se establece **en \_ cryptui SELECTCERT \_ Legacy**, se muestra el cuadro de diálogo heredado. De lo contrario, se muestra el cuadro de diálogo de selección de certificado actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                              |
| Finalización del soporte técnico<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                       |
| Biblioteca<br/>                  | <dl> <dt>Cryptui. lib</dt> </dl>            |
| Archivo DLL<br/>                      | <dl> <dt>Cryptui.dll</dt> </dl>            |
| Nombres Unicode y ANSI<br/>   | **CryptUIDlgSelectCertificateW** (Unicode) y **CryptUIDlgSelectCertificateA** (ANSI)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CRYPTUI \_ SELECTCERTIFICATE \_ struct**](cryptui-selectcertificate-struct.md)
</dt> </dl>

�

�




