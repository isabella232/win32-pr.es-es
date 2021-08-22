---
title: Método INapComponentConfig SetConfig (NapCommon.h)
description: Establece la configuración del componente del validador de estado del sistema (SHV).
ms.assetid: ec27e30b-4205-40bc-a24b-61072a746e53
keywords:
- Método NAP de SetConfig
- Método NAP de SetConfig, interfaz INapComponentConfig
- INapComponentConfig interface NAP , Método SetConfig
topic_type:
- apiref
api_name:
- INapComponentConfig.SetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b3ecf455c591985a5e8778e49495351bd1b4aba83e9d29fe2b25d7d406a507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940203"
---
# <a name="inapcomponentconfigsetconfig-method"></a>INapComponentConfig::SetConfig (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método SetConfig** establece la configuración del componente de validador de estado del sistema (SHV).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetConfig(
  [in] UINT16 bCount,
  [in] BYTE   *data
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bCount* \[ En\]
</dt> <dd>

Tamaño, en bytes, del blob *de configuración* de datos.

</dd> <dt>

*datos* \[ En\]
</dt> <dd>

Puntero a los datos de configuración del componente SHV.

> [!Note]  
> Los datos de configuración exportados desde una máquina x86 mediante el método [**GetConfig**](inapcomponentconfig-getconfig.md) se pueden importar a una máquina x64 mediante el **método SetConfig** y viceversa. Por lo tanto, los datos de configuración deben estar en un formato independiente de la arquitectura, como XML. El uso de XML en lugar de una secuencia de bytes facilita el uso de datos de configuración en distintas arquitecturas. El implementador determina los elementos XML utilizados en los datos de configuración.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error según el resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Comentarios

La información de control de versiones de componentes debe incluirse en el blob *de configuración* de datos. La información de control de versiones se puede usar al migrar de una versión de SHV a otra.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapConponentConfig::GetConfig**](inapcomponentconfig-getconfig.md)
</dt> </dl>

 

 





