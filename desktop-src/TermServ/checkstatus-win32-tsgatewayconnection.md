---
title: Método CheckStatus de la Win32_TSGatewayConnection clase
description: Comprueba el estado de una conexión de servidor Escritorio remoto Gateway (Puerta de enlace de Escritorio remoto) a otro equipo y determina si el equipo de destino está configurado para el equilibrio de carga.
ms.assetid: e8ee3d40-76eb-401f-b255-bccd7ba8c058
ms.tgt_platform: multiple
keywords:
- Método CheckStatus Servicios de Escritorio remoto
- Método CheckStatus Servicios de Escritorio remoto , Win32_TSGatewayConnection clase
- Win32_TSGatewayConnection clase Servicios de Escritorio remoto , método CheckStatus
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.CheckStatus
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babb083af5c0581abe27d442a466c3d6114b957a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168806"
---
# <a name="checkstatus-method-of-the-win32_tsgatewayconnection-class"></a>Método CheckStatus de la clase \_ TSGatewayConnection de Win32

Comprueba el estado de una conexión de servidor Escritorio remoto Gateway (Puerta de enlace de Escritorio remoto) a otro equipo y determina si el equipo de destino está configurado para el equilibrio de carga.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CheckStatus(
  [in] string ServerName,
  [in] string EndPointName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ServerName* \[ En\]
</dt> <dd>

Nombre del servidor de puerta de enlace de Escritorio remoto de origen desde el que se comprueba la conexión.

</dd> <dt>

*EndPointName* \[ En\]
</dt> <dd>

Nombre del servidor de destino (el punto de conexión) al que se comprueba el acceso desde el servidor de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores devueltos posibles.

<dl> <dt>


</dt> <dd>

0

El estado de la conexión es Correcto. El punto de conexión es accesible y está configurado para el equilibrio de carga.

</dd> <dt>


</dt> <dd>

1

Se desconoce el estado de conexión. Lo más probable es que se haya producido una excepción.

</dd> <dt>


</dt> <dd>

0x80075c34

El punto de conexión no es accesible o no está configurado para el equilibrio de carga.

</dd> <dt>


</dt> <dd>

0x80075c32

Error de estado. El punto de conexión es accesible, pero el servicio RPC/HTTP Load Balancing Service (RPCHTTPLBS) no se inicia en el equipo de destino.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSGatewayConnection de Win32 \_**](win32-tsgatewayconnection.md)
</dt> </dl>

 

