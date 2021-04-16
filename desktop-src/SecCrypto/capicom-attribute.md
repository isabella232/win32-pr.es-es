---
description: Define el tipo de atributo asociado a una firma.
ms.assetid: 94f0dce4-0b32-4c39-ab2e-b01795432acd
title: Enumeración CAPICOM_ATTRIBUTE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ATTRIBUTE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: b03f91d0737b29b98adeb7e6a56bf9eccd35cc8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671471"
---
# <a name="capicom_attribute-enumeration"></a>CAPICOM \_ (enumeración de atributos)

El tipo de enumeración del **\_ atributo CAPICOM** define el tipo de atributo asociado a una [*firma*](../secgloss/d-gly.md).

## <a name="members"></a>Miembros



| Miembro                                                       | Descripción                                                                | Value |
|--------------------------------------------------------------|----------------------------------------------------------------------------|-------|
| **\_tiempo de firma de atributo autenticado de CAPICOM \_ \_ \_**         | El atributo contiene la hora a la que se creó la firma.<br/> | 0     |
| **\_nombre de documento de atributo autenticado de CAPICOM \_ \_ \_**        | El atributo contiene el nombre del documento firmado.<br/>         | 1     |
| **\_Descripción del documento de atributo autenticado de CAPICOM \_ \_ \_** | El atributo contiene una descripción del documento firmado.<br/>    | 2     |



## <a name="remarks"></a>Observaciones

La propiedad [**Attribute.Name**](attribute-name.md) usa el tipo de enumeración del **\_ atributo CAPICOM** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
