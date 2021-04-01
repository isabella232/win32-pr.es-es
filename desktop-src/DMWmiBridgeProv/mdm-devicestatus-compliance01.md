---
title: MDM_DeviceStatus_Compliance01 (clase)
description: La \_ \_ clase Compliance01 de DEVICESTATUS de MDM permite consultar si el dispositivo cumple con la Directiva de cifrado empresarial.
ms.assetid: 99c4cb9b-ae53-432c-b970-d61fb8496123
keywords:
- MDM_DeviceStatus_Compliance01 (clase)
- MDM_DeviceStatus_Compliance01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Compliance01
- MDM_DeviceStatus_Compliance01.InstanceID
- MDM_DeviceStatus_Compliance01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf606b7f10fbe7abc196622ee54b271e5285f2c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150728"
---
# <a name="mdm_devicestatus_compliance01-class"></a>\_Clase Compliance01 DeviceStatus de MDM \_

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La **clase \_ \_ Compliance01 de DeviceStatus de MDM** permite consultar si el dispositivo cumple con la Directiva de cifrado empresarial.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Compliance01
{
  string  InstanceID;
  string  ParentID;
  boolean EncryptionCompliance;
};
```

## <a name="members"></a>Miembros

La **clase \_ \_ Compliance01 de MDM DeviceStatus** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ \_ Compliance01 de MDM DeviceStatus** tiene estas propiedades.

<dl> <dt>

[EncryptionCompliance](/windows/client-management/mdm/devicestatus-csp#devicestatus-compliance-encryptioncompliance)
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

Nodo para consultas en cumplimiento.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/DeviceStatus".

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

 

