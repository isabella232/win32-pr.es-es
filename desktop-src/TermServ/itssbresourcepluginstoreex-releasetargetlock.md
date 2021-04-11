---
title: ITsSbResourcePluginStoreEx ReleaseTargetLock, método
description: Libera un bloqueo en un destino.
ms.assetid: ab2ae9f3-2d38-4b31-9889-58297c574bd4
ms.tgt_platform: multiple
keywords:
- Método ReleaseTargetLock Servicios de Escritorio remoto
- Método ReleaseTargetLock Servicios de Escritorio remoto, interfaz ITsSbResourcePluginStoreEx
- Interfaz ITsSbResourcePluginStoreEx Servicios de Escritorio remoto, método ReleaseTargetLock
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
ms.openlocfilehash: 8fbc34bdb27e40316ea1271bf0faa5d8c6b0abfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150492"
---
# <a name="itssbresourcepluginstoreexreleasetargetlock-method"></a>ITsSbResourcePluginStoreEx:: ReleaseTargetLock (método)

Libera un bloqueo en un destino.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReleaseTargetLock(
  [in] IUnknown *pContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContext* \[ de\]
</dt> <dd>

Un puntero al contexto devuelto por el método [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método solo está disponible en Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) instalado en la interfaz [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) . Este método está disponible en la interfaz [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) a partir de Windows Server 2016.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                             |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2012 R2<br/>                                                             |
| IDL<br/>                      | <dl> <dt>SbTsV. idl</dt> </dl>          |
| IID<br/>                      | IID \_ ITsSbResourcePluginStoreEx se define como 80b83ffd-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





