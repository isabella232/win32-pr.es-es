---
description: En la tabla siguiente se enumeran todos los valores HRESULT que pueden ser devueltos por los métodos de la API de firma digital XPS.
ms.assetid: d20707b0-55ea-438a-8ce3-972c61678928
title: Errores de la API de firma digital XPS (XpsDigitalSignature. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82c6f5efe7e67d27f7d94b5d1db2732139fa59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361241"
---
# <a name="xps-digital-signature-api-errors"></a>Errores de la API de firma digital XPS

En la tabla siguiente se enumeran todos los valores **HRESULT** que pueden ser devueltos por los métodos de la API de firma digital XPS. Tenga en cuenta que no todos los métodos pueden devolver todos los valores devueltos que se enumeran en esta tabla.



| Código o valor devuelto                                                                                                                                                                                                                                                                                  | Descripción                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ correcto**</dt> </dl>                                                                                                                                                                 | El método se ha llevado a cabo de forma correcta.<br/>                                                                                                                                                  |
| <span id="XPS_E_INVALID_SIGNATUREBLOCK_MARKUP"></span><span id="xps_e_invalid_signatureblock_markup"></span><dl> <dt>**XPS \_ E \_ no válido \_ SIGNATUREBLOCK \_ Markup**</dt> <dt>0x8052038b</dt> </dl> | Se encontró un error en el marcado XML del bloque de firma mientras se estaba leyendo el marcado de la firma.<br/>                                                               |
| <span id="XPS_E_MARKUP_COMPATIBILITY_ELEMENTS"></span><span id="xps_e_markup_compatibility_elements"></span><dl> <dt>**XPS \_ \_Elementos de \_ compatibilidad \_ de marcado E**</dt> <dt>0x80520389</dt> </dl> | El valor de [**\_ \_ marcas de signo de XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) especificó que no se esperaba ningún elemento de compatibilidad de marcado; sin embargo, se encontraron elementos de compatibilidad de marcado.<br/> |
| <span id="XPS_E_OBJECT_DETACHED"></span><span id="xps_e_object_detached"></span><dl> <dt>**XPS \_ Objeto E 0x8052038a \_ \_ desasociados**</dt> <dt></dt> </dl>                                            | La interfaz no está asociada al administrador de firmas.<br/>                                                                                                            |
| <span id="XPS_E_PACKAGE_ALREADY_OPENED"></span><span id="xps_e_package_already_opened"></span><dl> <dt>**XPS \_ El \_ paquete E \_ ya está \_ abierto**</dt> <dt>0x80520387</dt> </dl>                      | Ya se ha abierto un paquete XPS en el administrador de firmas. <br/>                                                                                                      |
| <span id="XPS_E_PACKAGE_NOT_OPENED"></span><span id="xps_e_package_not_opened"></span><dl> <dt>**XPS \_ E \_ paquete \_ no \_ abierto**</dt> <dt>0x80520386</dt> </dl>                                  | Todavía no se ha abierto un paquete XPS en el administrador de firmas. <br/>                                                                                                      |
| <span id="XPS_E_SIGNATUREID_DUP"></span><span id="xps_e_signatureid_dup"></span><dl> <dt>**XPS \_ E \_ SIGNATUREID \_ DUP**</dt> <dt>0x80520388</dt> </dl>                                            | Dos o más firmas tienen el mismo identificador.<br/>                                                                                                                               |
| <span id="XPS_E_SIGREQUESTID_DUP"></span><span id="xps_e_sigrequestid_dup"></span><dl> <dt>**XPS \_ E \_ SIGREQUESTID \_ DUP**</dt> <dt>0x80520385</dt> </dl>                                         | El identificador de solicitud de firma no es único dentro del bloque de firma.<br/>                                                                                                     |



 

## <a name="remarks"></a>Observaciones

Algunos métodos de la API de firma digital XPS realizan llamadas a la API de [empaquetado](/previous-versions/windows/desktop/opc/packaging) . Para obtener información sobre los valores devueltos de la API de empaquetado, consulte [errores de empaquetado](/previous-versions/windows/desktop/opc/packaging-errors).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                            |
| Encabezado<br/>                   | <dl> <dt>XpsDigitalSignature. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>XpsDigitalSignature. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control de errores en COM](../com/error-handling-in-com.md)
</dt> <dt>

[Errores de empaquetado](/previous-versions/windows/desktop/opc/packaging-errors)
</dt> <dt>

[Valores devueltos de criptografía](/windows/desktop/SecCrypto/cryptography-return-values)
</dt> </dl>

 

