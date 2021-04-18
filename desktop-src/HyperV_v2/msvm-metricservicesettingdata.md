---
description: Representa la configuración para el servicio de métricas. Las propiedades de esta clase no se pueden modificar directamente. El cliente debe llamar al método ModifyServiceSettings para modificar cualquiera de estas propiedades.
ms.assetid: 578ddda7-4c8e-498e-8612-29c392390b73
title: Msvm_MetricServiceSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceSettingData
- Msvm_MetricServiceSettingData.InstanceID
- Msvm_MetricServiceSettingData.Caption
- Msvm_MetricServiceSettingData.Description
- Msvm_MetricServiceSettingData.ElementName
- Msvm_MetricServiceSettingData.MetricsFlushInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4a1211b19692761dd8b92de69cf42e4ad55246f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687269"
---
# <a name="msvm_metricservicesettingdata-class"></a>MSVM \_ MetricServiceSettingData (clase)

Representa la configuración para el servicio de métricas. Las propiedades de esta clase no se pueden modificar directamente. El cliente debe llamar al método [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) para modificar cualquiera de estas propiedades.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service Settings";
  string   Description = "Defines Hyper-V Metric Service Settings";
  string   ElementName = "Hyper-V Metric Service Settings";
  datetime MetricsFlushInterval;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ MetricServiceSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ MetricServiceSettingData** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración del servicio de métricas de Hyper-V".

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "define la configuración del servicio de métricas de Hyper-V".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración del servicio de métricas de Hyper-V".

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**MetricsFlushInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Define el intervalo en el que las métricas se deben vaciar en el disco.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SettingData de CIM \_**](cim-settingdata.md)
</dt> <dt>

[**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md)
</dt> </dl>

 

