---
title: Enumeración CB_RESOURCE_TYPE (Cbclient. h)
description: Especifica el tipo de recurso al que se está conectando la conexión entrante.
ms.assetid: 80D921BF-2D84-4A18-9544-50087B81F177
ms.tgt_platform: multiple
keywords:
- CB_RESOURCE_TYPE enumeración Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- CB_RESOURCE_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60561e4af54c6d27288d8df311693d51c0b9fc77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801586"
---
# <a name="cb_resource_type-enumeration"></a>\_Enumeración de tipos de recursos CB \_

Especifica el tipo de recurso al que se está conectando la conexión entrante. Esta enumeración se usa con la estructura de [**\_ \_ información de conexión CB**](cb-connection-info.md) .

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _CB_RESOURCE_TYPE { 
  CB_RESOURCE_UNDEFINED  = 0,
  CB_RESOURCE_SESSION    = 1,
  CB_RESOURCE_VM
} CB_RESOURCE_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**recurso CB no \_ \_ definido**
</dt> <dd>

El tipo de recurso no está definido.

</dd> <dt>

<span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**\_sesión de recursos CB \_**
</dt> <dd>

El recurso es una sesión remota.

</dd> <dt>

<span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**\_máquina virtual de recursos CB \_**
</dt> <dd>

El recurso es una máquina virtual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_información de conexión de CB \_**](cb-connection-info.md)
</dt> </dl>

 

 





