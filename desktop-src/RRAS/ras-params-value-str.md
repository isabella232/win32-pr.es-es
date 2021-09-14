---
title: RAS_PARAMS_VALUE unión (Rassapi.h)
description: La unión \_ RAS PARAMS VALUE se usa en la estructura PARAMETERS de RAS para almacenar los datos \_ \_ asociados a un parámetro específico del medio.
ms.assetid: 43284ee4-9bd4-4019-860f-0fb7ff3f38ee
keywords:
- RAS_PARAMS_VALUE ras de unión
topic_type:
- apiref
api_name:
- RAS_PARAMS_VALUE
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f8cc6d693b32b1bbe6f05e8d32ca31a48cfb29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073882"
---
# <a name="ras_params_value-union"></a>Unión DE \_ VALORES DE RAS PARAMS \_

\[La **unión \_ RAS PARAMS \_ VALUE** no se admite a Windows Vista.\]

La **unión \_ RAS PARAMS \_ VALUE** se usa en la estructura [**PARAMETERS \_ de RAS**](ras-parameters-str.md) para almacenar los datos asociados a un parámetro específico del medio. El **miembro P \_ Type** de la estructura **RAS \_ PARAMETERS** usa un valor de la enumeración [**RAS \_ PARAMS \_ FORMAT**](ras-params-format-str.md) para indicar el tipo de valor almacenado actualmente en **RAS \_ PARAMS \_ VALUE**.

## <a name="syntax"></a>Sintaxis


```C++
typedef union RAS_PARAMS_VALUE {
  DWORD  Number;
  struct {
    DWORD Length;
    PCHAR Data;
  } String;
} RAS_PARAMS_VALUE;
```



## <a name="members"></a>Members

<dl> <dt>

**Number**
</dt> <dd>

Si el **miembro P \_ Type** de la estructura [**RAS \_ PARAMETERS**](ras-parameters-str.md) es ParamNumber, el **miembro Number** contiene el valor del parámetro específico del medio. Por ejemplo, el parámetro MAXCONNECTBPS es de tipo ParamNumber y el valor podría ser 19200.

Si el **miembro P \_ Type** de la estructura [**RAS \_ PARAMETERS**](ras-parameters-str.md) es ParamNumber, el **miembro Number** contiene el valor del parámetro específico del medio. Por ejemplo, el parámetro MAXCONNECTBPS es de tipo ParamNumber y el valor podría ser 19200.

</dd> <dt>

**String**
</dt> <dd>

Si el **miembro \_ P Type** de la estructura RAS [**\_ PARAMETERS**](ras-parameters-str.md) es ParamString, el **miembro String** contiene el valor del parámetro específico del medio.

<dl> <dt>

**Duración**
</dt> <dd>

Especifica la longitud, en caracteres, de la cadena a la que apunta el **miembro** Data.

</dd> <dt>

**Data**
</dt> <dd>

Puntero a un búfer que contiene el valor de cadena de un parámetro específico del medio.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Introducción al Servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[RAS Server Administration Union](ras-server-administration-union.md)
</dt> <dt>

[**PARÁMETROS \_ RAS**](ras-parameters-str.md)
</dt> <dt>

[**RAS \_ PARAMS \_ FORMAT**](ras-params-format-str.md)
</dt> </dl>

 

 





