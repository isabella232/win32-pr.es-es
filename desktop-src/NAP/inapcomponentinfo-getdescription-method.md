---
title: Método INapComponentInfo GetDescription (NapCommon.h)
description: Lo usa el sistema NAP para obtener la descripción de un cliente de mantenimiento.
ms.assetid: f8d1d5ea-0de6-426d-90eb-b035b5bd0bfd
keywords:
- Método NAP de GetDescription
- Método GETDescription NAP, interfaz INapComponentInfo
- INapComponentInfo interface NAP , GetDescription method
topic_type:
- apiref
api_name:
- INapComponentInfo.GetDescription
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ece376dc2d5c8eb896850e6e92cb6cbd2439bf9b971302b52905368ded575d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891305"
---
# <a name="inapcomponentinfogetdescription-method"></a>INapComponentInfo::GetDescription (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El sistema NAP usa el método de devolución de llamada **INapComponentInfo::GetDescription** para obtener la descripción de un cliente de mantenimiento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDescription(
  [out] MessageId *description
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*descripción* \[ out\]
</dt> <dd>

Puntero a un [**MessageId**](nap-datatypes.md) que contiene el identificador de recurso de la descripción.

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

 

 





