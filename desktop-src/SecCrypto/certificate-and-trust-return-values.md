---
description: Enumera los valores devueltos de certificados y certificados de confianza. Estos valores están incluidos en el archivo de encabezado Winerror.h.
ms.assetid: f7d1bdcb-8e4f-493f-ad3c-9d4b9d21436b
title: Valores devueltos de certificados y confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e17f170c7c3aa1ac0839323b9a52767a101dd3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476508"
---
# <a name="certificate-and-trust-return-values"></a>Valores devueltos de certificados y confianza

En la tabla siguiente se enumeran los valores devueltos de certificados y certificados de confianza. Estos valores están incluidos en el archivo de encabezado Winerror.h.



| Nombre                            | Descripción                                                                                                                    | Value      |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------|------------|
| CERT \_ E \_ CRITICAL               | Un certificado contiene una extensión desconocida que está marcada como "crítica".                                                         | 0x800B0105 |
| CERT \_ E NOMBRE NO \_ \_ VÁLIDO          | El certificado tiene un nombre que no es válido. El nombre no está incluido en la lista permitida o está explícitamente excluido. | 0x800B0114 |
| DIRECTIVA \_ NO VÁLIDA DE CERT E \_ \_        | El certificado tiene una directiva que no es válida.                                                                                | 0x800B0113 |
| \_ISSUERCHAINING DE CERT E \_         | De hecho, un elemento primario de un certificado determinado no emitía ese certificado secundario.                                                  | 0x800B0107 |
| CERTIFICADO \_ E CON FORMATO \_ DESAFORMADO              | Falta un certificado o tiene un valor vacío para un campo importante, como un asunto o un nombre de emisor.                       | 0x800B0108 |
| CERT \_ E \_ PATHLENCONST           | Se ha infringido una restricción de longitud de ruta de acceso en la cadena de la certificación.                                                         | 0x800B0104 |
| CERT \_ E \_ UNTRUSTEDCA            | Una cadena de certificación se procesó correctamente, pero el proveedor de directivas no confía en uno de los certificados de entidad de certificación.               | 0x800B0112 |
| CRYPT \_ E \_ NO \_ REVOCATION \_ CHECK | La función de revocación no pudo comprobar la revocación del certificado.                                                    | 0x80092012 |
| TRUST \_ E \_ BAD \_ DIGEST           | No se ha comprobado la firma digital del objeto.                                                                            | 0x80096010 |
| RESTRICCIONES \_ TRUST E \_ \_ BASIC    | No se ha observado la extensión de la restricción básica de un certificado.                                                         | 0x80096019 |
| TRUST \_ E \_ CERT \_ SIGNATURE       | No se puede comprobar la firma del certificado.                                                                           | 0x80096004 |
| TRUST \_ E \_ COUNTER \_ SIGNER       | Una de las firmas de contador no era válida.                                                                                   | 0x80096003 |
| CONFIANZA \_ E \_ \_ DESCONFIANZA EXPLÍCITA    | El usuario ha marcado explícitamente el certificado como que no es de confianza.                                                                | 0x800B0111 |
| CRITERIOS \_ FINANCIEROS DE CONFIANZA E \_ \_   | El certificado no cumple ni contiene las extensiones financieras authenticode.                                                | 0x8009601E |
| TRUST \_ E \_ NO \_ SIGNER \_ CERT      | El certificado para el firmante del mensaje no es válido o no se encuentra.                                                       | 0x80096002 |
| ERROR \_ DEL SISTEMA TRUST E \_ \_         | Se ha producido un error del nivel de sistema al comprobar la confianza.                                                                           | 0x80096001 |
| TRUST \_ E \_ TIME \_ STAMP           | La firma o el certificado de la marca de tiempo no se ha podido comprobar o es incorrecta.                                                 | 0x80096005 |



 

 

 



