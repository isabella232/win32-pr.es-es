---
title: Método Initialize de INapSoHConstructor (NapProtocol.h)
description: Inicializa un paquete de protocolo SoH en el sistema NAP.
ms.assetid: 1678b677-c8c8-465c-a412-9b929e39bbac
keywords:
- Inicialización del método NAP
- Inicializar el método NAP , INapSoHConstructor (interfaz)
- INapSoHConstructor interface NAP , Initialize (método)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473761"
---
# <a name="inapsohconstructorinitialize-method"></a>INapSoHConstructor::Initialize (Método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapSoHConstructor::Initialize** inicializa un paquete de protocolo SoH en el sistema NAP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId id,
  [in] BOOL                 isRequest
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*id* \[ en\]
</dt> <dd>

[SystemHealthEntityId único que](nap-datatypes.md) contiene el identificador de SHA o SHV que está construyendo el paquete.

</dd> <dt>

*isRequest* \[ En\]
</dt> <dd>

Valor **BOOL** que es **TRUE** si el paquete va a ser [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) y **FALSE** si va a ser **soHResponse**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación correcta.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

Se debe llamar a este método exactamente una vez por paquete.

[SystemHealthEntityId](nap-datatypes.md) especificado en *el* identificador , es el primer TLV del paquete SOH recién construido y tiene el tipo de atributo [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





