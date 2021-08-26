---
title: Método IMsTscAxEvents OnRemoteDesktopSizeChange
description: Se llama para indicar que el tamaño del control de cliente en el Escritorio remoto ha cambiado en respuesta a una operación de control de cliente.
ms.assetid: 6d27aec0-7249-4aac-8755-186815b50be7
ms.tgt_platform: multiple
keywords:
- Método OnRemoteDesktopSizeChange Servicios de Escritorio remoto
- Método OnRemoteDesktopSizeChange Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto , método OnRemoteDesktopSizeChange
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
ms.openlocfilehash: 316b70c3405c13dd50c773d36c20f036c9e99aebeb3e5dedae692c2f9ad772fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125095"
---
# <a name="imstscaxeventsonremotedesktopsizechange-method"></a>Método IMsTscAxEvents::OnRemoteDesktopSizeChange

Se llama para indicar que el tamaño del control de cliente en el Escritorio remoto ha cambiado en respuesta a una operación de control de cliente.

## <a name="syntax"></a>Sintaxis


```C++
void OnRemoteDesktopSizeChange(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*width* \[ En\]
</dt> <dd>

Ancho, en píxeles, del escritorio remoto con el tamaño cambiado.

</dd> <dt>

*alto* \[ En\]
</dt> <dd>

Alto, en píxeles, del escritorio remoto con el tamaño cambiado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este evento permite al contenedor determinar si debe cambiar su tamaño en respuesta a una operación de control de cliente, lo que podría dar lugar a un mayor tamaño de escritorio visualizable. Tenga en cuenta que el control ajustará automáticamente las barras de desplazamiento para el nuevo tamaño de sesión.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

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

 

 





