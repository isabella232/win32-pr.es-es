---
description: Devuelve un objeto de certificados que contiene todos los certificados que coinciden con los criterios de búsqueda especificados.
ms.assetid: a2b8f4d4-dce3-467b-aaa0-a125056a1dd3
title: 'ICertificates2:: Find (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Find
- ICertificates2.Find
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9ea15891c33a0789e5b6746b55dfd0b0eb602afc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650165"
---
# <a name="icertificates2find-method"></a>ICertificates2:: Find (método)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **Find** devuelve un objeto [**Certificates**](certificates.md) que contiene todos los certificados que coinciden con los criterios de búsqueda especificados. Este método se presentó en CAPICOM 2,0.

## <a name="syntax"></a>Sintaxis


```VB
Certificates.Find( _
  ByVal FindType, _
  [ ByVal varCriteria ], _
  [ ByVal bFindValidOnly ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FindType* \[ de\]
</dt> <dd>

Un valor de la enumeración de búsqueda de certificado de CAPICOM que especifica el tipo de criterio de coincidencia proporcionado en el parámetro *varCriteria* . [**\_ \_ \_**](capicom-certificate-find-type.md) En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                                        | Significado                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_FIND_SHA1_HASH"></span><span id="capicom_certificate_find_sha1_hash"></span><dl> <dt>**Certificado de CAPICOM, \_ \_ Buscar \_ \_ hash SHA1**</dt> </dl>                              | Devuelve los certificados con un hash SHA1 que coincide con el hash SHA1 especificado en el parámetro *varCriteria* .<br/>                                                                                                                              |
| <span id="CAPICOM_CERTIFICATE_FIND_SUBJECT_NAME"></span><span id="capicom_certificate_find_subject_name"></span><dl> <dt>**\_el certificado de CAPICOM \_ encuentra \_ \_ el nombre del firmante**</dt> </dl>                     | Devuelve certificados cuyo nombre de sujeto coincide exactamente o parcialmente con el nombre de sujeto especificado en el parámetro *varCriteria* . Esta llamada busca solo en el campo de nombre de sujeto.<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_FIND_ISSUER_NAME"></span><span id="capicom_certificate_find_issuer_name"></span><dl> <dt>**\_nombre del \_ emisor de búsqueda de certificado de \_ CAPICOM \_**</dt> </dl>                        | Devuelve certificados cuyo nombre de emisor coincide exactamente o parcialmente con el nombre del emisor especificado en el parámetro *varCriteria* . Esta llamada busca solo en el campo de nombre del emisor.<br/>                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_ROOT_NAME"></span><span id="capicom_certificate_find_root_name"></span><dl> <dt>**nombre de la raíz del certificado de CAPICOM \_ \_ \_ \_**</dt> </dl>                              | Devuelve certificados cuyo nombre de sujeto raíz coincide exactamente o parcialmente con el nombre de sujeto raíz especificado en el parámetro *varCriteria* . Esta llamada crea una cadena. Esta llamada busca en el campo de nombre de sujeto del certificado raíz.<br/> |
| <span id="CAPICOM_CERTIFICATE_FIND_TEMPLATE_NAME"></span><span id="capicom_certificate_find_template_name"></span><dl> <dt>**\_nombre de \_ plantilla de búsqueda de certificado de CAPICOM \_ \_**</dt> </dl>                  | Devuelve los certificados cuyo nombre de plantilla coincide con el nombre de plantilla especificado en el parámetro *varCriteria* .<br/>                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENSION"></span><span id="capicom_certificate_find_extension"></span><dl> <dt>**\_extensión de \_ búsqueda de certificado de CAPICOM \_**</dt> </dl>                               | Devuelve los certificados que tienen una extensión que coincide con la extensión especificada en el parámetro *varCriteria* .<br/>                                                                                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENDED_PROPERTY"></span><span id="capicom_certificate_find_extended_property"></span><dl> <dt>**\_ \_ \_ propiedad extendida de búsqueda de certificado de CAPICOM \_**</dt> </dl>      | Devuelve los certificados del almacén que contienen explícitamente una propiedad extendida con el valor especificado en el parámetro *varCriteria* .<br/>                                                                                                 |
| <span id="CAPICOM_CERTIFICATE_FIND_APPLICATION_POLICY"></span><span id="capicom_certificate_find_application_policy"></span><dl> <dt>**\_Directiva de \_ aplicación de búsqueda de certificado de CAPICOM \_ \_**</dt> </dl>   | Devuelve los certificados del almacén que tienen una extensión de uso mejorado de claves, una extensión de directiva de aplicación o una propiedad extendida especificada en el parámetro *varCriteria* .<br/>                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_CERTIFICATE_POLICY"></span><span id="capicom_certificate_find_certificate_policy"></span><dl> <dt>**\_Directiva de \_ certificado de búsqueda \_ \_ de certificado de CAPICOM**</dt> </dl>   | Devuelve los certificados que contienen el OID de la Directiva en la extensión de directiva de certificado especificada en el parámetro *varCriteria* .<br/>                                                                                                          |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_VALID"></span><span id="capicom_certificate_find_time_valid"></span><dl> <dt>**tiempo de búsqueda de certificado de CAPICOM \_ \_ \_ \_ válido**</dt> </dl>                           | Devuelve certificados cuya hora es válida.<br/>                                                                                                                                                                                               |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_NOT_YET_VALID"></span><span id="capicom_certificate_find_time_not_yet_valid"></span><dl> <dt>**tiempo de búsqueda de certificado de CAPICOM \_ \_ \_ \_ no \_ \_ válido todavía**</dt> </dl> | Devuelve certificados cuya hora todavía no es válida.<br/>                                                                                                                                                                                       |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_EXPIRED"></span><span id="capicom_certificate_find_time_expired"></span><dl> <dt>**tiempo de búsqueda de certificado de CAPICOM \_ \_ \_ \_ expirado**</dt> </dl>                     | Devuelve los certificados cuya hora ha expirado.<br/>                                                                                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_KEY_USAGE"></span><span id="capicom_certificate_find_key_usage"></span><dl> <dt>**uso de la clave de certificado de CAPICOM \_ \_ \_ \_**</dt> </dl>                              | Devuelve los certificados que contienen los usos de clave en la extensión KeyUsage especificada en el parámetro *varCriteria* . Si la extensión KeyUsage no está presente, se supone que todos los usos de clave no están disponibles.<br/>                           |



 

</dd> <dt>

*varCriteria* \[ en, opcional\]
</dt> <dd>

Variante que contiene los criterios de búsqueda. Estos datos deben coincidir con el tipo de datos especificado en el parámetro *FindType* . Si el valor del parámetro *FindType* es válido para el certificado de CAPICOM, el tiempo de \_ búsqueda del certificado de \_ \_ \_ CAPICOM \_ \_ \_ \_ todavía no es \_ \_ válido, o \_ el tiempo de búsqueda de certificado de CAPICOM \_ \_ \_ expiró y no se pasa un valor a este parámetro, se supone la hora actual. Para obtener ejemplos de cada tipo de datos, vea la sección Comentarios. El valor predeterminado es 0.

</dd> <dt>

*bFindValidOnly* \[ en, opcional\]
</dt> <dd>

Valor booleano que indica si solo se devuelven certificados válidos. El valor predeterminado es false; Esto indica que se devuelven todos los certificados que coinciden con los criterios de búsqueda.

Si es true, la búsqueda no devolverá los siguientes tipos de certificados:

-   Certificados cuyo tiempo ha expirado o aún no es válido.
-   Los certificados no están encadenados correctamente.
-   Certificados que tienen problemas de firma.
-   Certificados que se revocan.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto [**Certificates**](certificates.md) que contiene los resultados de la búsqueda.

**CAPICOM 2,1:** El objeto de [**certificados**](certificates.md) que se devuelve contiene referencias a los certificados de la colección en la que se realizó la búsqueda. Cualquier cambio realizado en los certificados del objeto de **certificados** devueltos se refleja en esa colección.

**Capicom 2,0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 y CAPICOM 2.0.0.3:** El objeto de [**certificados**](certificates.md) que se devuelve contiene copias de los certificados de la colección en la que se realizó la búsqueda. Los cambios realizados en los certificados del objeto de **certificados** devueltos no se reflejan en esa colección.

## <a name="remarks"></a>Observaciones

En los siguientes ejemplos se muestran los criterios de búsqueda posibles para los distintos tipos de criterios de búsqueda.



| *FindType* (parámetro)                              | parámetro *varCriteria*                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Certificado de CAPICOM, \_ \_ Buscar \_ \_ hash SHA1            | 33F362434B577F844BB7226BE36F7D72EF9D9393                                                                                           |
| \_el certificado de CAPICOM \_ encuentra \_ \_ el nombre del firmante         | "NameOfPerson"                                                                                                                     |
| \_nombre del \_ emisor de búsqueda de certificado de \_ CAPICOM \_          | VeriSign                                                                                                                         |
| nombre de la raíz del certificado de CAPICOM \_ \_ \_ \_            | "Entidad de certificación raíz de Microsoft"                                                                                                         |
| \_nombre de \_ plantilla de búsqueda de certificado de CAPICOM \_ \_        | "AutoEnrollEFS"<br/> 1.3.6.1.4.1.311.21.8.3692315854.1256661383.1690418588.4201632533.1741915387.2177932052<br/>       |
| \_extensión de \_ búsqueda de certificado de CAPICOM \_             | "2.5.29.31"<br/> \_extensión de \_ uso de claves \_ \_ de CAPICOM OID<br/> "Lista de distribución de CRL"<br/>                           |
| \_ \_ \_ propiedad extendida de búsqueda de certificado de CAPICOM \_    | \_información de \_ Prov de clave \_ \_ de CAPICOM PROPID                                                                                                   |
| \_Directiva de \_ aplicación de búsqueda de certificado de CAPICOM \_ \_   | 1.3.6.1.5.5.7.3.3<br/> "1.3.6.1.5.5.7.3.4"<br/> \_EKU de \_ autenticación del servidor \_ \_ de CAPICOM OID<br/> "Firma de código"<br/> |
| \_Directiva de \_ certificado de búsqueda \_ \_ de certificado de CAPICOM   | "1.3.6.1.5.5.7.3.4.3.5"<br/> "Corporate High Assurance"<br/>                                                           |
| tiempo de búsqueda de certificado de CAPICOM \_ \_ \_ \_ válido           | \#04/15/2002, 6:00 PM\#                                                                                                            |
| tiempo de búsqueda de certificado de CAPICOM \_ \_ \_ \_ no \_ \_ válido todavía | \#04/15/2002, 6:00 PM\#                                                                                                            |
| tiempo de búsqueda de certificado de CAPICOM \_ \_ \_ \_ expirado         | \#04/15/2002, 6:00 PM\#                                                                                                            |
| uso de la clave de certificado de CAPICOM \_ \_ \_ \_            | CAPICOM \_ \_ solo cifrado \_ uso de claves \_                                                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Certificados**](certificates.md)
</dt> <dt>

[**OID de CAPICOM \_**](capicom-oid.md)
</dt> </dl>

 

 
