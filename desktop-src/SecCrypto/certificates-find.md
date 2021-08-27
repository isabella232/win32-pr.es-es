---
description: Devuelve un objeto Certificates que contiene todos los certificados que coinciden con los criterios de búsqueda especificados.
ms.assetid: a2b8f4d4-dce3-467b-aaa0-a125056a1dd3
title: ICertificates2::Find (Método)
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
ms.openlocfilehash: 51e3d19348f0bff9cdbe0b4211d648a25025b2a3ab8feee9df6f804486265857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100995"
---
# <a name="icertificates2find-method"></a>ICertificates2::Find (Método)

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2Collection en**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método Find** devuelve un objeto [**Certificates**](certificates.md) que contiene todos los certificados que coinciden con los criterios de búsqueda especificados. Este método se introdujo en CAPICOM 2.0.

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

*FindType* \[ En\]
</dt> <dd>

Valor de la enumeración [**CAPICOM \_ CERTIFICATE \_ FIND \_ TYPE**](capicom-certificate-find-type.md) que especifica el tipo de criterios de coincidencia proporcionados en el *parámetro varCriteria.* En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                                        | Significado                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_FIND_SHA1_HASH"></span><span id="capicom_certificate_find_sha1_hash"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ FIND \_ SHA1 \_ HASH**</dt> </dl>                              | Devuelve certificados con un hash SHA1 que coincide con el hash SHA1 especificado en el *parámetro varCriteria.*<br/>                                                                                                                              |
| <span id="CAPICOM_CERTIFICATE_FIND_SUBJECT_NAME"></span><span id="capicom_certificate_find_subject_name"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ FIND \_ SUBJECT \_ NAME**</dt> </dl>                     | Devuelve certificados cuyo nombre de sujeto coincide exactamente o parcialmente con el nombre de sujeto especificado en el *parámetro varCriteria.* Esta llamada busca solo en el campo de nombre del sujeto.<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_FIND_ISSUER_NAME"></span><span id="capicom_certificate_find_issuer_name"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ FIND \_ ISSUER \_ NAME**</dt> </dl>                        | Devuelve certificados cuyo nombre de emisor coincide exactamente o parcialmente con el nombre del emisor especificado en el *parámetro varCriteria.* Esta llamada busca solo en el campo de nombre del emisor.<br/>                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_ROOT_NAME"></span><span id="capicom_certificate_find_root_name"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ FIND \_ ROOT \_ NAME**</dt> </dl>                              | Devuelve certificados cuyo nombre de sujeto raíz coincide exactamente o parcialmente con el nombre de sujeto raíz especificado en el *parámetro varCriteria.* Esta llamada crea una cadena. Esta llamada busca en el campo de nombre de sujeto del certificado raíz.<br/> |
| <span id="CAPICOM_CERTIFICATE_FIND_TEMPLATE_NAME"></span><span id="capicom_certificate_find_template_name"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ FIND \_ TEMPLATE \_ NAME**</dt> </dl>                  | Devuelve certificados cuyo nombre de plantilla coincide con el nombre de plantilla especificado en el *parámetro varCriteria.*<br/>                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENSION"></span><span id="capicom_certificate_find_extension"></span><dl> <dt>**EXTENSIÓN CAPICOM \_ CERTIFICATE \_ FIND \_**</dt> </dl>                               | Devuelve certificados que tienen una extensión que coincide con la extensión especificada en el *parámetro varCriteria.*<br/>                                                                                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENDED_PROPERTY"></span><span id="capicom_certificate_find_extended_property"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ FIND \_ EXTENDED \_ PROPERTY**</dt> </dl>      | Devuelve certificados en el almacén que contienen explícitamente una propiedad extendida con el valor especificado en el *parámetro varCriteria.*<br/>                                                                                                 |
| <span id="CAPICOM_CERTIFICATE_FIND_APPLICATION_POLICY"></span><span id="capicom_certificate_find_application_policy"></span><dl> <dt>**DIRECTIVA DE APLICACIÓN \_ CAPICOM CERTIFICATE \_ FIND \_ \_**</dt> </dl>   | Devuelve certificados del almacén que tienen una extensión de uso de clave mejorada, una extensión de directiva de aplicación o una propiedad extendida especificada en el *parámetro varCriteria.*<br/>                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_CERTIFICATE_POLICY"></span><span id="capicom_certificate_find_certificate_policy"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ FIND \_ CERTIFICATE \_ POLICY**</dt> </dl>   | Devuelve certificados que contienen el OID de directiva en la extensión de directiva de certificado especificada en el *parámetro varCriteria.*<br/>                                                                                                          |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_VALID"></span><span id="capicom_certificate_find_time_valid"></span><dl> <dt>**TIEMPO DE DE \_ IDENTIFICACIÓN DEL \_ CERTIFICADO \_ CAPICOM \_ VÁLIDO**</dt> </dl>                           | Devuelve certificados cuya hora es válida.<br/>                                                                                                                                                                                               |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_NOT_YET_VALID"></span><span id="capicom_certificate_find_time_not_yet_valid"></span><dl> <dt>**EL TIEMPO DE \_ DE IDENTIFICACIÓN DEL CERTIFICADO \_ \_ CAPICOM AÚN NO ES \_ \_ \_ VÁLIDO**</dt> </dl> | Devuelve certificados cuya hora aún no es válida.<br/>                                                                                                                                                                                       |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_EXPIRED"></span><span id="capicom_certificate_find_time_expired"></span><dl> <dt>**TIEMPO DE \_ DESCOMPOSICIÓN DEL CERTIFICADO CAPICOM \_ \_ \_ EXPIRADO**</dt> </dl>                     | Devuelve certificados cuyo tiempo ha expirado.<br/>                                                                                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_KEY_USAGE"></span><span id="capicom_certificate_find_key_usage"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ FIND \_ KEY \_ USAGE**</dt> </dl>                              | Devuelve certificados que contienen usos de claves en la extensión KeyUsage especificada en el *parámetro varCriteria.* Si la extensión KeyUsage no está presente, se supone que todos los usos de claves no están disponibles.<br/>                           |



 

