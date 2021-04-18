---
title: Método CheckStatus de la clase Win32_TSGatewayConnection
description: Comprueba el estado de una conexión de servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) con otro equipo y determina si el equipo de destino está configurado para el equilibrio de carga.
ms.assetid: e8ee3d40-76eb-401f-b255-bccd7ba8c058
ms.tgt_platform: multiple
keywords:
- Método CheckStatus Servicios de Escritorio remoto
- Método CheckStatus Servicios de Escritorio remoto, clase Win32_TSGatewayConnection
- Win32_TSGatewayConnection de clase Servicios de Escritorio remoto, método CheckStatus
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685906"
---
# <a name="checkstatus-method-of-the-win32_tsgatewayconnection-class"></a>Método CheckStatus de la \_ clase TSGatewayConnection de Win32

Comprueba el estado de una conexión de servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) con otro equipo y determina si el equipo de destino está configurado para el equilibrio de carga.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CheckStatus(
  [in] string ServerName,
  [in] string EndPointName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NombreDeServidor* \[ de\]
</dt> <dd>

Nombre del servidor de puerta de enlace de escritorio remoto de origen desde el que se comprueba la conexión.

</dd> <dt>

*EndPointName* \[ de\]
</dt> <dd>

Nombre del servidor de destino (el punto de conexión) al que se comprueba el acceso desde el servidor de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores devueltos posibles.

<dl> <dt>


</dt> <dd>

0

El estado de la conexión es correcto. El punto de conexión es accesible y está configurado para el equilibrio de carga.

</dd> <dt>


</dt> <dd>

1

Se desconoce el estado de la conexión. Lo más probable es que se produzca una excepción.

</dd> <dt>


</dt> <dd>

0x80075c34

No se puede tener acceso al punto de conexión o no está configurado para el equilibrio de carga.

</dd> <dt>


</dt> <dd>

0x80075c32

Se produjo un error de estado. El extremo es accesible, pero el servicio de equilibrio de carga de RPC/HTTP (RPCHTTPLBS) no se ha iniciado en el equipo de destino.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> </dl>

 

