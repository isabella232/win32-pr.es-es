---
description: Representa la configuración específica del almacenamiento para un sistema virtual.
ms.assetid: 0b3fcd78-7e9a-4a94-ad18-0ca72b3cfd73
title: Msvm_StorageSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageSettingData
- Msvm_StorageSettingData.VirtualProcessorsPerChannel
- Msvm_StorageSettingData.DisableInterruptBatching
- Msvm_StorageSettingData.ThreadCountPerChannel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: db061d048ce45a4d6fa076a5b0367e794cdf16e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653093"
---
# <a name="msvm_storagesettingdata-class"></a>MSVM \_ StorageSettingData (clase)

Representa la configuración específica del almacenamiento para un sistema virtual.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageSettingData : Msvm_SystemComponentSettingData
{
  uint16  VirtualProcessorsPerChannel;
  boolean DisableInterruptBatching;
  uint16  ThreadCountPerChannel;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ StorageSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ StorageSettingData** tiene estas propiedades.

<dl> <dt>

**DisableInterruptBatching**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si el procesamiento por lotes de interrupción debe deshabilitarse.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) de la clase [**\_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) de WMI MSVM.

</dd> <dt>

**ThreadCountPerChannel**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El número de subprocesos por canal de almacenamiento para procesar la e/s.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Valor predeterminado** (0)


</dt> <dd>

Comportamiento predeterminado

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>**Bajo** (1)


</dt> <dd>

Número bajo de subprocesos por canal de almacenamiento.

</dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Medio** (2)


</dt> <dd>

Número medio de subprocesos por canal de almacenamiento.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alto** (3)


</dt> <dd>

Gran número de subprocesos por canal de almacenamiento.

</dd> </dl>

</dd> <dt>

**VirtualProcessorsPerChannel**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El número de procesadores por canal de almacenamiento. El número de canales que se van a abrir viene dado por (recuento de procesadores lógicos en el host/**VirtualProcessorsPerChannel**).

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md)
</dt> </dl>

 

 




