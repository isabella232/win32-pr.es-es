---
title: Método INapComponentConfig SetConfig (NapCommon. h)
description: Establece la configuración del componente de validador de mantenimiento del sistema (SHV).
ms.assetid: ec27e30b-4205-40bc-a24b-61072a746e53
keywords:
- Método SetConfig NAP
- Método SetConfig NAP, interfaz INapComponentConfig
- Interfaz INapComponentConfig NAP, método SetConfig
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
ms.openlocfilehash: 7a1f3d557517ec27f9537a7cbcd46be9e2cd107e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535613"
---
# <a name="inapcomponentconfigsetconfig-method"></a>INapComponentConfig:: SetConfig (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **SetConfig** establece la configuración del componente de validador de mantenimiento del sistema (SHV).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetConfig(
  [in] UINT16 bCount,
  [in] BYTE   *data
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bCount* \[ de\]
</dt> <dd>

Tamaño, en bytes, del BLOB de configuración de *datos* .

</dd> <dt>

*datos* \[ de de\]
</dt> <dd>

Puntero a los datos de configuración del componente de SHV.

> [!Note]  
> Los datos de configuración exportados desde un equipo x86 mediante el método [**GetConfig**](inapcomponentconfig-getconfig.md) se pueden importar en un equipo x64 mediante el método **SetConfig** y viceversa. Por lo tanto, los datos de configuración deben estar en un formato independiente de la arquitectura, como XML. El uso de XML en lugar de un flujo de bytes facilita el uso de datos de configuración en diferentes arquitecturas. El implementador determina los elementos XML utilizados en los datos de configuración.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

La información de control de versiones de componentes debe incluirse en el BLOB de configuración de *datos* . Se puede usar la información de control de versiones al migrar de una versión de SHV a otra.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapConponentConfig:: GetConfig**](inapcomponentconfig-getconfig.md)
</dt> </dl>

 

 





