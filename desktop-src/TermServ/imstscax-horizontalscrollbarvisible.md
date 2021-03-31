---
title: Propiedad HorizontalScrollBarVisible de IMsTscAx
description: Indica si el control ha mostrado una barra de desplazamiento horizontal.
ms.assetid: d3c22c5f-321f-476e-bcdb-224eb988a7bb
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsTscAx
- Servicios de Escritorio remoto de la interfaz IMsTscAx, propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad HorizontalScrollBarVisible
topic_type:
- apiref
api_name:
- IMsTscAx.HorizontalScrollBarVisible
- IMsTscAx.get_HorizontalScrollBarVisible
- IMsRdpClient.HorizontalScrollBarVisible
- IMsRdpClient.get_HorizontalScrollBarVisible
- IMsRdpClient2.HorizontalScrollBarVisible
- IMsRdpClient2.get_HorizontalScrollBarVisible
- IMsRdpClient3.HorizontalScrollBarVisible
- IMsRdpClient3.get_HorizontalScrollBarVisible
- IMsRdpClient4.HorizontalScrollBarVisible
- IMsRdpClient4.get_HorizontalScrollBarVisible
- IMsRdpClient5.HorizontalScrollBarVisible
- IMsRdpClient5.get_HorizontalScrollBarVisible
- IMsRdpClient6.HorizontalScrollBarVisible
- IMsRdpClient6.get_HorizontalScrollBarVisible
- IMsRdpClient7.HorizontalScrollBarVisible
- IMsRdpClient7.get_HorizontalScrollBarVisible
- IMsRdpClient8.HorizontalScrollBarVisible
- IMsRdpClient8.get_HorizontalScrollBarVisible
- IMsRdpClient9.HorizontalScrollBarVisible
- IMsRdpClient9.get_HorizontalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08fa2abb97a28af013e5791bcbd643f3f479d5c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079298"
---
# <a name="imstscaxhorizontalscrollbarvisible-property"></a>IMsTscAx:: HorizontalScrollBarVisible (propiedad)

Indica si el control ha mostrado una barra de desplazamiento horizontal.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_HorizontalScrollBarVisible(
  [out] BOOL *pfHScrollVisible
);
```



## <a name="property-value"></a>Valor de propiedad

El valor de este parámetro es **true** si la barra de desplazamiento horizontal está visible y **false** en caso contrario.

## <a name="error-codes"></a>Códigos de error

Vuelva **a \_ Aceptar si es** correcto.

## <a name="remarks"></a>Observaciones

El control muestra automáticamente una barra de desplazamiento horizontal si el ancho del control es menor que el ancho del escritorio.

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



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

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)
</dt> </dl>

 

 





