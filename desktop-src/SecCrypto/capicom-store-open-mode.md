---
description: Se usa con el método Store.Open para indicar cómo se va a abrir un almacén de certificados.
ms.assetid: 6ec87b8c-9431-4ecc-bd90-943cfe2df1c2
title: CAPICOM_STORE_OPEN_MODE enumeración (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_OPEN_MODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: ebd46b751f4a098361618f3b6e992e4333425f501bf6afdedfca047e921ad7ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772062"
---
# <a name="capicom_store_open_mode-enumeration"></a>CAPICOM \_ STORE OPEN MODE \_ \_ (enumeración)

El tipo de enumeración CAPICOM STORE OPEN MODE se usa con el método \_ \_ \_ [**Store.Open**](store-open.md) para indicar cómo se va a abrir un almacén de certificados.

## <a name="members"></a>Miembros



| Miembro                                      | Descripción                                                                                                                                                              | Value |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ STORE \_ OPEN \_ READ \_ ONLY**        | Abra el almacén en modo de solo lectura.<br/>                                                                                                                             | 0     |
| **CAPICOM \_ STORE \_ OPEN \_ READ \_ WRITE**       | Abra el almacén en modo de lectura y escritura.<br/>                                                                                                                            | 1     |
| **CAPICOM \_ STORE \_ OPEN \_ MAXIMUM \_ ALLOWED**  | Abra el almacén en modo de lectura y escritura si el usuario tiene permisos de lectura y escritura. Si el usuario no tiene permisos de lectura y escritura, abra el almacén en modo de solo lectura.<br/> | 2     |
| **CAPICOM \_ STORE \_ OPEN \_ EXISTING \_ ONLY**    | Abra solo los almacenes existentes; no cree un nuevo almacén. Introducido por CAPICOM 2.0.<br/>                                                                              | 128   |
| **CAPICOM \_ STORE \_ OPEN \_ INCLUDE \_ ARCHIVED** | Incluya certificados archivados al usar el almacén. Introducido por CAPICOM 2.0.<br/>                                                                                | 256   |



## <a name="remarks"></a>Comentarios

Cuando se usa la enumeración CAPICOM STORE OPEN MODE, solo se puede usar una de las \_ \_ opciones \_ siguientes.

-   CAPICOM \_ STORE \_ OPEN \_ READ \_ ONLY
-   CAPICOM \_ STORE \_ OPEN \_ READ \_ WRITE
-   CAPICOM \_ STORE \_ OPEN \_ MAXIMUM \_ ALLOWED

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Store.Open**](store-open.md)
</dt> </dl>

 

 




