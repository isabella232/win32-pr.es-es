---
title: Método INapComponentConfig3 documento newconfig (NapCommon. h)
description: Lo implementan los validadores de mantenimiento del sistema (SHV) para proporcionar una manera de crear datos de configuración para un identificador de configuración específico.
ms.assetid: cea762d3-815d-4034-94c1-5fa9a859cce8
keywords:
- Método documento newconfig NAP
- Método documento newconfig NAP, interfaz INapComponentConfig3
- Interfaz INapComponentConfig3 NAP, método documento newconfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.NewConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 924204068dbb66b22cc06d28966511d8922e0068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150102"
---
# <a name="inapcomponentconfig3newconfig-method"></a>INapComponentConfig3:: documento newconfig (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los validadores de mantenimiento del sistema (SHV) implementan el método **documento newconfig** para proporcionar una manera de crear datos de configuración para un identificador de configuración específico. Cuando se llama a esta función, un SHV debe asignar nuevos datos de configuración y rellenarlos con una copia de los datos de configuración predeterminados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NewConfig(
   UINT32 configID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*configID* 
</dt> <dd>

Valor que representa la configuración. El servicio del servidor de directivas de redes (NPS) asigna *ConfigID* y es único en el SHV.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                                 | Descripción                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>                       | La operación se realizó correctamente.<br/>                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                | *ConfigID* es 0 (un valor reservado para la configuración predeterminada).<br/>                  |
| <dl> <dt>**\_existe la \_ configuración de SHV E \_ NAP \_**</dt> </dl> | *ConfigID* ya existe. La lista de identificadores conocidos para NPS es diferente del SHV.<br/> |



 

## <a name="remarks"></a>Observaciones

Una vez que **documento newconfig** crea la nueva configuración, se deben usar los métodos [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md), [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)y [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) para modificar la configuración según sea necesario.

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

 

 





