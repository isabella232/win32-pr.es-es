---
title: Propiedad IMsRdpClientAdvancedSettings6 ConnectToAdminadminserver
description: Recupera o especifica si el control ActiveX debe intentar conectarse al servidor con fines administrativos.
ms.assetid: b98f9b9b-a3e7-4a3c-a7e3-e388ce53c5c9
ms.tgt_platform: multiple
keywords:
- Propiedad ConnectToAdminadminserver Servicios de Escritorio remoto
- Propiedad ConnectToAdminadminserver Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings6
- Interfaz IMsRdpClientAdvancedSettings6 Servicios de Escritorio remoto , propiedad ConnectToAdminadminserver
- Propiedad ConnectToAdminadminserver Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings7
- Interfaz IMsRdpClientAdvancedSettings7 Servicios de Escritorio remoto , propiedad ConnectToAdminadminserver
- Propiedad ConnectToAdminadminserver Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings8
- Interfaz IMsRdpClientAdvancedSettings8 Servicios de Escritorio remoto , propiedad ConnectToAdminadminserver
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.put_ConnectToAdministerServer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1df4327a263f5bc77fa482e3f84bb971cd5fb047a7c2fed7c1092efdd4d06f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771675"
---
# <a name="imsrdpclientadvancedsettings6connecttoadministerserver-property"></a>IMsRdpClientAdvancedSettings6::ConnectToAdminadminserver, propiedad

Recupera o especifica si el control ActiveX debe intentar conectarse al servidor con fines administrativos.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ConnectToAdministerServer(
  [in]  VARIANT_BOOL connectToAdministerServer
);

HRESULT get_ConnectToAdministerServer(
  [out] VARIANT_BOOL *pConnectToAdministerServer
);
```



## <a name="property-value"></a>Valor de propiedad

**VARIANT \_ TRUE** para hacer que el control ActiveX intente conectarse al servidor con fines administrativos; en caso **contrario, VARIANT \_ FALSE**. El valor predeterminado es **VARIANT \_ FALSE.**

## <a name="remarks"></a>Comentarios

Para usar **ConnectToAdminadminserver,** debe ejecutar la versión 6.1 del cliente Conexión a Escritorio remoto (RDC) o posterior.

> [!Note]  
> RDC versión 6.1 (6.0.6001) admite Protocolo de escritorio remoto 6.1. RDC 6.1 se incluye con Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).

 

**ConnectToAdminadmin** se conecta a una sesión que se usa con fines administrativos en el servidor remoto. Si el Escritorio remoto de rol host de sesión de Escritorio remoto está instalado en el servidor remoto, **ConnectToAdminadminserver** hace lo siguiente:

-   Deshabilita Servicios de Escritorio remoto licencias de acceso de cliente para la sesión.
-   Deshabilita el redireccionamiento de zona horaria para la sesión.
-   Deshabilita la Conexión a Escritorio remoto broker (Agente de conexión a Escritorio remoto) para la sesión.
-   Deshabilita Plug and Play redireccionamiento de dispositivos para la sesión.
-   Cambia el tema de sesión remota a Windows clásico para la sesión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 se define como 222c4b5d-45d9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





