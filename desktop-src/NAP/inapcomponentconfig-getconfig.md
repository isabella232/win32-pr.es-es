---
title: Método INapComponentConfig GetConfig (NapCommon.h)
description: Recupera la configuración del componente de validador de estado del sistema (SHV).
ms.assetid: 57a1d3a7-05c0-4e0f-91b8-b3cf8982d04f
keywords:
- Método NAP de GetConfig
- Método NAP de GetConfig, interfaz INapComponentConfig
- INapComponentConfig interface NAP , GetConfig method
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
ms.openlocfilehash: d8dc5495df10e3a5ff3907941644c5558aea35d29b52c8773fb56314c4a8620c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134503"
---
# <a name="inapcomponentconfiggetconfig-method"></a>INapComponentConfig::GetConfig (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método GetConfig** recupera la configuración del componente de validador de estado del sistema (SHV).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetConfig(
  [out] UINT16 *bCount,
  [out] BYTE   **data
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bCount* \[ out\]
</dt> <dd>

Tamaño, en bytes, del blob *de configuración* de datos.

</dd> <dt>

*datos* \[ out\]
</dt> <dd>

Puntero a la dirección de los datos de configuración del componente SHV.

> [!Note]  
> Los datos de configuración exportados desde una máquina x86 mediante el método **GetConfig** se pueden importar a una máquina x64 mediante el [**método SetConfig**](inapcomponentconfig-setconfig.md) y viceversa. Por lo tanto, los datos de configuración deben estar en un formato independiente de la arquitectura, como XML. El uso de XML en lugar de una secuencia de bytes facilita el uso de datos de configuración en arquitecturas diferentes. El implementador determina los elementos XML utilizados en los datos de configuración.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Comentarios

El destinatario (implementador de componentes) debe asignar el parámetro de datos mediante **CoTaskMemAlloc** y liberarlo el autor de la llamada mediante **CoTaskMemFree.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md)
</dt> </dl>

 

 





