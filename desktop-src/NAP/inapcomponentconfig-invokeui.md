---
title: Método INapComponentConfig InvokeUI (NapCommon. h)
description: Inicia una interfaz de usuario personalizada para un componente de validador de mantenimiento del sistema (SHV).
ms.assetid: da2a5e3e-bc17-4984-bdbe-b72e9e710a9d
keywords:
- Método InvokeUI NAP
- Método InvokeUI NAP, interfaz INapComponentConfig
- Interfaz INapComponentConfig NAP, método InvokeUI
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
ms.openlocfilehash: 2dd86d683365286fc2130c1ac9edf21ff075d61a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996188"
---
# <a name="inapcomponentconfiginvokeui-method"></a>INapComponentConfig:: InvokeUI (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **InvokeUI** inicia una interfaz de usuario personalizada para un componente de validador de mantenimiento del sistema (SHV).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InvokeUI(
  [in] HWND hwndParent
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ de\]
</dt> <dd>

Identificador de la ventana primaria o propietaria. Se debe proporcionar un identificador de ventana válido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>       | El SHV no es compatible con una interfaz de usuario personalizada.<br/>               |



 

## <a name="remarks"></a>Observaciones

Esta llamada al método debe bloquearse hasta que se cierre la interfaz de usuario de SHV.

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

[**INapComponentConfig::IsUISupported**](inapcomponentconfig-isuisupported.md)
</dt> </dl>

 

 





