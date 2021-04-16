---
title: Propiedad StartConnected de IMsTscAx
description: Indica si el control establecerá la conexión del servidor de host de sesión Escritorio remoto de escritorio remoto (host de sesión de RD) inmediatamente al iniciar.
ms.assetid: cf2956c0-be4f-4f80-a14b-253ae8117824
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsTscAx
- Servicios de Escritorio remoto de la interfaz IMsTscAx, propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad StartConnected
topic_type:
- apiref
api_name:
- IMsTscAx.StartConnected
- IMsTscAx.get_StartConnected
- IMsTscAx.put_StartConnected
- IMsRdpClient.StartConnected
- IMsRdpClient.get_StartConnected
- IMsRdpClient.put_StartConnected
- IMsRdpClient2.StartConnected
- IMsRdpClient2.get_StartConnected
- IMsRdpClient2.put_StartConnected
- IMsRdpClient3.StartConnected
- IMsRdpClient3.get_StartConnected
- IMsRdpClient3.put_StartConnected
- IMsRdpClient4.StartConnected
- IMsRdpClient4.get_StartConnected
- IMsRdpClient4.put_StartConnected
- IMsRdpClient5.StartConnected
- IMsRdpClient5.get_StartConnected
- IMsRdpClient5.put_StartConnected
- IMsRdpClient6.StartConnected
- IMsRdpClient6.get_StartConnected
- IMsRdpClient6.put_StartConnected
- IMsRdpClient7.StartConnected
- IMsRdpClient7.get_StartConnected
- IMsRdpClient7.put_StartConnected
- IMsRdpClient8.StartConnected
- IMsRdpClient8.get_StartConnected
- IMsRdpClient8.put_StartConnected
- IMsRdpClient9.StartConnected
- IMsRdpClient9.get_StartConnected
- IMsRdpClient9.put_StartConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bda77a06723a6df63055374a3fc96cb80f7654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676595"
---
# <a name="imstscaxstartconnected-property"></a>IMsTscAx:: StartConnected (propiedad)

Indica si el control establecerá la conexión del servidor de host de sesión Escritorio remoto de escritorio remoto (host de sesión de RD) inmediatamente al iniciar.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_StartConnected(
  [in]  BOOL fStartConnected
);

HRESULT get_StartConnected(
  [out] BOOL *pfStartConnected
);
```



## <a name="property-value"></a>Valor de propiedad

Establezca este parámetro en **true** si el control debe conectarse inmediatamente al iniciarse o **false** en caso contrario.

## <a name="error-codes"></a>Códigos de error

Vuelva **a \_ Aceptar si es** correcto.

## <a name="remarks"></a>Observaciones

Esta propiedad es muy útil cuando las propiedades del control se establecen en la lista de parámetros de una <OBJECT> etiqueta, en lugar de mediante llamadas de script.

Esta propiedad solo se puede usar si el nombre del servidor también se especifica mediante la propiedad del servidor. Este parámetro debe establecerse antes de que se inicie el control, por ejemplo, si se incluye en la lista de parámetros de una <OBJECT> etiqueta al usar el control de una página web.

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

[Incrustar el control ActiveX Escritorio remoto en una página web](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





