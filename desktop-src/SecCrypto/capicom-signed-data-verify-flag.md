---
description: Indica qué se comprueba cuando se comprueba una firma digital.
ms.assetid: e6259c3f-caed-42f4-832c-250365caa0d7
title: Enumeración CAPICOM_SIGNED_DATA_VERIFY_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_SIGNED_DATA_VERIFY_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bc8db48ee067e8d12bffa9dbff433384058013b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671366"
---
# <a name="capicom_signed_data_verify_flag-enumeration"></a>\_ \_ \_ Enumeración de marca de comprobación de datos FIRMAdos de CAPICOM \_

La enumeración de **\_ marcas de \_ \_ verificación \_ de datos firmados de CAPICOM** indica lo que se comprueba cuando se comprueba una [*firma digital*](../secgloss/d-gly.md) .

## <a name="members"></a>Miembros



| Miembro                                           | Descripción                                                                                                 | Value |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ comprobar \_ solo la firma \_**             | Solo se comprueba la firma.<br/>                                                                   | 0     |
| **CAPICOM \_ comprobar la \_ firma \_ y el \_ certificado** | Se comprueban tanto la firma como la validez del certificado utilizado para crear la firma.<br/> | 1     |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
