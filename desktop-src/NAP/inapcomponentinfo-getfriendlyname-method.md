---
title: Método INapComponentInfo GetFriendlyName (NapCommon. h)
description: Lo usa el sistema NAP para obtener el nombre descriptivo de un cliente de mantenimiento.
ms.assetid: 28614f06-a250-4f92-abf2-422675efd8a0
keywords:
- Método GetFriendlyName NAP
- Método GetFriendlyName NAP, interfaz INapComponentInfo
- Interfaz INapComponentInfo NAP, método GetFriendlyName
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
ms.openlocfilehash: 3848f8fb8365f91bceb5a44c498578f04a1776b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492808"
---
# <a name="inapcomponentinfogetfriendlyname-method"></a>INapComponentInfo:: GetFriendlyName (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El sistema NAP usa el método de devolución de llamada **INapComponentInfo:: GetFriendlyName** para obtener el nombre descriptivo de un cliente de mantenimiento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFriendlyName(
  [out] MessageId *friendlyName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*friendlyName* \[ enuncia\]
</dt> <dd>

Un puntero a un [**MessageId**](nap-datatypes.md) que contiene el identificador de recurso del nombre descriptivo.

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

 

 





