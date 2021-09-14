---
description: En la tabla siguiente se enumeran todos los valores HRESULT que pueden devolver los métodos de XPS Digital Signature API.
ms.assetid: d20707b0-55ea-438a-8ce3-972c61678928
title: XpS Digital Signature API Errors (Xpsdigitalsignature.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82c6f5efe7e67d27f7d94b5d1db2732139fa59
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168034"
---
# <a name="xps-digital-signature-api-errors"></a>Errores de API de firma digital XPS

En la tabla siguiente se enumeran todos **los valores HRESULT** que pueden devolver los métodos de XPS Digital Signature API. Tenga en cuenta que no todos los métodos pueden devolver todos los valores devueltos enumerados en esta tabla.



| Código o valor devuelto                                                                                                                                                                                                                                                                                  | Descripción                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ OK**</dt> </dl>                                                                                                                                                                 | El método se ha llevado a cabo de forma correcta.<br/>                                                                                                                                                  |
| <span id="XPS_E_INVALID_SIGNATUREBLOCK_MARKUP"></span><span id="xps_e_invalid_signatureblock_markup"></span><dl> <dt>**XPS \_ E \_ MARCADO \_ SIGNATUREBLOCK \_ NO**</dt> <dt>VÁLIDO 0x8052038b</dt> </dl> | Se encontró un error en el marcado XML del bloque de firma mientras se estaba leyendo el marcado de firma.<br/>                                                               |
| <span id="XPS_E_MARKUP_COMPATIBILITY_ELEMENTS"></span><span id="xps_e_markup_compatibility_elements"></span><dl> <dt>**XPS \_ E \_ ELEMENTOS DE COMPATIBILIDAD DE \_ \_ MARCADO**</dt> <dt>0x80520389</dt> </dl> | El [**valor XPS \_ SIGN \_ FLAGS especificaba**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) que no se esperaba ningún elemento de compatibilidad de marcado; sin embargo, se encontraron elementos de compatibilidad de marcado.<br/> |
| <span id="XPS_E_OBJECT_DETACHED"></span><span id="xps_e_object_detached"></span><dl> <dt>**XPS \_ E \_ OBJECT \_ DETACHED**</dt> <dt>0x8052038a</dt> </dl>                                            | La interfaz no está asociada al administrador de firmas.<br/>                                                                                                            |
| <span id="XPS_E_PACKAGE_ALREADY_OPENED"></span><span id="xps_e_package_already_opened"></span><dl> <dt>**XPS \_ E \_ PACKAGE \_ ALREADY \_ OPENED**</dt> <dt>0x80520387</dt> </dl>                      | Ya se ha abierto un paquete XPS en el administrador de firmas. <br/>                                                                                                      |
| <span id="XPS_E_PACKAGE_NOT_OPENED"></span><span id="xps_e_package_not_opened"></span><dl> <dt>**XPS \_ E \_ PACKAGE \_ NOT \_ OPENED**</dt> <dt>0x80520386</dt> </dl>                                  | Aún no se ha abierto un paquete XPS en el administrador de firmas. <br/>                                                                                                      |
| <span id="XPS_E_SIGNATUREID_DUP"></span><span id="xps_e_signatureid_dup"></span><dl> <dt>**XPS \_ E \_ SIGNATUREID \_ DUP**</dt> <dt>0x80520388</dt> </dl>                                            | Dos o más firmas tienen el mismo identificador.<br/>                                                                                                                               |
| <span id="XPS_E_SIGREQUESTID_DUP"></span><span id="xps_e_sigrequestid_dup"></span><dl> <dt>**XPS \_ E \_ SIGREQUESTID \_ DUP**</dt> <dt>0x80520385</dt> </dl>                                         | El identificador de solicitud de firma no es único dentro del bloque de firma.<br/>                                                                                                     |



 

## <a name="remarks"></a>Observaciones

Algunos métodos de API de firma digital XPS hacen llamadas a [Packaging](/previous-versions/windows/desktop/opc/packaging) API. Para obtener información sobre los valores devueltos de Packaging API, vea [Errores de empaquetado.](/previous-versions/windows/desktop/opc/packaging-errors)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                            |
| Encabezado<br/>                   | <dl> <dt>Xpsdigitalsignature.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>XpsDigitalSignature.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control de errores en COM](../com/error-handling-in-com.md)
</dt> <dt>

[Errores de empaquetado](/previous-versions/windows/desktop/opc/packaging-errors)
</dt> <dt>

[Valores devueltos de criptografía](/windows/desktop/SecCrypto/cryptography-return-values)
</dt> </dl>

 

