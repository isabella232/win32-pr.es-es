---
title: IRemoteDesktopClientEvents OnNetworkStatusChanged, método
description: Se llama cuando el estado de la red ha cambiado. | IRemoteDesktopClientEvents OnNetworkStatusChanged, método
ms.assetid: B68D1AA0-6403-40CA-95C5-BBBF39CEFFD8
ms.tgt_platform: multiple
keywords:
- Método OnNetworkStatusChanged Servicios de Escritorio remoto
- Método OnNetworkStatusChanged Servicios de Escritorio remoto, interfaz IRemoteDesktopClientEvents
- Interfaz IRemoteDesktopClientEvents Servicios de Escritorio remoto, método OnNetworkStatusChanged
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
ms.openlocfilehash: de64d8b16ea9acf9defc976d4baa91afd64f8fa7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547574"
---
# <a name="iremotedesktopclienteventsonnetworkstatuschanged-method"></a>IRemoteDesktopClientEvents:: OnNetworkStatusChanged (método)

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

*qualityLevel* \[ de\]
</dt> <dd>

Nuevo nivel de calidad de la conexión. El nivel de calidad se determina a partir de los valores de ancho de banda y de tiempo de ida y vuelta (RTT).

Uno de los siguientes valores.



| Valor                                                                        | Significado                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | No se pudo determinar el nivel de calidad.<br/>       |
| <dl> <dt>1</dt> </dl> | La calidad de la conexión es deficiente (una barra).<br/>        |
| <dl> <dt>2</dt> </dl> | La calidad de la conexión es justa (dos barras).<br/>       |
| <dl> <dt>3</dt> </dl> | La calidad de la conexión es buena (tres barras).<br/>     |
| <dl> <dt>4</dt> </dl> | La calidad de la conexión es excelente (cuatro barras).<br/> |



 

</dd> <dt>

*ancho de banda* \[ de\]
</dt> <dd>

Especifica el nuevo ancho de banda de conexión, en kilobits por segundo (kbps).

</dd> <dt>

*RTT* \[ de\]
</dt> <dd>

Especifica el nuevo tiempo de ida y vuelta (latencia) de la conexión, en milisegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





