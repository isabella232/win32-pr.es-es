---
title: MDM_VPNv2_DomainNameInformationList02_01 (clase)
description: La \_ clase VPNv2 \_ DomainNameInformationList02 \_ 01 de MDM describe las reglas de la tabla de directivas de resolución de nombres (NRPT) para el perfil de VPN.
ms.assetid: ed6863aa-f85e-4f65-9312-ddf60a8c0d5a
keywords:
- MDM_VPNv2_DomainNameInformationList02_01 (clase)
- MDM_VPNv2_DomainNameInformationList02_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_DomainNameInformationList02_01
- MDM_VPNv2_DomainNameInformationList02_01.InstanceID
- MDM_VPNv2_DomainNameInformationList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec2fa2b6fd4216256a085caa23333bccc5f386d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996956"
---
# <a name="mdm_vpnv2_domainnameinformationlist02_01-class"></a>\_Clase VPNv2 \_ DomainNameInformationList02 \_ 01 de MDM

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La **clase \_ VPNv2 \_ DomainNameInformationList02 \_ 01 de MDM** describe las reglas de la tabla de directivas de resolución de nombres (NRPT) para el perfil de VPN.

La tabla de directivas de resolución de nombres (NRPT) es una tabla de espacios de nombres y la configuración correspondiente almacenada en el registro de Windows que determina el comportamiento del cliente DNS cuando se emiten consultas y procesan respuestas. Cada fila de la tabla NRPT representa una regla para una parte del espacio de nombres para la que el cliente DNS emite consultas. Antes de emitir consultas de resolución de nombres, el cliente DNS consulta la NRPT para determinar si se debe establecer alguna marca adicional en la consulta. Después de recibir la respuesta, el cliente consulta de nuevo la tabla NRPT para comprobar si hay algún requisito de procesamiento o Directiva especial. En ausencia de la NRPT, el cliente opera en función de los servidores DNS y los sufijos establecidos en la interfaz.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_DomainNameInformationList02_01
{
  string InstanceID;
  string ParentID;
  string DomainName;
  string DomainNameType;
  string DnsServers;
  string WebProxyServers;
};
```

## <a name="members"></a>Miembros

La **clase \_ VPNv2 \_ DomainNameInformationList02 \_ 01 de MDM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ VPNv2 \_ DomainNameInformationList02 \_ 01 de MDM** tiene estas propiedades.

<dl> <dt>

[DnsServers](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-dnsservers)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

[DomainName](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainname)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

[DomainNameType](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainnametype)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
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

Identifica el nombre del nodo primario.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*"

</dd> <dt>

[WebProxyServers](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-webproxyservers)
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

 

