---
description: Define los nombres de uso de clave extendidos en función de dónde se pueden usar.
ms.assetid: 78f9f9cb-46e7-4f81-a16e-503750a0d743
title: Enumeración CAPICOM_EKU (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EKU
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: e1d2f4f435fa31df00b87e20254aad57b690b047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670852"
---
# <a name="capicom_eku-enumeration"></a>\_Enumeración de EKU de CAPICOM

El tipo de enumeración **\_ EKU de CAPICOM** define los nombres de uso de clave extendidos en función de dónde se pueden usar.

## <a name="members"></a>Miembros



| Miembro                                     | Descripción                                                                                                                                                 | Value |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **EKU de CAPICOM \_ \_ otro**                    | El certificado tiene usos definidos en la directiva local. Se usa si el EKU necesario no está predefinido y la aplicación debe establecer el valor de OID.<br/> | 0     |
| **\_autenticación del \_ servidor \_ EKU de CAPICOM**             | El certificado se puede usar para autenticar un servidor.<br/>                                                                                                | 1     |
| **\_autenticación de \_ cliente de EKU de CAPICOM \_**             | El certificado se puede utilizar para autenticar a un cliente.<br/>                                                                                                | 2     |
| **\_firma de \_ código \_ EKU de CAPICOM**            | El certificado se puede utilizar para crear una firma digital.<br/>                                                                                           | 3     |
| **\_protección de \_ correo electrónico de EKU de CAPICOM \_**        | El certificado se puede usar para la protección de correo electrónico.<br/>                                                                                                    | 4     |
| **\_Inicio de \_ sesión con tarjeta inteligente EKU de CAPICOM \_**         | El certificado se puede usar para el inicio de sesión con tarjeta inteligente. Introducido en CAPICOM 2,0.<br/>                                                                         | 5     |
| **\_sistema de \_ cifrado de \_ archivos \_ EKU de CAPICOM** | El certificado se puede usar para EFS. Introducido en CAPICOM 2,0.<br/>                                                                                      | 6     |



## <a name="remarks"></a>Observaciones

El EKU usa el tipo de enumeración **\_ EKU de CAPICOM** [**. Propiedad nombre**](eku-name.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




