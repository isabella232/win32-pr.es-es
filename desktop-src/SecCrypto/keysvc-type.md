---
description: La \_ enumeración de tipo KEYSVC define si una clave se aplica a un equipo o a un servicio.
ms.assetid: 573a412a-1e9d-47ac-bd09-2319d4b9712b
title: Enumeración KEYSVC_TYPE (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_TYPE
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 71d6724f7bae78a3c1ac4da83289c151b7ec1a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003118"
---
# <a name="keysvc_type-enumeration"></a>\_Enumeración de tipo KEYSVC

La enumeración de **\_ tipo KEYSVC** define si una clave se aplica a un equipo o a un servicio.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _KEYSVC_TYPE { 
  KeySvcMachine,
  KeySvcService
} KEYSVC_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**KeySvcMachine**
</dt> <dd>

La clave es para un equipo.

</dd> <dt>

<span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**KeySvcService**
</dt> <dd>

La clave es para un servicio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> </dl>

 

 




