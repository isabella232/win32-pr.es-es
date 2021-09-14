---
title: Método AddServers de la Win32_TSGatewayLoadBalancer clase
description: Agrega servidores a los servidores de equilibrio de carga Escritorio remoto Gateway (Puerta de enlace de Escritorio remoto) en la propiedad Servidores .
ms.assetid: ffcbe14b-5ada-4951-bf51-95db14af41d7
ms.tgt_platform: multiple
keywords:
- Método AddServers Servicios de Escritorio remoto
- Método AddServers Servicios de Escritorio remoto , Win32_TSGatewayLoadBalancer clase
- Win32_TSGatewayLoadBalancer clase Servicios de Escritorio remoto método , AddServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.AddServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a510fd6ecee12b5251ec84773327d6217463240f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168818"
---
# <a name="addservers-method-of-the-win32_tsgatewayloadbalancer-class"></a>Método AddServers de la clase \_ TSGatewayLoadBalancer de Win32

Agrega servidores a los servidores de equilibrio de carga Escritorio remoto Gateway (Puerta de enlace de Escritorio remoto) en la **propiedad** Servidores.

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddServers(
  [in] string Servers
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Servidores* \[ En\]
</dt> <dd>

Lista separada por punto y coma de servidores de equilibrio de carga de puerta de enlace de Escritorio remoto que se van a agregar a la **propiedad** Servidores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Observaciones

Si hay varios servidores en el *parámetro Servidores* y no se puede procesar uno de ellos, no se procesará ninguno de los servidores.

Debe ser miembro del grupo Administradores para llamar a este método.

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

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

