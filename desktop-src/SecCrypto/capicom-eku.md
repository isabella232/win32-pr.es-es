---
description: Define los nombres de uso de clave extendidos en función de dónde se pueden usar.
ms.assetid: 78f9f9cb-46e7-4f81-a16e-503750a0d743
title: CAPICOM_EKU enumeración (Capicom.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171182"
---
# <a name="capicom_eku-enumeration"></a>CAPICOM \_ EKU (enumeración)

El **tipo de enumeración \_ CAPICOM EKU** define los nombres de uso de clave extendidos en función de dónde se pueden usar.

## <a name="members"></a>Members



| Miembro                                     | Descripción                                                                                                                                                 | Value |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ EKU \_ OTHER**                    | El certificado tiene usos definidos en la directiva local. Se usa si el EKU necesario no está predefinido y la aplicación debe establecer el valor de OID.<br/> | 0     |
| **CAPICOM \_ EKU \_ SERVER \_ AUTH**             | El certificado se puede usar para autenticar un servidor.<br/>                                                                                                | 1     |
| **CAPICOM \_ EKU \_ CLIENT \_ AUTH**             | El certificado se puede usar para autenticar un cliente.<br/>                                                                                                | 2     |
| **FIRMA DE CÓDIGO \_ CAPICOM EKU \_ \_**            | El certificado se puede usar para crear una firma digital.<br/>                                                                                           | 3     |
| **CAPICOM \_ EKU \_ EMAIL \_ PROTECTION**        | El certificado se puede usar para la protección de correo electrónico.<br/>                                                                                                    | 4     |
| **INICIO DE SESIÓN \_ DE TARJETA INTELIGENTE CAPICOM EKU \_ \_**         | El certificado se puede usar para el inicio de sesión con tarjeta inteligente. Introducido en CAPICOM 2.0.<br/>                                                                         | 5     |
| **CAPICOM \_ EKU \_ ENCRYPTING \_ FILE \_ SYSTEM** | El certificado se puede usar para EFS. Introducido en CAPICOM 2.0.<br/>                                                                                      | 6     |



## <a name="remarks"></a>Observaciones

El EKU usa el tipo de enumeración **\_ CAPICOM EKU.** [**Propiedad**](eku-name.md) Name.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




