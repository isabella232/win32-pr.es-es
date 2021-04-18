---
description: Se utiliza con el método Store. Open para indicar cómo se va a abrir un almacén de certificados.
ms.assetid: 6ec87b8c-9431-4ecc-bd90-943cfe2df1c2
title: Enumeración CAPICOM_STORE_OPEN_MODE (CAPICOM. h)
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
ms.openlocfilehash: 61fe8be0bdf75db5204066563ca07f8225678f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650006"
---
# <a name="capicom_store_open_mode-enumeration"></a>\_ \_ Enumeración de modo de apertura de la tienda CAPICOM \_

El \_ tipo de \_ enumeración de modo abierto de CAPICOM \_ se utiliza con el método [**Store. Open**](store-open.md) para indicar cómo se va a abrir un almacén de certificados.

## <a name="members"></a>Miembros



| Miembro                                      | Descripción                                                                                                                                                              | Value |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ Store \_ Open \_ Read \_ Only**        | Abra el almacén en modo de solo lectura.<br/>                                                                                                                             | 0     |
| **CAPICOM \_ Store \_ Open \_ Read \_ Write**       | Abra el almacén en modo de lectura y escritura.<br/>                                                                                                                            | 1     |
| **\_ \_ \_ máximo permitido del almacén \_ de CAPICOM**  | Abra el almacén en modo de lectura y escritura si el usuario tiene permisos de lectura y escritura. Si el usuario no tiene permisos de lectura/escritura, abra el almacén en modo de solo lectura.<br/> | 2     |
| **CAPICOM \_ Store \_ Open \_ exist \_ Only**    | Abrir solo los almacenes existentes; no cree un nuevo almacén. Introducido por CAPICOM 2,0.<br/>                                                                              | 128   |
| **\_ \_ archivos abiertos de \_ la tienda de CAPICOM \_** | Incluir certificados archivados al usar el almacén. Introducido por CAPICOM 2,0.<br/>                                                                                | 256   |



## <a name="remarks"></a>Observaciones

Al utilizar la \_ \_ enumeración de modo abierto de la tienda CAPICOM \_ , solo se puede usar una de las siguientes opciones.

-   CAPICOM \_ Store \_ Open \_ Read \_ Only
-   CAPICOM \_ Store \_ Open \_ Read \_ Write
-   \_ \_ \_ máximo permitido del almacén \_ de CAPICOM

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Store. Open**](store-open.md)
</dt> </dl>

 

 




