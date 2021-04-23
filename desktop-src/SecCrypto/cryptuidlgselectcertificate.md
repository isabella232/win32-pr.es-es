---
description: Muestra un cuadro de diálogo que permite a un usuario seleccionar un certificado.
ms.assetid: 242c19a7-179b-4fc0-a050-a1b598566a6b
title: Función CryptUIDlgSelectCertificate
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 8f015796671990491407d91cbd51761816c5434b
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925698"
---
# <a name="cryptuidlgselectcertificate-function"></a>Función CryptUIDlgSelectCertificate

La **función CryptUIDlgSelectCertificate** muestra un cuadro de diálogo que permite a un usuario seleccionar un certificado.

## <a name="syntax"></a>Sintaxis


```C++
PCCERT_CONTEXT WINAPI CryptUIDlgSelectCertificate(
  _In_  PCCRYPTUI_SELECTCERTIFICATE_STRUCT pcsc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcsc* \[ En\]
</dt> <dd>

Puntero a una [**estructura CRYPTUI \_ SELECTCERTIFICATE \_ STRUCT**](cryptui-selectcertificate-struct.md) que contiene información sobre el cuadro de diálogo que se mostrará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Puntero a una [**estructura CERT \_ CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) que representa el certificado seleccionado por el usuario. Cuando haya terminado de usar este certificado, debe pasar este puntero a la función [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) para disminuir el recuento de referencias del contexto del certificado.

Si el **miembro dwFlags** de la estructura *pcsc* no contiene la marca **CRYPTUI \_ SELECTCERT \_ MULTISELECT,** un valor devuelto de **NULL** significa que el usuario cerró el cuadro de diálogo sin seleccionar un certificado.

Si el **miembro dwFlags** de la estructura *pcsc* contiene la marca **CRYPTUI \_ SELECTCERT \_ MULTISELECT,** esta función siempre devuelve **NULL.** Los certificados seleccionados se incluirán en el almacén de certificados representado por el **miembro hSelectedCertStore** de *pcsc*. Si el número de certificados del almacén es el mismo antes y después de llamar a **CryptUIDlgSelectCertificate,** el usuario cerró el cuadro de diálogo sin seleccionar ningún certificado.

## <a name="remarks"></a>Comentarios

Si el **miembro dwFlags** de la estructura [**CRYPTUI \_ SELECTCERTIFICATE \_ STRUCT**](cryptui-selectcertificate-struct.md) se establece en **CRYPTUI \_ SELECTCERT \_ LEGACY,** se muestra el cuadro de diálogo heredado. De lo contrario, se muestra el cuadro de diálogo de selección de certificado actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                              |
| Finalización del soporte técnico<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                       |
| Biblioteca<br/>                  | <dl> <dt>Cryptui.lib</dt> </dl>            |
| Archivo DLL<br/>                      | <dl> <dt>Cryptui.dll</dt> </dl>            |
| Nombres Unicode y ANSI<br/>   | **CryptUIDlgSelectCertificateW** (Unicode) y **CryptUIDlgSelectCertificateA** (ANSI)<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CRYPTUI \_ SELECTCERTIFICATE \_ STRUCT**](cryptui-selectcertificate-struct.md)
</dt> </dl>






