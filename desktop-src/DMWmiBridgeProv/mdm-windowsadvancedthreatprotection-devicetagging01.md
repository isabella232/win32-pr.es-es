---
title: MDM_WindowsAdvancedThreatProtection_DeviceTagging01 clase
description: La clase \_ MDM WindowsAdvancedThreatProtection DeviceTagging01 se usa para incorporar, determinar el estado de configuración y estado de mantenimiento y los puntos de conexión externos para \_ Windows Defender Advanced Threat Protection.
ms.assetid: b56d5d46-e994-404a-865a-c59bb948f2b3
keywords:
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01 clase
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01 clase, descrita
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.InstanceID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.ParentID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.IdMethod
api_type:
- DllExport
api_location:
- DMWmiBridgeProv.dll
ms.openlocfilehash: f095c39c78400f5d040ff00ab668f51c7d7abfaac2b0d872ed860f768ea55404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913415"
---
# <a name="mdm_windowsadvancedthreatprotection_devicetagging01-class"></a>Mdm \_ WindowsAdvancedThreatProtection \_ DeviceTagging01 (clase)

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

La clase \_ MDM WindowsAdvancedThreatProtection DeviceTagging01 se usa para incorporar, determinar el estado de configuración y estado de mantenimiento y los puntos de conexión externos para \_ Windows Defender Advanced Threat Protection.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_DeviceTagging01
{
  string InstanceID;
  string ParentID;
  string Group;
  sint32 Criticality;
  sint32 IdMethod;
};
```

## <a name="members"></a>Miembros

La **clase \_ MDM WindowsAdvancedThreatProtection \_ DeviceTagging01** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ MDM WindowsAdvancedThreatProtection \_ DeviceTagging01** tiene estas propiedades.

<dl> <dt>

[Grado de importancia](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#criticality)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[Grupo](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#group)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

**IdMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Por determinar

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                     |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                       |
| Espacio de nombres<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



 

