---
title: Método INapComponentConfig3 SetConfigToID (NapCommon. h)
description: Los validadores de mantenimiento del sistema (SHV) implementan para proporcionar una manera de establecer los datos de configuración para un identificador de configuración específico.
ms.assetid: 1fa0b8e7-b597-4ab1-bb61-2cab47b92ce3
keywords:
- Método SetConfigToID NAP
- Método SetConfigToID NAP, interfaz INapComponentConfig3
- Interfaz INapComponentConfig3 NAP, método SetConfigToID
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
ms.openlocfilehash: 3158a216ba4fd4f82f3e4fc21fc1e0043b16a46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666086"
---
# <a name="inapcomponentconfig3setconfigtoid-method"></a>INapComponentConfig3:: SetConfigToID (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los validadores de mantenimiento del sistema (SHV) implementan el método **SetConfigToID** para proporcionar una manera de establecer los datos de configuración para un identificador de configuración específico.

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

*configID* \[ de\]
</dt> <dd>

Valor que representa la configuración. El servicio del servidor de directivas de redes (NPS) asigna *ConfigID* y es único en el SHV. Si *ConfigID* es 0, se establece la configuración predeterminada del SHV.

</dd> <dt>

*recuento* \[ de\]
</dt> <dd>

Tamaño, en bytes, de los datos de configuración de los *datos*.

</dd> <dt>

*datos* \[ de de\]
</dt> <dd>

En la entrada, una matriz de BYTEs que contiene los datos de configuración establecidos en *ConfigID*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                                    | Descripción                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>                          | La operación se realizó correctamente.<br/> |
| <dl> <dt>**\_ \_ \_ \_ no se encontró la configuración \_ de SHV de NAP**</dt> </dl> | No se encuentra *ConfigID* .<br/>  |



 

## <a name="remarks"></a>Observaciones

El método [**documento newconfig**](inapcomponentconfig3-newconfig.md) debe usarse para asignar los datos de configuración de *ConfigID* antes de que se pueda llamar a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





