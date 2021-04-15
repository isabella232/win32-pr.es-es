---
title: IMsTscAxEvents OnRemoteDesktopSizeChange, método
description: Se llama para indicar que el tamaño del control de cliente en el escritorio remoto ha cambiado en respuesta a una operación de control de cliente.
ms.assetid: 6d27aec0-7249-4aac-8755-186815b50be7
ms.tgt_platform: multiple
keywords:
- Método OnRemoteDesktopSizeChange Servicios de Escritorio remoto
- Método OnRemoteDesktopSizeChange Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnRemoteDesktopSizeChange
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteDesktopSizeChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aee74049ea726b4e2686a028359afe01d2d7632
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534438"
---
# <a name="imstscaxeventsonremotedesktopsizechange-method"></a>IMsTscAxEvents:: OnRemoteDesktopSizeChange (método)

Se llama para indicar que el tamaño del control de cliente en el escritorio remoto ha cambiado en respuesta a una operación de control de cliente.

## <a name="syntax"></a>Sintaxis


```C++
void OnRemoteDesktopSizeChange(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ancho* \[ de de\]
</dt> <dd>

Ancho, en píxeles, del escritorio remoto cuyo tamaño se ha cambiado.

</dd> <dt>

*alto* \[ de de\]
</dt> <dd>

Alto, en píxeles, del escritorio remoto cuyo tamaño se ha cambiado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este evento permite al contenedor determinar si debe cambiar su tamaño en respuesta a una operación de control de cliente, lo que podría dar lugar a un mayor tamaño de escritorio visible. Tenga en cuenta que el control ajustará automáticamente las barras de desplazamiento para el nuevo tamaño de la sesión.

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





