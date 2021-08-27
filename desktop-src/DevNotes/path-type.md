---
description: Representa el tipo de ruta de acceso que se usa como argumento.
ms.assetid: f308c638-b383-432e-9dd3-edc33b792139
title: PATH_TYPE enumeración
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATH_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: c05e71e485eaaf3ff309dc3a0df3d792ccd18c1438964d387afe969adbfd3fc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058605"
---
# <a name="path_type-enumeration"></a>Path \_ TYPE (enumeración)

Representa el tipo de ruta de acceso que se usa como argumento.

## <a name="syntax"></a>Syntax


```C++
typedef enum _PATH_TYPE { 
  DOS_PATH,
  NT_PATH
} PATH_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DOS_PATH"></span><span id="dos_path"></span>**RUTA DE \_ ACCESO DE DOS**
</dt> <dd>

Ruta de acceso estándar.

</dd> <dt>

<span id="NT_PATH"></span><span id="nt_path"></span>**NT \_ PATH**
</dt> <dd>

Ruta de acceso interna.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbCreateDatabase**](sdbcreatedatabase.md)
</dt> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




