---
title: RAS_PARAMETERS estructura (rassapi. h)
description: '\_La función RasAdminPortGetInfo utiliza la estructura de parámetros de ras para devolver el nombre y el valor de un parámetro específico del medio asociado a un puerto en un servidor RAS.'
ms.assetid: b46b6176-9a0c-4d9b-b961-b20fdc41653b
keywords:
- RAS_PARAMETERS de la estructura RAS
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
ms.openlocfilehash: fffaefa8a6f2cffb895cc18882ed8fc0c382a4bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534906"
---
# <a name="ras_parameters-structure"></a>Estructura de parámetros de RAS \_

\[La estructura de **\_ parámetros de Ras** no es compatible con Windows Vista.\]

La función [**RasAdminPortGetInfo**](rasadminportgetinfo.md) utiliza la estructura de **\_ parámetros de Ras** para devolver el nombre y el valor de un parámetro específico del medio asociado a un puerto en un servidor RAS.

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

**\_Tecla P**
</dt> <dd>

Especifica el nombre de la clave que representa el parámetro específico del medio, como MAXCONNECTBPS.

</dd> <dt>

**\_Tipo P**
</dt> <dd>

Identifica el tipo de datos asociado al parámetro. Este miembro puede ser uno de los siguientes valores de la enumeración de [**\_ \_ formato**](ras-params-format-str.md) de los parámetros de Ras.



| Value                                                                                                                                                                                | Significado                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span><dl> <dt>**ParamNumber**</dt> </dl> | Indica que los datos asociados a la clave son un número.<br/> |
| <span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span><dl> <dt>**ParamString**</dt> </dl> | Indica que los datos asociados a la clave son una cadena.<br/> |



 

</dd> <dt>

**\_Atributos P**
</dt> <dd>

Reservado.

</dd> <dt>

**\_Valor P**
</dt> <dd>

Especifica el valor asociado al parámetro. Este miembro es una Unión de [**\_ \_ valores de parámetros de Ras**](ras-params-value-str.md) . Si el miembro de **\_ tipo P** es ParamNumber, el miembro **Number** de la Unión contiene el valor. Si **el \_ tipo P** es ParamString, el miembro de **cadena** de la Unión contiene el valor.

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

[Estructuras de administración del servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





