---
title: Propiedad GatewayCredSourceCookie de IMsRdpClientTransportSettings3
description: Especifica si el origen de credenciales está basado en cookies.
ms.assetid: 039459a3-7a83-444c-a0b4-46ef0dc5ddd0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayCredSourceCookie
- Propiedad GatewayCredSourceCookie Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings3, propiedad GatewayCredSourceCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.get_GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.put_GatewayCredSourceCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9547df10ce9f528a4b52c526c970a82d0bd098c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676959"
---
# <a name="imsrdpclienttransportsettings3gatewaycredsourcecookie-property"></a>IMsRdpClientTransportSettings3:: GatewayCredSourceCookie (propiedad)

Especifica si el origen de credenciales está basado en cookies. Contiene una si el origen de la credencial está basado en cookies o cero de lo contrario.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_GatewayCredSourceCookie(
  [in]          ULONG ulProxyCredSourceCookie
);

HRESULT get_GatewayCredSourceCookie(
  [out, retval] ULONG *pulProxyCredSourceCookie
);
```



## <a name="property-value"></a>Valor de propiedad

Valor **ULong** que especifica si el origen de credenciales está basado en cookies.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





