---
title: Método INapComponentConfig3 GetConfigFromID (NapCommon. h)
description: Lo implementan los validadores de mantenimiento del sistema (SHV) para proporcionar una manera de obtener datos de configuración para un identificador de configuración específico.
ms.assetid: 5c91681d-16d6-42f3-b1e0-c4b6e7561a73
keywords:
- Método GetConfigFromID NAP
- Método GetConfigFromID NAP, interfaz INapComponentConfig3
- Interfaz INapComponentConfig3 NAP, método GetConfigFromID
topic_type:
- apiref
api_name:
- INapComponentConfig3.GetConfigFromID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce3a0e20f19c73271cdcba4070972649fe25aea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801855"
---
# <a name="inapcomponentconfig3getconfigfromid-method"></a>INapComponentConfig3:: GetConfigFromID (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los validadores de mantenimiento del sistema (SHV) implementan el método **GetConfigFromID** para proporcionar una manera de obtener datos de configuración para un identificador de configuración específico.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetConfigFromID(
  [in]  UINT32 configID,
  [out] UINT16 *count,
  [out] BYTE   **outdata
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*configID* \[ de\]
</dt> <dd>

Valor que representa la configuración. Si *ConfigID* es **0**, el SHV debe devolver los datos de configuración predeterminados *de los datos.*

</dd> <dt>

*recuento* \[ enuncia\]
</dt> <dd>

Tamaño, en bytes, de los datos de configuración devueltos en *outdata*.

</dd> <dt>

*outdata* \[ enuncia\]
</dt> <dd>

En la devolución, una matriz de BYTEs que contiene los datos de configuración representados por *ConfigID*.

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

 

 





