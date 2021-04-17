---
title: Método SetFlags de INapEnforcementClientConnection (NapEnforcementClient. h)
description: Se usa para diferenciar las respuestas por primera vez de las respuestas debido a SoHRequests almacenados en memoria caché por los imforcedores. | Método SetFlags de INapEnforcementClientConnection (NapEnforcementClient. h)
ms.assetid: 2f35bcdf-662c-431f-a39e-a7c758f35603
keywords:
- Método SetFlags NAP
- Método SetFlags NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método SetFlags
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489997fb97f0e97c5a72d23646af8ae92272628
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105653201"
---
# <a name="inapenforcementclientconnectionsetflags-method"></a>INapEnforcementClientConnection:: SetFlags (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapEnforcementClientConnection:: SetFlags** se usa para diferenciar las respuestas por primera vez de las respuestas debidas a SoHRequests almacenados en memoria caché por los imforcedores.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetFlags(
  [in] UINT8 flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*marcas* \[ de de\]
</dt> <dd>

Marcas que determinan si el [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) se debe a un **SoHRequest** almacenado en memoria caché. Si *Flags* tiene un valor de [**freshSoHRequest**](nap-type-constants.md), es una solicitud nueva; en caso contrario, se trata de una solicitud almacenada en caché.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

NapAgent establece este valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





