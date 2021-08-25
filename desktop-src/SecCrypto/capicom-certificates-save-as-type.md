---
description: Define el formato de un archivo que contiene información de certificados.
ms.assetid: 2118746a-9fa4-4e6a-82ce-e57f154f4a94
title: CAPICOM_CERTIFICATES_SAVE_AS_TYPE enumeración (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATES_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 70185a7a48b7dc195727991fb0dcc35f4909451fa0e4da5f4100e8385adebc2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879375"
---
# <a name="capicom_certificates_save_as_type-enumeration"></a>CAPICOM \_ CERTIFICATES \_ SAVE AS TYPE \_ \_ (Enumeración)

El **tipo de enumeración CAPICOM \_ CERTIFICATES SAVE AS \_ \_ \_ TYPE** define el formato de un archivo que contiene información de certificados. CAPICOM 2.0 introdujo este tipo de enumeración.

## <a name="members"></a>Miembros



| Miembro                                          | Descripción                                          | Value |
|-------------------------------------------------|------------------------------------------------------|-------|
| **LOS CERTIFICADOS \_ CAPICOM \_ SE \_ GUARDARÁN COMO \_ SERIALIZADOS** | Los certificados guardados se serializan.<br/>    | 0     |
| **LOS CERTIFICADOS CAPICOM \_ \_ SE GUARDA COMO \_ \_ PKCS7**      | Los certificados se guardan como PKCS \# 7.<br/> | 1     |
| **CERTIFICADOS CAPICOM \_ \_ GUARDADOS \_ COMO \_ PFX**        | Los certificados se guardan como PFX.<br/>      | 2     |



## <a name="remarks"></a>Comentarios

El método \_ \_ \_ \_ [**Certificates.Save**](certificates-save.md) usa el tipo de enumeración CAPICOM CERTIFICATES SAVE AS TYPE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




