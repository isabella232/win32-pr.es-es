---
title: MDM_WindowsAdvancedThreatProtection (clase)
description: La \_ clase WindowsAdvancedThreatProtection de MDM se usa para incorporar puntos de conexión y externalización para la protección contra amenazas avanzada de Windows Defender (WDATP).
ms.assetid: 7a95253e-6d13-4c1b-b78d-c56c6378f7c3
keywords:
- MDM_WindowsAdvancedThreatProtection (clase)
- MDM_WindowsAdvancedThreatProtection clase, descrita
topic_type:
- apiref
api_name:
- MDM_WindowsAdvancedThreatProtection
- MDM_WindowsAdvancedThreatProtection.InstanceID
- MDM_WindowsAdvancedThreatProtection.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c369406a3c8bcf982aeb18b4bbb53c1af4983e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658271"
---
# <a name="mdm_windowsadvancedthreatprotection-class"></a>\_Clase WindowsAdvancedThreatProtection de MDM

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La **clase \_ WindowsAdvancedThreatProtection de MDM** se usa para incorporar puntos de conexión y externalización para la protección contra amenazas avanzada de Windows Defender (WDATP).

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection
{
  string InstanceID;
  string ParentID;
  string Onboarding;
  string Offboarding;
};
```

## <a name="members"></a>Miembros

La **clase \_ WindowsAdvancedThreatProtection de MDM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ WindowsAdvancedThreatProtection de MDM** tiene estas propiedades.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica el nombre del nodo primario. Para esta clase, la cadena es "WindowsAdvancedThreatProtection".

</dd> <dt>

[Retirada](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#offboarding)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

[Incorporación](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#onboarding)
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

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/".

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                            |
| Espacio de nombres<br/>                | Dmmap de MDM raíz de \\ cimv2 \\ \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl>      |
| Archivo DLL<br/>                      | <dl> <dt>\\DMWmiBridgeProv.dllMOF</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar scripting de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

