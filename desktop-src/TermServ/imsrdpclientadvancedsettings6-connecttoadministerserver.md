---
title: Propiedad ConnectToAdministerServer de IMsRdpClientAdvancedSettings6
description: Recupera o especifica si el control ActiveX debe intentar conectarse al servidor con fines administrativos.
ms.assetid: b98f9b9b-a3e7-4a3c-a7e3-e388ce53c5c9
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ConnectToAdministerServer
- Propiedad ConnectToAdministerServer Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad ConnectToAdministerServer
- Propiedad ConnectToAdministerServer Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad ConnectToAdministerServer
- Propiedad ConnectToAdministerServer Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad ConnectToAdministerServer
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
ms.openlocfilehash: 4d9cad8d50e2e0a4c1ec18fbd33733dc394101a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079378"
---
# <a name="imsrdpclientadvancedsettings6connecttoadministerserver-property"></a>IMsRdpClientAdvancedSettings6:: ConnectToAdministerServer (propiedad)

Recupera o especifica si el control ActiveX debe intentar conectarse al servidor con fines administrativos.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_ConnectToAdministerServer(
  [in]  VARIANT_BOOL connectToAdministerServer
);

HRESULT get_ConnectToAdministerServer(
  [out] VARIANT_BOOL *pConnectToAdministerServer
);
```



## <a name="property-value"></a>Valor de propiedad

**Variante \_ TRUE** para hacer que el control ActiveX intente conectarse al servidor con fines administrativos; de lo contrario, **Variant \_ false**. El valor predeterminado es **Variant \_ false**.

## <a name="remarks"></a>Observaciones

Para usar **ConnectToAdministerServer**, debe ejecutar el cliente conexión A escritorio remoto (RDC) versión 6,1 o posterior.

> [!Note]  
> La versión de RDC 6,1 (6.0.6001) admite Protocolo de escritorio remoto 6,1. RDC 6,1 se incluye con Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).

 

**ConnectToAdministerServer** se conecta a una sesión que se usa con fines administrativos en el servidor remoto. Si el servicio de rol host de sesión de Escritorio remoto (host de sesión de escritorio remoto) está instalado en el servidor remoto, **ConnectToAdministerServer** hace lo siguiente:

-   Deshabilita la concesión de licencias de acceso de cliente de Servicios de Escritorio remoto para la sesión.
-   Deshabilita el redireccionamiento de zona horaria para la sesión.
-   Deshabilita el redireccionamiento de Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto) de la sesión.
-   Deshabilita la redirección de dispositivos Plug and Play para la sesión.
-   Cambia el tema de la sesión remota a Windows clásico para la sesión.

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

 

 





