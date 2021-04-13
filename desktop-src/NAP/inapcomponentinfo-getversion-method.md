---
title: Método GetVersion de INapComponentInfo (NapCommon. h)
description: Lo usa el sistema NAP para obtener la versión de un cliente de mantenimiento.
ms.assetid: aabd13d9-d2ad-4554-a9f6-7845e6775ccd
keywords:
- GetVersion (método) NAP
- Método GetVersion NAP, interfaz INapComponentInfo
- Interfaz INapComponentInfo NAP, método GetVersion
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
ms.openlocfilehash: fa1d62c22acf778430bfc2f9dc0e969887c7b306
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535535"
---
# <a name="inapcomponentinfogetversion-method"></a>INapComponentInfo:: GetVersion (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El sistema NAP usa el método de devolución de llamada **INapComponentInfo:: GetVersion** para obtener la versión de un cliente de mantenimiento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetVersion(
  [out] MessageId *version
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*versión* \[ de enuncia\]
</dt> <dd>

Un puntero a un [**MessageId**](nap-datatypes.md) que contiene el identificador de recurso de la versión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelva uno de estos códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





