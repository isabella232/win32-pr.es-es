---
title: Método IsLoadBalancingServer de la clase Win32_TSGatewayLoadBalancer
description: Determina si el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) puede realizar el equilibrio de carga.
ms.assetid: ae1a91c1-0b8b-4bd0-83f9-41c973247f27
ms.tgt_platform: multiple
keywords:
- Método IsLoadBalancingServer Servicios de Escritorio remoto
- Método IsLoadBalancingServer Servicios de Escritorio remoto, clase Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer de clase Servicios de Escritorio remoto, método IsLoadBalancingServer
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.IsLoadBalancingServer
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eae909df4074c8129a1b49eb0d5c3b336fed5d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686052"
---
# <a name="isloadbalancingserver-method-of-the-win32_tsgatewayloadbalancer-class"></a>Método IsLoadBalancingServer de la \_ clase TSGatewayLoadBalancer de Win32

Determina si el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) puede realizar el equilibrio de carga.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsLoadBalancingServer(
  [out] boolean LoadBalancing
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Equilibrio* \[ enuncia\]
</dt> <dd>

**True** si el servidor puede realizar el equilibrio de carga y **false** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

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

 

