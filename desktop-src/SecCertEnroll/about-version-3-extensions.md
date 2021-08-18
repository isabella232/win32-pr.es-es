---
description: Un certificado X.509 versión 3 contiene los campos definidos en la versión 1 y la versión 2, y además agrega extensiones de certificado. La sintaxis ASN.1 de las extensiones de certificado se muestra en el ejemplo siguiente.
ms.assetid: ca8df7a4-caa4-4fe7-81a8-8fce372454f4
title: Extensiones de la versión 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c96bc15ca4089499f5573fc83d2a33445377d2b7947d70900019f0629acaf1f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903232"
---
# <a name="version-3-extensions"></a>Extensiones de la versión 3

Un certificado X.509 versión 3 contiene los campos definidos en la versión 1 y la versión 2, y además agrega extensiones de certificado. La sintaxis ASN.1 de las extensiones de certificado se muestra en el ejemplo siguiente.

``` syntax
---------------------------------------------------------------------
-- Extensions (beginning with version 3).
---------------------------------------------------------------------
Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
  Id                  OBJECT IDENTIFIER,
  critical            BOOLEAN DEFAULT FALSE,
  extnValue           OCTET STRING
}
```

Las extensiones de la versión estándar 3 y sus identificadores de objeto (ID) se muestran en la tabla siguiente. Microsoft los admite e incluye extensiones personalizadas adicionales. Para obtener más información, vea [Extensiones](extensions.md).

| Extensión                                         | Descripción                                                                                                                                                                                              |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de clave de autoridad(2.5.29.19)<br/>    | Identifica la clave pública de la entidad de certificación (CA) correspondiente a la clave privada de CA utilizada para firmar el certificado.                                                                              |
| Restricciones básicas(2.5.29.35)<br/>           | Especifica si la entidad se puede utilizar como una CA y, en caso afirmativo, el número de CA subordinadas que pueden existir por debajo en la cadena de certificados.                                                           |
| Directivas de certificado(2.5.29.32)<br/>        | Especifica las directivas con las que se ha emitido el certificado y los fines para los que se puede utilizar.                                                                                            |
| Puntos de distribución CRL(2.5.29.31)<br/>     | Contiene el URI de la lista base [*de revocación de certificados*](/windows/desktop/SecGloss/c-gly) (CRL).                                  |
| Uso mejorado de clave (2.5.29.46)<br/>          | Especifica la manera en que se puede utilizar la clave pública contenida en el certificado.                                                                                                                   |
| Nombre alternativo del emisor(2.5.29.8)<br/>      | Especifica una o más formas de nombre alternativas para el emisor de la solicitud de certificado.                                                                                                                  |
| Uso de claves(2.5.29.15)<br/>                   | Especifica restricciones en las operaciones que puede realizar la clave pública contenida en el certificado.                                                                                           |
| Restricciones de nombre(2.5.29.30)<br/>            | Especifica el espacio de nombres en el que deben encontrarse todos los nombres de firmantes en una jerarquía de certificados. La extensión solo se utiliza en un certificado de CA.                                                       |
| Restricciones de directiva(2.5.29.36)<br/>          | Restringen la validación de rutas prohibiendo la asignación de directivas o exigiendo que cada certificado de la jerarquía contenga un identificador de directiva aceptable. La extensión solo se utiliza en un certificado de CA. |
| Asignaciones de directivas(2.5.29.33)<br/>             | Especifica las directivas de una CA subordinada correspondientes a directivas de la CA emisora.                                                                                                                |
| Período de uso de clave privada(2.5.29.16)<br/>    | Especifica un período de validez distinto para la clave privada que para el certificado con el que la clave privada está asociada.                                                                             |
| Nombre alternativo del sujeto(2.5.29.17)<br/>    | Especifica una o más formas de nombre alternativas para el firmante de la solicitud de certificado. Algunos ejemplos de formas alternativas son direcciones de correo electrónico, nombres DNS, direcciones IP y URI.                           |
| Atributos de directorio del sujeto(2.5.29.9)<br/> | Contiene atributos de identificación, como la nacionalidad del firmante del certificado. El valor de extensión es una secuencia de pares de valores OID.                                                              |
| Identificador de clave de sujeto(2.5.29.14)<br/>      | Diferencia entre varias claves públicas de las que el firmante del certificado es titular. El valor de extensión suele ser un hash SHA-1 de la clave.                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Campos básicos](about-basic-fields.md)
</dt> <dt>

[Campos de la versión 2](about-version-2-fields.md)
</dt> <dt>

[Certificados de clave pública X.509](about-x-509-public-key-certificates.md)
</dt> </dl>

 

