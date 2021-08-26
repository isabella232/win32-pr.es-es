---
title: Método ITsSbResourcePluginStoreEx ReleaseTargetLock
description: Libera un bloqueo en un destino.
ms.assetid: ab2ae9f3-2d38-4b31-9889-58297c574bd4
ms.tgt_platform: multiple
keywords:
- Método ReleaseTargetLock Servicios de Escritorio remoto
- Método ReleaseTargetLock Servicios de Escritorio remoto , interfaz ITsSbResourcePluginStoreEx
- Interfaz ITsSbResourcePluginStoreEx Servicios de Escritorio remoto , método ReleaseTargetLock
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.ReleaseTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7fbe40d0fc7a28697d0e2fa9727f9e844eb39759db0dddf02c1d9e01bd843c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989915"
---
# <a name="itssbresourcepluginstoreexreleasetargetlock-method"></a>Método ITsSbResourcePluginStoreEx::ReleaseTargetLock

Libera un bloqueo en un destino.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReleaseTargetLock(
  [in] IUnknown *pContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContext* \[ En\]
</dt> <dd>

Puntero al contexto devuelto por el [**método AcquireTargetLock.**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Este método solo está disponible en Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) instalado en la [**interfaz ITsSbResourcePluginStoreEx.**](itssbresourcepluginstoreex.md) Este método está disponible en la [**interfaz ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) a partir de Windows Server 2016.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                             |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2012 R2<br/>                                                             |
| Idl<br/>                      | <dl> <dt>SbTsV.idl</dt> </dl>          |
| IID<br/>                      | IID \_ ITsSbResourcePluginStoreEx se define como 80b83ffd-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





