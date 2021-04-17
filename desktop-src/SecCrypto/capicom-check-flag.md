---
description: Define las condiciones para las que se va a comprobar una cadena de certificados.
ms.assetid: 87df623c-5661-4325-8dd6-393ce2e44066
title: Enumeración CAPICOM_CHECK_FLAG (CAPICOM. h)
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
ms.openlocfilehash: 47b6168fb87ebbb65b07eadfe9adaf488934e252
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670449"
---
# <a name="capicom_check_flag-enumeration"></a>\_Enumeración de marca de comprobación de CAPICOM \_

El tipo de enumeración de la **\_ \_ marca de comprobación de CAPICOM** define las condiciones para las que se va a comprobar una cadena de certificados.

## <a name="members"></a>Miembros



| Miembro                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Value      |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ comprobar \_ ninguno**                        | No se realiza ninguna comprobación de la validez.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0x00000000 |
| **CAPICOM \_ comprobar \_ raíz de confianza \_**               | Comprueba si existe una raíz de confianza de la cadena de certificados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 0x00000001 |
| **\_validez de \_ tiempo de comprobación de CAPICOM \_**              | Comprueba la validez de tiempo de todos los certificados de la cadena.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | 0x00000002 |
| **comprobación de la validez de la firma de CAPICOM \_ \_ \_**         | Comprueba las firmas válidas en todos los certificados de la cadena.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0x00000004 |
| **CAPICOM \_ comprobar \_ el \_ Estado de revocación en línea \_**  | Comprueba el estado de revocación de todos los certificados de la cadena mediante listas de revocación de certificados (CRL) disponibles en línea. Las CRL se descargan mediante la extensión de punto de distribución de CRL (CDP) del certificado. <br/> Si la CRL se ha descargado y no ha expirado, CAPICOM lo usa y no se conecta. Si una CRL no se ha descargado o no está actualizada, CAPICOM se conecta para intentar descargar la CRL.<br/> Esta marca se omite si \_ se especifica también CAPICOM comprobar el \_ \_ Estado de revocación sin conexión \_ .<br/> | 0x00000008 |
| **CAPICOM \_ comprobar \_ el \_ Estado de revocación sin conexión \_** | Comprueba el estado de revocación de todos los certificados de la cadena usando solo las CRL sin conexión. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              | 0x00000010 |
| **\_ \_ cadena completa de comprobación de CAPICOM \_**             | Comprueba la cadena completa. Introducido en CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | 0x00000020 |
| **CAPICOM \_ comprobar \_ restricciones de nombres \_**           | Comprueba las restricciones de nombre. Introducido en CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 0x00000040 |
| **CAPICOM \_ comprobar \_ \_ Restricciones básicas**          | Comprueba las restricciones básicas. Introducido en CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | 0x00000080 |
| **CAPICOM \_ comprobar el \_ período de \_ validez anidado \_**    | Comprueba la validez anidada. Introducido en CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | 0x00000100 |
| **CAPICOM \_ comprobar \_ todo en línea \_**                 | Comprueba todas las condiciones excepto CAPICOM \_ Compruebe el \_ Estado de \_ revocación sin conexión \_ . Las comprobaciones de revocación se realizan en todos los certificados de la cadena excepto en el certificado raíz. Introducido en CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                               | 0x000001EF |
| **CAPICOM \_ comprobar \_ todo sin conexión \_**                | Comprueba todas las condiciones excepto CAPICOM \_ comprueba el \_ Estado de \_ revocación en línea \_ . Las comprobaciones de revocación se realizan en todos los certificados de la cadena excepto en el certificado raíz. Introducido en CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                | 0x000001F7 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




