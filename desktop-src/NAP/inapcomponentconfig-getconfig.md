---
title: Método GetConfig de INapComponentConfig (NapCommon. h)
description: Recupera la configuración del componente de validador de mantenimiento del sistema (SHV).
ms.assetid: 57a1d3a7-05c0-4e0f-91b8-b3cf8982d04f
keywords:
- GetConfig (método) NAP
- Método GetConfig NAP, interfaz INapComponentConfig
- Interfaz INapComponentConfig NAP, método GetConfig
topic_type:
- apiref
api_name:
- INapComponentConfig.GetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e07465d768c8902166150e53d4200e775e2597
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492335"
---
# <a name="inapcomponentconfiggetconfig-method"></a>INapComponentConfig:: GetConfig (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **GetConfig** recupera la configuración del componente de validador de mantenimiento del sistema (SHV).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetConfig(
  [out] UINT16 *bCount,
  [out] BYTE   **data
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bCount* \[ enuncia\]
</dt> <dd>

Tamaño, en bytes, del BLOB de configuración de *datos* .

</dd> <dt>

*datos* \[ de enuncia\]
</dt> <dd>

Puntero a la dirección de los datos de configuración del componente de SHV.

> [!Note]  
> Los datos de configuración exportados desde un equipo x86 mediante el método **GetConfig** se pueden importar en un equipo x64 mediante el método [**SetConfig**](inapcomponentconfig-setconfig.md) y viceversa. Por lo tanto, los datos de configuración deben estar en un formato independiente de la arquitectura, como XML. El uso de XML en lugar de un flujo de bytes facilita el uso de datos de configuración en diferentes arquitecturas. El implementador determina los elementos XML utilizados en los datos de configuración.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

El destinatario (implementador de componentes) debe asignar el parámetro de datos mediante **CoTaskMemAlloc** y el autor de la llamada lo libera mediante **CoTaskMemFree**.

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

[**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md)
</dt> </dl>

 

 