</dd> <dt>

*varCriteria* \[ in, opcional\]
</dt> <dd>

Variante que contiene los criterios de búsqueda. Estos datos deben coincidir con el tipo de datos especificado en el *parámetro FindType.* Si el valor del parámetro *FindType* es CAPICOM \_ CERTIFICATE FIND TIME \_ \_ \_ VALID, CAPICOM CERTIFICATE FIND TIME NOT YET VALID o \_ \_ \_ \_ \_ \_ CAPICOM CERTIFICATE FIND TIME \_ EXPIRED \_ \_ \_ y no se pasa un valor a este parámetro, se supone que es la hora actual. Para obtener ejemplos de cada tipo de datos, vea Comentarios. El valor predeterminado es 0.

</dd> <dt>

*bFindValidOnly* \[ in, opcional\]
</dt> <dd>

Valor booleano que indica si solo se devuelven certificados válidos. El valor predeterminado es false; esto indica que se devuelven todos los certificados que coinciden con los criterios de búsqueda.

Si es true, la búsqueda no devolverá los siguientes tipos de certificados:

-   Certificados cuyo tiempo ha expirado o aún no es válido.
-   Los certificados no están encadenados correctamente.
-   Certificados que tienen problemas de firma.
-   Certificados que se revocan.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

[**Objeto Certificates**](certificates.md) que contiene los resultados de la búsqueda.

**CAPICOM 2.1:** El [**objeto Certificates**](certificates.md) que se devuelve contiene referencias a los certificados de la colección en la que se ha realizado la búsqueda. Los cambios realizados en los certificados en el **objeto Certificates** devuelto se reflejan en esa colección.

**CAPICOM 2.0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 y CAPICOM 2.0.0.3:** El [**objeto Certificates**](certificates.md) que se devuelve contiene copias de los certificados de la colección en la que se ha realizado la búsqueda. Los cambios realizados en los certificados en el **objeto Certificates** devuelto no se reflejan en esa colección.

## <a name="remarks"></a>Comentarios

En los ejemplos siguientes se muestran posibles criterios de búsqueda para los distintos tipos de criterios de búsqueda.



| *Parámetro FindType*                              | *parámetro varCriteria*                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| CAPICOM \_ CERTIFICATE \_ FIND \_ SHA1 \_ HASH            | 33F362434B577F844BB7226BE36F7D72EF9D9393                                                                                           |
| CAPICOM \_ CERTIFICATE \_ FIND \_ SUBJECT \_ NAME         | "NameOfPerson"                                                                                                                     |
| CAPICOM \_ CERTIFICATE \_ FIND \_ ISSUER \_ NAME          | "VeriSign"                                                                                                                         |
| CAPICOM \_ CERTIFICATE \_ FIND \_ ROOT \_ NAME            | "Microsoft Root Authority"                                                                                                         |
| CAPICOM \_ CERTIFICATE \_ FIND \_ TEMPLATE \_ NAME        | "AutoEnrollEFS"<br/> 1.3.6.1.4.1.311.21.8.3692315854.1256661383.1690418588.4201632533.1741915387.2177932052<br/>       |
| EXTENSIÓN CAPICOM \_ CERTIFICATE \_ FIND \_             | "2.5.29.31"<br/> EXTENSIÓN CAPICOM \_ OID \_ KEY \_ USAGE \_<br/> "Lista de distribución de CRL"<br/>                           |
| CAPICOM \_ CERTIFICATE \_ FIND \_ EXTENDED \_ PROPERTY    | CAPICOM \_ PROPID \_ KEY \_ PROV \_ INFO                                                                                                   |
| DIRECTIVA DE APLICACIÓN \_ CAPICOM CERTIFICATE \_ FIND \_ \_   | "1.3.6.1.5.5.7.3.3"<br/> "1.3.6.1.5.5.7.3.4"<br/> CAPICOM \_ OID \_ SERVER \_ AUTH \_ EKU<br/> "Firma de código"<br/> |
| CAPICOM \_ CERTIFICATE \_ FIND \_ CERTIFICATE \_ POLICY   | "1.3.6.1.5.5.7.3.4.3.5"<br/> "Corporate High Assurance"<br/>                                                           |
| TIEMPO DE DE \_ IDENTIFICACIÓN DEL \_ CERTIFICADO \_ CAPICOM \_ VÁLIDO           | \#15/04/2002, 6:00 p. m.\#                                                                                                            |
| EL TIEMPO DE \_ DE IDENTIFICACIÓN DEL CERTIFICADO \_ \_ CAPICOM AÚN NO ES \_ \_ \_ VÁLIDO | \#15/04/2002, 6:00 p. m.\#                                                                                                            |
| TIEMPO DE \_ DESCOMPOSICIÓN DEL CERTIFICADO CAPICOM \_ \_ \_ EXPIRADO         | \#15/04/2002, 6:00 p. m.\#                                                                                                            |
| CAPICOM \_ CERTIFICATE \_ FIND \_ KEY \_ USAGE            | USO DE CLAVE \_ CAPICOM ENCIPHER \_ ONLY \_ \_                                                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Certificados**](certificates.md)
</dt> <dt>

[**CAPICOM \_ OID**](capicom-oid.md)
</dt> </dl>

 

 
