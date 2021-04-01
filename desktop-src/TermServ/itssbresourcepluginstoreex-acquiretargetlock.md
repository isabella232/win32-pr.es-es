---
title: ITsSbResourcePluginStoreEx AcquireTargetLock, método
description: Bloquea un destino.
ms.assetid: 76707f1d-1f13-4d81-8954-2acf05cda2cd
ms.tgt_platform: multiple
keywords:
- Método AcquireTargetLock Servicios de Escritorio remoto
- Método AcquireTargetLock Servicios de Escritorio remoto, interfaz ITsSbResourcePluginStoreEx
- Interfaz ITsSbResourcePluginStoreEx Servicios de Escritorio remoto, método AcquireTargetLock
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.AcquireTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c18be0a544ebcea2d2cecb40dcea3a08e4bd35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150031"
---
# <a name="itssbresourcepluginstoreexacquiretargetlock-method"></a>ITsSbResourcePluginStoreEx:: AcquireTargetLock (método)

Bloquea un destino.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AcquireTargetLock(
  [in]  BSTR     targetName,
  [in]  DWORD    dwTimeout,
  [out] IUnknown **ppContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*targetName* \[ de\]
</dt> <dd>

Nombre del destino que se va a bloquear.

</dd> <dt>

*dwTimeout* \[ de\]
</dt> <dd>

Tiempo de espera de la operación, en milisegundos.

</dd> <dt>

*ppContext* \[ enuncia\]
</dt> <dd>

Devuelve un puntero al contexto del bloqueo. Para liberar el bloqueo, suministre este puntero al método [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Una vez adquirido el bloqueo, se supone que el subproceso que realiza la llamada tiene acceso exclusivo al objeto de destino y, por tanto, ningún otro subproceso (dentro del mismo equipo) puede actualizarlo. Por lo tanto, el subproceso que realiza la llamada debe llamar al método [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) en cuanto haya realizado las actualizaciones necesarias en el objeto de destino.

> [!IMPORTANT]
> Este bloqueo no impide que los objetos de destino se modifiquen externamente si existe más de un agente de conexión en la implementación. El subproceso de llamada debe estar preparado para controlar un error correctamente y reintentar la actualización del destino.

 

Este método está disponible en Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) instalado en la interfaz [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) .

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

 

 





