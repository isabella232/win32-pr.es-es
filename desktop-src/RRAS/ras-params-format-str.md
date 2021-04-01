---
title: Enumeración RAS_PARAMS_FORMAT (rassapi. h)
description: El \_ \_ tipo de enumeración de formato de los parámetros de Ras se usa en la estructura de parámetros de Ras \_ para indicar el tipo de datos asociado a una clave específica del medio.
ms.assetid: dd2c0110-1f27-4a8f-bc61-f15588ebc4ca
keywords:
- RAS_PARAMS_FORMAT enumeración de RAS
topic_type:
- apiref
api_name:
- RAS_PARAMS_FORMAT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00065f3781fd2ada420f67367e84e0863fe3b446
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150523"
---
# <a name="ras_params_format-enumeration"></a>\_Enumeración de formato de parámetros ras \_

\[La enumeración de **\_ \_ formato** de los parámetros de Ras no es compatible con Windows Vista.\]

El tipo de enumeración de **\_ \_ formato** de los parámetros de Ras se usa en la estructura de [**\_ parámetros de Ras**](ras-parameters-str.md) para indicar el tipo de datos asociado a una clave específica del medio.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum RAS_PARAMS_FORMAT { 
  ParamNumber  = 0,
  ParamString  = 1
} RAS_PARAMS_FORMAT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**ParamNumber**
</dt> <dd>

Indica que los datos asociados a la clave son un número.

</dd> <dt>

<span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**ParamString**
</dt> <dd>

Indica que los datos asociados a la clave son una cadena.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción al servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Enumeraciones de administración del servidor RAS](ras-server-administration-enumerations.md)
</dt> <dt>

[**parámetros de RAS \_**](ras-parameters-str.md)
</dt> </dl>

 

 





