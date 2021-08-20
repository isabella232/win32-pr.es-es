---
title: Método INapComponentConfig IsUISupported (NapCommon.h)
description: Especifica si el componente admite una interfaz de usuario personalizada.
ms.assetid: 044f8014-f041-4e9c-922a-2691b799ba84
keywords:
- Método NAP de IsUISupported
- Método NAP de IsUISupported, interfaz INapComponentConfig
- INapComponentConfig interface NAP , IsUISupported method
topic_type:
- apiref
api_name:
- INapComponentConfig.IsUISupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e343b037e4f77b4c1e342ffa78278854b11d714e09e9e57188d83fc9f93a180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134493"
---
# <a name="inapcomponentconfigisuisupported-method"></a>INapComponentConfig::IsUISupported (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método IsUISupported** especifica si el componente admite una interfaz de usuario personalizada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsUISupported(
  [out] BOOL *isSupported
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*isSupported* \[ out\]
</dt> <dd>

Puntero a un bool que se establece en **TRUE** si el componente admite una interfaz de usuario personalizada y **FALSE** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Comentarios

La interfaz de usuario personalizada de un componente debe iniciarse mediante [**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md).

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

[**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md)
</dt> </dl>

 

 





