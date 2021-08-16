---
title: Método INapComponentInfo GetVersion (NapCommon.h)
description: Lo usa el sistema NAP para obtener la versión de un cliente de mantenimiento.
ms.assetid: aabd13d9-d2ad-4554-a9f6-7845e6775ccd
keywords:
- Nap del método GetVersion
- Método NAP de GetVersion, interfaz INapComponentInfo
- Nap de interfaz INapComponentInfo, método GetVersion
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVersion
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e815c7d92ba9a33c07ba4d8d68c588ed0014019d0d173e0304c4a10204d4d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368392"
---
# <a name="inapcomponentinfogetversion-method"></a>INapComponentInfo::GetVersion (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El sistema NAP usa el método de devolución de llamada **INapComponentInfo::GetVersion** para obtener la versión de un cliente de mantenimiento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetVersion(
  [out] MessageId *version
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*versión* \[ out\]
</dt> <dd>

Puntero a un [**MessageId**](nap-datatypes.md) que contiene el identificador de recurso de la versión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de estos códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





