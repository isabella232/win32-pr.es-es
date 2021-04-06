---
title: Método SetServers de la clase Win32_TSGatewayLoadBalancer
description: Establece la propiedad servidores con la lista de servidores de equilibrio de carga de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: c82de8e2-301b-465d-b375-038b8a480cde
ms.tgt_platform: multiple
keywords:
- Método SetServers Servicios de Escritorio remoto
- Método SetServers Servicios de Escritorio remoto, clase Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer de clase Servicios de Escritorio remoto, método SetServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.SetServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b28d1123ce82844fb501f3562014b93337502b51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802929"
---
# <a name="setservers-method-of-the-win32_tsgatewayloadbalancer-class"></a>Método SetServers de la \_ clase TSGatewayLoadBalancer de Win32

Establece la propiedad **servidores** con la lista de servidores de equilibrio de carga de puerta de enlace de escritorio remoto (puerta de enlace de escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetServers(
  [in] string Servers
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Servidores* \[ de de\]
</dt> <dd>

Lista separada por punto y coma de servidores de equilibrio de carga de puerta de enlace de escritorio remoto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Si hay varios servidores en el parámetro *Servers* y uno de ellos no se puede procesar, no se procesará ninguno de los servidores.

Para llamar a este método, debe ser miembro del grupo administradores.

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

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

