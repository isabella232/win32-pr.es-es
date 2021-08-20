---
title: Método INapComponentInfo GetFriendlyName (NapCommon.h)
description: Lo usa el sistema NAP para obtener el nombre descriptivo de un cliente de mantenimiento.
ms.assetid: 28614f06-a250-4f92-abf2-422675efd8a0
keywords:
- Método NAP GetFriendlyName
- Método GetFriendlyName NAP , interfaz INapComponentInfo
- INapComponentInfo interfaz NAP , Método GetFriendlyName
topic_type:
- apiref
api_name:
- INapComponentInfo.GetFriendlyName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3236a9d4959c441816aa476993d95286b4ac1f710ccdb63325aba225bfabb106
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799720"
---
# <a name="inapcomponentinfogetfriendlyname-method"></a>Método INapComponentInfo::GetFriendlyName

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El sistema NAP usa el método de devolución de llamada **INapComponentInfo::GetFriendlyName** para obtener el nombre descriptivo de un cliente de mantenimiento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFriendlyName(
  [out] MessageId *friendlyName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*friendlyName* \[ out\]
</dt> <dd>

Puntero a un [**MessageId**](nap-datatypes.md) que contiene el identificador de recurso del nombre descriptivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de estos códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





