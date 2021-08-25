---
title: Propiedad IMsTscAx VerticalScrollBarVisible
description: Indica si el control muestra una barra de desplazamiento vertical.
ms.assetid: b31e2db3-b367-4900-a2c6-51fd794341c2
ms.tgt_platform: multiple
keywords:
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto , interfaz IMsTscAx
- Interfaz IMsTscAx Servicios de Escritorio remoto , propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto , interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto , propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto , interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto , propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto , interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto , propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto , interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto , propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto , interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto , propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto , interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto , propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto , interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto , propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto , interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto , propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto , interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto , propiedad VerticalScrollBarVisible
topic_type:
- apiref
api_name:
- IMsTscAx.VerticalScrollBarVisible
- IMsTscAx.get_VerticalScrollBarVisible
- IMsRdpClient.VerticalScrollBarVisible
- IMsRdpClient.get_VerticalScrollBarVisible
- IMsRdpClient2.VerticalScrollBarVisible
- IMsRdpClient2.get_VerticalScrollBarVisible
- IMsRdpClient3.VerticalScrollBarVisible
- IMsRdpClient3.get_VerticalScrollBarVisible
- IMsRdpClient4.VerticalScrollBarVisible
- IMsRdpClient4.get_VerticalScrollBarVisible
- IMsRdpClient5.VerticalScrollBarVisible
- IMsRdpClient5.get_VerticalScrollBarVisible
- IMsRdpClient6.VerticalScrollBarVisible
- IMsRdpClient6.get_VerticalScrollBarVisible
- IMsRdpClient7.VerticalScrollBarVisible
- IMsRdpClient7.get_VerticalScrollBarVisible
- IMsRdpClient8.VerticalScrollBarVisible
- IMsRdpClient8.get_VerticalScrollBarVisible
- IMsRdpClient9.VerticalScrollBarVisible
- IMsRdpClient9.get_VerticalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b09cf6c50c4724cc7374163998af7b7bab77d61f4c16177fedddcc9b1e8de055
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125265"
---
# <a name="imstscaxverticalscrollbarvisible-property"></a>Propiedad IMsTscAx::VerticalScrollBarVisible

Indica si el control muestra una barra de desplazamiento vertical.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_VerticalScrollBarVisible(
  [out] BOOL *pfVScrollVisible
);
```



## <a name="property-value"></a>Valor de propiedad

El valor de este parámetro es **TRUE si** la barra de desplazamiento vertical está visible y **FALSE** en caso contrario.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

El control muestra automáticamente una barra de desplazamiento vertical si el alto del control actual es menor que el alto del escritorio.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID IMsTscAx se define como \_ 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





