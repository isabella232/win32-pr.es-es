---
title: RAS_PARAMETERS estructura (Rassapi.h)
description: La función RasAdminPortGetInfo usa la estructura DE PARÁMETROS DE RAS para devolver el nombre y el valor de un parámetro específico del medio asociado a un puerto en \_ un servidor RAS.
ms.assetid: b46b6176-9a0c-4d9b-b961-b20fdc41653b
keywords:
- RAS_PARAMETERS estructura RAS
topic_type:
- apiref
api_name:
- RAS_PARAMETERS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e38ec1a8febbca4319a9c098eafee3705fe59602af81b3ec94e4e974892be771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909675"
---
# <a name="ras_parameters-structure"></a>Estructura \_ DE PARÁMETROS RAS

\[La **estructura DE PARÁMETROS \_ RAS** no se admite a Windows Vista.\]

La función [**RasAdminPortGetInfo**](rasadminportgetinfo.md) usa la estructura **\_ DE** PARÁMETROS DE RAS para devolver el nombre y el valor de un parámetro específico del medio asociado a un puerto en un servidor RAS.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct RAS_PARAMETERS {
  CHAR              P_Key[RASSAPI_MAX_PARAM_KEY_SIZE];
  RAS_PARAMS_FORMAT P_Type;
  BYTE              P_Attributes;
  RAS_PARAMS_VALUE  P_Value;
} RAS_PARAMETERS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**P \_ Key**
</dt> <dd>

Especifica el nombre de la clave que representa el parámetro específico del medio, como MAXCONNECTBPS.

</dd> <dt>

**Tipo \_ P**
</dt> <dd>

Identifica el tipo de datos asociados al parámetro . Este miembro puede ser uno de los siguientes valores de la [**enumeración RAS \_ PARAMS \_ FORMAT.**](ras-params-format-str.md)



| Value                                                                                                                                                                                | Significado                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span><dl> <dt>**ParamNumber**</dt> </dl> | Indica que los datos asociados a la clave son un número.<br/> |
| <span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span><dl> <dt>**ParamString**</dt> </dl> | Indica que los datos asociados a la clave son una cadena.<br/> |



 

</dd> <dt>

**Atributos \_ P**
</dt> <dd>

Reservado.

</dd> <dt>

**Valor \_ P**
</dt> <dd>

Especifica el valor asociado al parámetro . Este miembro es una [**unión RAS \_ PARAMS \_ VALUE.**](ras-params-value-str.md) Si el **miembro \_ tipo P** es ParamNumber, el **miembro Number** de la unión contiene el valor. Si **P \_ Type** es ParamString, el **miembro String** de la unión contiene el valor.

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

[Estructuras de administración del servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





