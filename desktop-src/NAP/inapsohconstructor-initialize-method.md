---
title: Método Initialize INapSoHConstructor (NapProtocol. h)
description: Inicializa un paquete de protocolo SoH en el sistema NAP.
ms.assetid: 1678b677-c8c8-465c-a412-9b929e39bbac
keywords:
- Inicializar el método NAP
- Inicializar método NAP, interfaz INapSoHConstructor
- Interfaz INapSoHConstructor NAP, método Initialize
topic_type:
- apiref
api_name:
- INapSoHConstructor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab8d6b27547be6e7c7e9abb59f7edb7b49e716e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996319"
---
# <a name="inapsohconstructorinitialize-method"></a>INapSoHConstructor:: Initialize (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapSoHConstructor:: Initialize** Inicializa un paquete de protocolo SOH en el sistema NAP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId id,
  [in] BOOL                 isRequest
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ID.* \[ en\]
</dt> <dd>

Un [SystemHealthEntityId](nap-datatypes.md) único que contiene el identificador del Sha o SHV que está construyendo el paquete.

</dd> <dt>

*isRequest* \[ de\]
</dt> <dd>

Valor **booleano** que es **true** si el paquete va a ser un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) y **false** si va a ser un **SoHResponse**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | Operación correcta.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

Se debe llamar a este método exactamente una vez por paquete.

El [SystemHealthEntityId](nap-datatypes.md) especificado en *ID*. es el primer TLV del paquete SOH recién construido y tiene el tipo de atributo [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





