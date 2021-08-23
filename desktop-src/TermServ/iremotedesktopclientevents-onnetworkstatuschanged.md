---
title: Método IRemoteDesktopClientEvents OnNetworkStatusChanged
description: Se llama cuando el estado de la red ha cambiado. | Método IRemoteDesktopClientEvents OnNetworkStatusChanged
ms.assetid: B68D1AA0-6403-40CA-95C5-BBBF39CEFFD8
ms.tgt_platform: multiple
keywords:
- Método OnNetworkStatusChanged Servicios de Escritorio remoto
- Método OnNetworkStatusChanged Servicios de Escritorio remoto , interfaz IRemoteDesktopClientEvents
- Interfaz IRemoteDesktopClientEvents Servicios de Escritorio remoto método , OnNetworkStatusChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d14519f5da78a0d42b5bd7e52abf790c21406bfe20848235d2639beed2e215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515115"
---
# <a name="iremotedesktopclienteventsonnetworkstatuschanged-method"></a>IRemoteDesktopClientEvents::OnNetworkStatusChanged (método)

Se llama cuando el estado de la red ha cambiado.

## <a name="syntax"></a>Sintaxis


```C++
void OnNetworkStatusChanged(
  [in] unsigned long qualityLevel,
  [in] long          bandwidth,
  [in] long          rtt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*qualityLevel* \[ En\]
</dt> <dd>

Nuevo nivel de calidad de la conexión. El nivel de calidad se determina a partir de los valores de ancho de banda y tiempo de ida y vuelta (rtt).

Uno de los siguientes valores.



| Valor                                                                        | Significado                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | No se pudo determinar el nivel de calidad.<br/>       |
| <dl> <dt>1</dt> </dl> | La calidad de la conexión es deficiente (una barra).<br/>        |
| <dl> <dt>2</dt> </dl> | La calidad de la conexión es equitativa (dos barras).<br/>       |
| <dl> <dt>3</dt> </dl> | La calidad de la conexión es buena (tres barras).<br/>     |
| <dl> <dt>4</dt> </dl> | La calidad de la conexión es excelente (cuatro barras).<br/> |



 

</dd> <dt>

*ancho de banda* \[ En\]
</dt> <dd>

Especifica el nuevo ancho de banda de conexión, en kilobits por segundo (Kbps).

</dd> <dt>

*rtt* \[ En\]
</dt> <dd>

Especifica el nuevo tiempo de ida y vuelta (latencia) de la conexión, en milisegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                           |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents se define como 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





