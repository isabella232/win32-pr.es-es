---
title: Método INapComponentConfig3 DeleteConfig (NapCommon. h)
description: Lo implementan los validadores de mantenimiento del sistema (SHV) para proporcionar una manera de eliminar los datos de configuración de un identificador de configuración específico.
ms.assetid: 9740c122-86c8-4b77-9268-faa90e84d8aa
keywords:
- Método DeleteConfig NAP
- Método DeleteConfig NAP, interfaz INapComponentConfig3
- Interfaz INapComponentConfig3 NAP, método DeleteConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a9b9a6838616f0892b45df34d9a7c5ed63ff16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801861"
---
# <a name="inapcomponentconfig3deleteconfig-method"></a>INapComponentConfig3::D método eleteConfig

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los validadores de mantenimiento del sistema (SHV) implementan el método **DeleteConfig** para proporcionar una manera de eliminar los datos de configuración de un identificador de configuración específico. El identificador se puede reutilizar una vez eliminados los datos de configuración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteConfig(
   UINT32 configID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*configID* 
</dt> <dd>

Valor que representa los datos de configuración que se van a eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                                    | Descripción                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>                          | La operación se realizó correctamente.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                   | *ConfigID* es 0 (un valor reservado para la configuración predeterminada).<br/> |
| <dl> <dt>**\_ \_ \_ \_ no se encontró la configuración \_ de SHV de NAP**</dt> </dl> | No se encuentra *ConfigID* .<br/>                                       |



 

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

 

 





