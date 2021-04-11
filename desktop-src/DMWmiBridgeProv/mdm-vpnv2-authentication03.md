---
title: MDM_VPNv2_Authentication03 (clase)
description: La \_ \_ clase Authentication03 de VPNV2 de MDM contiene información de autenticación para el perfil de VPN nativo.
ms.assetid: 931752a9-6de5-46d4-b9d9-2c59c49e8ed9
keywords:
- MDM_VPNv2_Authentication03 (clase)
- MDM_VPNv2_Authentication03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_Authentication03
- MDM_VPNv2_Authentication03.InstanceID
- MDM_VPNv2_Authentication03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ca50bcc83df01b4aa5e7ec900985cf15f7e67d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079390"
---
# <a name="mdm_vpnv2_authentication03-class"></a>\_Clase Authentication03 VPNv2 de MDM \_

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La [**clase \_ \_ Authentication03 de VPNv2 de MDM**](mdm-vpnv2-01.md) contiene información de autenticación para el perfil de VPN nativo.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Authentication03
{
  string InstanceID;
  string ParentID;
  string UserMethod;
  string MachineMethod;
};
```

## <a name="members"></a>Miembros

La **clase \_ \_ Authentication03 de MDM VPNv2** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ \_ Authentication03 de MDM VPNv2** tiene estas propiedades.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica el nombre del nodo primario.

</dd> <dt>

[MachineMethod](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-machinemethod)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"

</dd> <dt>

[UserMethod](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-usermethod)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

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

 

