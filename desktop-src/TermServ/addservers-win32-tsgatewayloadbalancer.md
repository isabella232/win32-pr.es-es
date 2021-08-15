---
title: Método AddServers de la Win32_TSGatewayLoadBalancer clase
description: Agrega servidores a los servidores de equilibrio de carga Escritorio remoto Gateway (Puerta de enlace de Escritorio remoto) en la propiedad Servidores.
ms.assetid: ffcbe14b-5ada-4951-bf51-95db14af41d7
ms.tgt_platform: multiple
keywords:
- Método AddServers Servicios de Escritorio remoto
- Método AddServers Servicios de Escritorio remoto , Win32_TSGatewayLoadBalancer clase
- Win32_TSGatewayLoadBalancer clase Servicios de Escritorio remoto , método AddServers
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
ms.openlocfilehash: 00bb232572c49b77f11de469f8e09fc536e73354f907d4070bc2281d42fc87fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117942273"
---
# <a name="addservers-method-of-the-win32_tsgatewayloadbalancer-class"></a>Método AddServers de la clase \_ TSGatewayLoadBalancer de Win32

Agrega servidores a los servidores de equilibrio de carga Escritorio remoto Gateway (puerta de enlace de Escritorio remoto) en la **propiedad** Servidores.

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

Lista separada por punto y coma de los servidores de equilibrio de carga de puerta de enlace de Escritorio remoto que se van a agregar a la **propiedad** Servidores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Si hay varios servidores en el *parámetro Servidores* y uno de los servidores no se puede procesar, no se procesará ninguno de los servidores.

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

