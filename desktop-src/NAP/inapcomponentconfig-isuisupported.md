---
title: Método INapComponentConfig IsUISupported (NapCommon. h)
description: Especifica si el componente admite una interfaz de usuario personalizada.
ms.assetid: 044f8014-f041-4e9c-922a-2691b799ba84
keywords:
- Método IsUISupported NAP
- Método IsUISupported NAP, interfaz INapComponentConfig
- Interfaz INapComponentConfig NAP, método IsUISupported
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
ms.openlocfilehash: ab7d3f6b87ba5e483b466e6746f0f63d039cb205
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676747"
---
# <a name="inapcomponentconfigisuisupported-method"></a>INapComponentConfig:: IsUISupported (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **IsUISupported** especifica si el componente admite una interfaz de usuario personalizada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsUISupported(
  [out] BOOL *isSupported
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*isSupported* \[ enuncia\]
</dt> <dd>

Un puntero a un valor BOOLEANO que se establece en **true** si el componente admite una interfaz de usuario personalizada y **false** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

La interfaz de usuario personalizada de un componente se debe iniciar mediante [**INapComponentConfig:: InvokeUI**](inapcomponentconfig-invokeui.md).

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

[**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md)
</dt> </dl>

 

 





