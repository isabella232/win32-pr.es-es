---
title: CB_RESOURCE_TYPE enumeración (Cbclient.h)
description: Especifica el tipo de recurso al que se conecta la conexión entrante.
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
ms.openlocfilehash: 63dfce0f575147233735dd943645eb51c26141cacaaa61c044698b29b8d118e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139118"
---
# <a name="cb_resource_type-enumeration"></a>Enumeración \_ CB RESOURCE \_ TYPE

Especifica el tipo de recurso al que se conecta la conexión entrante. Esta enumeración se usa con la [**estructura CB \_ CONNECTION \_ INFO.**](cb-connection-info.md)

## <a name="syntax"></a>Syntax


```C++
typedef enum _CB_RESOURCE_TYPE { 
  CB_RESOURCE_UNDEFINED  = 0,
  CB_RESOURCE_SESSION    = 1,
  CB_RESOURCE_VM
} CB_RESOURCE_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**RECURSO \_ CB \_ SIN DEFINIR**
</dt> <dd>

El tipo de recurso no está definido.

</dd> <dt>

<span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**SESIÓN \_ DE RECURSOS \_ CB**
</dt> <dd>

El recurso es una sesión remota.

</dd> <dt>

<span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**MÁQUINA \_ VIRTUAL DE RECURSOS DE \_ CB**
</dt> <dd>

El recurso es una máquina virtual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cbclient.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INFORMACIÓN \_ DE CONEXIÓN \_ CB**](cb-connection-info.md)
</dt> </dl>

 

 





