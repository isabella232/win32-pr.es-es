---
title: RAS_PARAMS_VALUE Union (rassapi. h)
description: La \_ \_ Unión de valores de parámetros de Ras se usa en la estructura de parámetros de Ras \_ para almacenar los datos asociados a un parámetro específico del medio.
ms.assetid: 43284ee4-9bd4-4019-860f-0fb7ff3f38ee
keywords:
- RAS de RAS_PARAMS_VALUE Union
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149869"
---
# <a name="ras_params_value-union"></a>Valores de parámetros de RAS \_ \_ Union

\[La Unión de **\_ \_ valores de parámetros de Ras** no es compatible con Windows Vista.\]

La Unión de **\_ \_ valores** de parámetros de Ras se usa en la estructura de [**\_ parámetros de Ras**](ras-parameters-str.md) para almacenar los datos asociados a un parámetro específico del medio. El miembro de **\_ tipo P** de la estructura de parámetros de Ras usa un valor de la enumeración de [**\_ \_ formato**](ras-params-format-str.md) de **\_ parámetros** de ras para indicar el tipo de valor almacenado actualmente en el valor de los **\_ parámetros \_ de Ras**.

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



## <a name="members"></a>Miembros

<dl> <dt>

**Number**
</dt> <dd>

Si el miembro de **\_ tipo P** de la estructura de [**\_ parámetros de Ras**](ras-parameters-str.md) es ParamNumber, el miembro **Number** contiene el valor del parámetro específico del medio. Por ejemplo, el parámetro MAXCONNECTBPS es de tipo ParamNumber y el valor puede ser 19200.

Si el miembro de **\_ tipo P** de la estructura de [**\_ parámetros de Ras**](ras-parameters-str.md) es ParamNumber, el miembro **Number** contiene el valor del parámetro específico del medio. Por ejemplo, el parámetro MAXCONNECTBPS es de tipo ParamNumber y el valor puede ser 19200.

</dd> <dt>

**String**
</dt> <dd>

Si el miembro de **\_ tipo P** de la estructura de [**\_ parámetros de Ras**](ras-parameters-str.md) es ParamString, el miembro de **cadena** contiene el valor del parámetro específico del medio.

<dl> <dt>

**Duración**
</dt> <dd>

Especifica la longitud, en caracteres, de la cadena a la que apunta el miembro de **datos** .

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
| Encabezado<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción al servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Unión de administración del servidor RAS](ras-server-administration-union.md)
</dt> <dt>

[**parámetros de RAS \_**](ras-parameters-str.md)
</dt> <dt>

[**formato de parámetros de RAS \_ \_**](ras-params-format-str.md)
</dt> </dl>

 

 





