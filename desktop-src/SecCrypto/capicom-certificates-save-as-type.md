---
description: Define el formato de un archivo que contiene información de certificados.
ms.assetid: 2118746a-9fa4-4e6a-82ce-e57f154f4a94
title: Enumeración CAPICOM_CERTIFICATES_SAVE_AS_TYPE (CAPICOM. h)
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
ms.openlocfilehash: 3cbde0e8a64fa931ce50d2277d33b5fd5c27ee68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670854"
---
# <a name="capicom_certificates_save_as_type-enumeration"></a>La \_ \_ enumeración de los certificados de CAPICOM se guardan \_ como \_ tipo

El tipo de enumeración de los **certificados de CAPICOM \_ \_ Save \_ as \_** define el formato de un archivo que contiene información de certificados. CAPICOM 2,0 presentó este tipo de enumeración.

## <a name="members"></a>Miembros



| Miembro                                          | Descripción                                          | Value |
|-------------------------------------------------|------------------------------------------------------|-------|
| **los \_ certificados \_ de CAPICOM se guardan \_ como \_ serializados** | Los certificados guardados se serializan.<br/>    | 0     |
| **Los \_ certificados \_ de CAPICOM se guardan \_ como \_ pkcs7**      | Los certificados se guardan como PKCS \# 7.<br/> | 1     |
| **los \_ certificados \_ de CAPICOM se guardan \_ como \_ pfx**        | Los certificados se guardan como un archivo PFX.<br/>      | 2     |



## <a name="remarks"></a>Observaciones

El método de los certificados \_ \_ \_ \_ [**. Save**](certificates-save.md) usa el tipo de enumeración de tipo guardar certificados de CAPICOM.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




