---
description: Representa el tipo de ruta de acceso que se usa como argumento.
ms.assetid: f308c638-b383-432e-9dd3-edc33b792139
title: Enumeración PATH_TYPE
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
ms.openlocfilehash: 1e5602aa7384c8de6c33b407e9a536141d8d002b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538367"
---
# <a name="path_type-enumeration"></a>Enumeración de tipo de ruta de acceso \_

Representa el tipo de ruta de acceso que se usa como argumento.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _PATH_TYPE { 
  DOS_PATH,
  NT_PATH
} PATH_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DOS_PATH"></span><span id="dos_path"></span>**Ruta de acceso de DOS \_**
</dt> <dd>

Ruta de acceso estándar.

</dd> <dt>

<span id="NT_PATH"></span><span id="nt_path"></span>**\_ruta de acceso NT**
</dt> <dd>

Ruta de acceso interna.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbCreateDatabase**](sdbcreatedatabase.md)
</dt> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




