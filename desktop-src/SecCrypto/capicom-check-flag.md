---
description: Define las condiciones para las que se va a comprobar una cadena de certificados.
ms.assetid: 87df623c-5661-4325-8dd6-393ce2e44066
title: CAPICOM_CHECK_FLAG enumeración (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CHECK_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 4b9fbc5ec1717acbd32c70ea3467465daf47de5d41af794a5164f44174a602d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772517"
---
# <a name="capicom_check_flag-enumeration"></a>CAPICOM \_ CHECK \_ FLAG (enumeración)

El **tipo de \_ enumeración CAPICOM CHECK \_ FLAG** define las condiciones para las que se va a comprobar una cadena de certificados.

## <a name="members"></a>Miembros



| Miembro                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Valor      |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ CHECK \_ NONE**                        | No se realiza ninguna comprobación de validez.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0x00000000 |
| **CAPICOM \_ CHECK \_ TRUSTED \_ ROOT**               | Comprueba si hay una raíz de confianza de la cadena de certificados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 0x00000001 |
| **VALIDEZ DE LA \_ HORA \_ DE COMPROBACIÓN \_ DE CAPICOM**              | Comprueba la validez de tiempo de todos los certificados de la cadena.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | 0x00000002 |
| **VALIDEZ DE LA \_ FIRMA DE COMPROBACIÓN \_ \_ DE CAPICOM**         | Comprueba si hay firmas válidas en todos los certificados de la cadena.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0x00000004 |
| **CAPICOM \_ CHECK \_ ONLINE \_ REVOCATION \_ STATUS**  | Comprueba el estado de revocación de todos los certificados de la cadena mediante listas de revocación de certificados (CRL) disponibles en línea. Las CRL se descargan mediante la extensión de punto de distribución crl (CDP) en el certificado. <br/> Si la CRL se ha descargado y no ha expirado, CAPICOM la usa y no se encuentra en línea. Si no se ha descargado una CRL o no está actualizada, CAPICOM se queda en línea para intentar descargar la CRL.<br/> Esta marca se omite si también se especifica CAPICOM \_ CHECK \_ OFFLINE \_ REVOCATION \_ STATUS.<br/> | 0x00000008 |
| **CAPICOM \_ CHECK \_ OFFLINE \_ REVOCATION \_ STATUS** | Comprueba el estado de revocación de todos los certificados de la cadena usando solo las CRL sin conexión. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              | 0x00000010 |
| **CAPICOM \_ CHECK \_ COMPLETE \_ CHAIN**             | Comprueba la cadena completa. Introducido en CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | 0x00000020 |
| **RESTRICCIONES \_ DE NOMBRE CHECK \_ DE CAPICOM \_**           | Comprueba las restricciones de nombre. Introducido en CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 0x00000040 |
| **RESTRICCIONES \_ \_ BÁSICAS DE CAPICOM CHECK \_**          | Comprueba las restricciones básicas. Introducido en CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | 0x00000080 |
| **CAPICOM \_ CHECK \_ NESTED \_ VALIDITY \_ PERIOD**    | Comprueba la validez anidada. Introducido en CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | 0x00000100 |
| **CAPICOM \_ CHECK \_ ONLINE \_ ALL**                 | Comprueba todas las condiciones excepto CAPICOM \_ CHECK \_ OFFLINE \_ REVOCATION \_ STATUS. Las comprobaciones de revocación se realizan en todos los certificados de la cadena, excepto en el certificado raíz. Introducido en CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                               | 0x000001EF |
| **CAPICOM \_ CHECK \_ OFFLINE \_ ALL**                | Comprueba todas las condiciones excepto CAPICOM \_ CHECK \_ ONLINE \_ REVOCATION \_ STATUS. Las comprobaciones de revocación se realizan en todos los certificados de la cadena, excepto en el certificado raíz. Introducido en CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                | 0x000001F7 |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




