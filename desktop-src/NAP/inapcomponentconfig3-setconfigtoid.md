---
title: Método INapComponentConfig3 SetConfigToID (NapCommon.h)
description: Los validadores de estado del sistema (SHV) implementan para proporcionar una manera de establecer los datos de configuración de un identificador de configuración específico.
ms.assetid: 1fa0b8e7-b597-4ab1-bb61-2cab47b92ce3
keywords:
- Método NAP de SetConfigToID
- Método NAP de SetConfigToID, interfaz INapComponentConfig3
- Nap de interfaz INapComponentConfig3, método SetConfigToID
topic_type:
- apiref
api_name:
- INapComponentConfig3.SetConfigToID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 010fdc6cbb236a113e4f1804d3a4780c0e6a72f89b1f03bf90f1d99a92dc2bdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781085"
---
# <a name="inapcomponentconfig3setconfigtoid-method"></a>INapComponentConfig3::SetConfigToID (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los validadores de estado del sistema (SHV) implementan el método **SetConfigToID** para proporcionar una manera de establecer los datos de configuración de un identificador de configuración específico.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetConfigToID(
  [in] UINT32 configID,
  [in] UINT16 count,
  [in] BYTE   *data
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*configID* \[ En\]
</dt> <dd>

Valor que representa la configuración. *El servicio Servidor* de directivas de red (NPS) asigna ConfigID y es único dentro de shv. Si *ConfigID* es 0, se establece la configuración predeterminada de shv.

</dd> <dt>

*count* \[ En\]
</dt> <dd>

Tamaño, en bytes, de los datos de configuración de *los datos*.

</dd> <dt>

*datos* \[ En\]
</dt> <dd>

En la entrada, una matriz BYTE que contiene los datos de configuración establecidos en *ConfigID*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                                    | Descripción                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>                          | La operación se realizó correctamente.<br/> |
| <dl> <dt>**NO \_ SE ENCONTRÓ LA CONFIGURACIÓN DE NAP E \_ SHV \_ \_ \_**</dt> </dl> | *No se encuentra ConfigID.*<br/>  |



 

## <a name="remarks"></a>Comentarios

El [**método NewConfig**](inapcomponentconfig3-newconfig.md) debe usarse para asignar datos de configuración para *ConfigID* antes de que se pueda llamar a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                  |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





