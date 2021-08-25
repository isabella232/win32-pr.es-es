---
title: RAS_PARAMS_FORMAT enumeración (Rassapi.h)
description: El tipo de enumeración RAS PARAMS FORMAT se usa en la estructura PARAMETERS de RAS para indicar el tipo de datos \_ asociado a una clave específica del \_ \_ medio.
ms.assetid: dd2c0110-1f27-4a8f-bc61-f15588ebc4ca
keywords:
- RAS_PARAMS_FORMAT enumeración RAS
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
ms.openlocfilehash: 92b798ef8a5257afcb4e4ad653801bda0d21691057abad970d6e8158f592146e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673185"
---
# <a name="ras_params_format-enumeration"></a>Enumeración RAS \_ PARAMS \_ FORMAT

\[La **\_ enumeración RAS PARAMS \_ FORMAT** no se admite desde Windows Vista.\]

El **tipo \_ de enumeración RAS PARAMS \_ FORMAT** se usa en la estructura [**PARAMETERS \_ de RAS**](ras-parameters-str.md) para indicar el tipo de datos asociado a una clave específica del medio.

## <a name="syntax"></a>Syntax


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
| Header<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción al Servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Enumeraciones de administración del servidor RAS](ras-server-administration-enumerations.md)
</dt> <dt>

[**PARÁMETROS \_ RAS**](ras-parameters-str.md)
</dt> </dl>

 

 





