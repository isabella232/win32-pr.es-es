---
title: MDM_VPNv2_DeviceCompliance02 (clase)
description: Reservado para uso futuro. | MDM_VPNv2_DeviceCompliance02 (clase)
ms.assetid: f84f4812-3083-46c4-a60c-919ec92c844f
keywords:
- MDM_VPNv2_DeviceCompliance02 (clase)
- MDM_VPNv2_DeviceCompliance02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_DeviceCompliance02
- MDM_VPNv2_DeviceCompliance02.InstanceID
- MDM_VPNv2_DeviceCompliance02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a454a5cce3a40066c7cf14a60bdeeb81dcabab9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105649359"
---
# <a name="mdm_vpnv2_devicecompliance02-class"></a>\_Clase DeviceCompliance02 VPNv2 de MDM \_

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Reservado para uso futuro

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_DeviceCompliance02
{
  string  InstanceID;
  string  ParentID;
  boolean Enabled;
};
```

## <a name="members"></a>Miembros

La **clase \_ \_ DeviceCompliance02 de MDM VPNv2** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ \_ DeviceCompliance02 de MDM VPNv2** tiene estas propiedades.

<dl> <dt>

[Enabled](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-enabled)
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Agregado en Windows 10, versión 1607. Los nodos de DeviceCompliance se pueden usar para habilitar el acceso condicional basado en AAD para VPN.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Agregado en Windows 10, versión 1607. Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*"

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | Dmmap de MDM raíz de \\ cimv2 \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar scripting de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

