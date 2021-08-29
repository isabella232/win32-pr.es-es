---
title: Método InvokeUI de INapComponentConfig (NapCommon.h)
description: Inicia una interfaz de usuario personalizada para un componente de validador de estado del sistema (SHV).
ms.assetid: da2a5e3e-bc17-4984-bdbe-b72e9e710a9d
keywords:
- Método NAP de InvokeUI
- Método NAP de InvokeUI, interfaz INapComponentConfig
- INapComponentConfig interface NAP , InvokeUI method
topic_type:
- apiref
api_name:
- INapComponentConfig.InvokeUI
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0983c01ae1adc86b54eca3c958942aab9b5c832c8cac3b2c8a0b9352b7d96b39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686505"
---
# <a name="inapcomponentconfiginvokeui-method"></a>INapComponentConfig::InvokeUI (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método InvokeUI** inicia una interfaz de usuario personalizada para un componente de validador de estado del sistema (SHV).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InvokeUI(
  [in] HWND hwndParent
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ En\]
</dt> <dd>

Identificador de la ventana primaria o propietaria. Se debe proporcionar un identificador de ventana válido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>       | Shv no admite una interfaz de usuario personalizada.<br/>               |



 

## <a name="remarks"></a>Comentarios

Esta llamada al método debe bloquearse hasta que se cierre la interfaz de usuario de SHV.

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

[**INapComponentConfig::IsUISupported**](inapcomponentconfig-isuisupported.md)
</dt> </dl>

 

 





