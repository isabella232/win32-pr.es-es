---
title: Método INapSystemHealthAgentBinding FlushCache (NapSystemHealthAgent. h)
description: Un SHA llama a para vaciar su caché de SoH.
ms.assetid: a771ce03-1922-4e2d-9490-7ee9f693857c
keywords:
- Método FlushCache NAP
- Método FlushCache NAP, interfaz INapSystemHealthAgentBinding
- Interfaz INapSystemHealthAgentBinding NAP, método FlushCache
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
ms.openlocfilehash: 5ead6e496d220619439b80fdc5c7601675fdb7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676553"
---
# <a name="inapsystemhealthagentbindingflushcache-method"></a>INapSystemHealthAgentBinding:: FlushCache (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Un SHA llama al método **INapSystemHealthAgentBinding:: FlushCache** para vaciar su caché de SOH.

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
| <dl> <dt>**S \_ Aceptar**</dt> </dl>               | Operación realizada correctamente.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>     | Error de permisos, acceso denegado.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>      | Límite de recursos del sistema, no se pudo realizar la operación.<br/>                                                             |
| <dl> <dt>**RPC \_ E \_ desconectado**</dt> </dl> | NapAgent se ha detenido. Este objeto se recuperará automáticamente y se volverá a enlazar a NapAgent, una vez que se reinicie.<br/> |



 

## <a name="remarks"></a>Observaciones

NapAgent mantiene una memoria caché de SOH recientes proporcionadas por diferentes Sha. Esta caché es útil para optimizar el rendimiento en tiempo de arranque, cuando se puede enlazar Sha o no al sistema.

SHA debe llamar a [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) antes de llamar a este método o a cualquier otro método de la interfaz [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





