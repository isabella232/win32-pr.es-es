---
title: Método INapSystemHealthAgentBinding FlushCache (NapSystemHealthAgent.h)
description: Un SHA llama a para vaciar su caché de SoH.
ms.assetid: a771ce03-1922-4e2d-9490-7ee9f693857c
keywords:
- Nap del método FlushCache
- Método NAP de FlushCache, interfaz INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP , FlushCache method
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.FlushCache
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca721f2176b5e600c4afc7d71cd23d0507083d3c112adb4cb36af3b8734da0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037765"
---
# <a name="inapsystemhealthagentbindingflushcache-method"></a>INapSystemHealthAgentBinding::FlushCache (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Sha llama al método **INapSystemHealthAgentBinding::FlushCache** para vaciar su caché de SoH.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FlushCache();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                         | Descripción                                                                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>               | Operación realizada correctamente.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>     | Error de permisos, acceso denegado.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>      | El límite de recursos del sistema no pudo realizar la operación.<br/>                                                             |
| <dl> <dt>**RPC \_ E \_ DESCONECTADO**</dt> </dl> | NapAgent se ha detenido. Este objeto se recuperará automáticamente y se volverá a conectar a NapAgent, una vez que se reinicie.<br/> |



 

## <a name="remarks"></a>Comentarios

NapAgent mantiene una memoria caché de los SOH recientes proporcionados por diferentes SHA. Esta memoria caché es útil para optimizar el rendimiento en tiempo de arranque, cuando es posible que las SHA se puedan enlazar al sistema o no.

Sha debe llamar a [**Initialize antes**](inapsystemhealthagentbinding-initialize-method.md) de llamar a este método o a cualquier otro método de la [**interfaz INapSystemHealthAgentBinding2.**](inapsystemhealthagentbinding2.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





