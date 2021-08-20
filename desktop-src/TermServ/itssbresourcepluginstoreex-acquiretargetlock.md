---
title: Método ITsSbResourcePluginStoreEx AcquireTargetLock
description: Bloquea un destino.
ms.assetid: 76707f1d-1f13-4d81-8954-2acf05cda2cd
ms.tgt_platform: multiple
keywords:
- Método AcquireTargetLock Servicios de Escritorio remoto
- Método AcquireTargetLock Servicios de Escritorio remoto , interfaz ITsSbResourcePluginStoreEx
- Interfaz ITsSbResourcePluginStoreEx Servicios de Escritorio remoto método AcquireTargetLock
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
ms.openlocfilehash: f80a2ab7068ec754a89e384028f2d43989345e9801c4ededb800117d211b0f8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128462"
---
# <a name="itssbresourcepluginstoreexacquiretargetlock-method"></a>Método ITsSbResourcePluginStoreEx::AcquireTargetLock

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

*targetName* \[ En\]
</dt> <dd>

Nombre del destino que se bloqueará.

</dd> <dt>

*dwTimeout* \[ En\]
</dt> <dd>

Tiempo de espera de la operación, en milisegundos.

</dd> <dt>

*ppContext* \[ out\]
</dt> <dd>

Devuelve un puntero al contexto del bloqueo. Para liberar el bloqueo, proporcione este puntero al [**método ReleaseTargetLock.**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Una vez adquirido el bloqueo, se supone que el subproceso que realiza la llamada tiene acceso exclusivo al objeto de destino y, por tanto, ningún otro subproceso (dentro de la misma máquina) puede actualizarlo. Por lo tanto, el subproceso que realiza la llamada debe llamar [**al método ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) en cuanto haya realizado las actualizaciones necesarias en el objeto de destino.

> [!IMPORTANT]
> Este bloqueo no impide completamente que los objetos de destino se modifiquen externamente si hay más de un agente de conexión en la implementación. El subproceso de llamada debe estar preparado para controlar correctamente un error y volver a intentar la actualización de destino.

 

Este método está disponible en Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) instalado en la [**interfaz ITsSbResourcePluginStoreEx.**](itssbresourcepluginstoreex.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





