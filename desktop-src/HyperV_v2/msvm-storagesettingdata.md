---
description: Representa la configuración específica del almacenamiento para un sistema virtual.
ms.assetid: 0b3fcd78-7e9a-4a94-ad18-0ca72b3cfd73
title: Msvm_StorageSettingData clase
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
ms.openlocfilehash: 315eb41b5c445d7ce8856f79054e9a227b2a62fc0986419172e519fc65a9ac31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950114"
---
# <a name="msvm_storagesettingdata-class"></a>Clase \_ StorageSettingData de Msvm

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

La **clase \_ StorageSettingData de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ StorageSettingData de Msvm** tiene estas propiedades.

<dl> <dt>

**DisableInterruptBatching**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si se debe deshabilitar el procesamiento por lotes de interrupción.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) de la clase Wmi [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**ThreadCountPerChannel**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de subprocesos por canal de almacenamiento para procesar E/S.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) de la clase [**\_ VirtualSystemManagementService de Msvm.**](msvm-virtualsystemmanagementservice.md)

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Valor** predeterminado (0)


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

Número elevado de subprocesos por canal de almacenamiento.

</dd> </dl>

</dd> <dt>

**VirtualProcessorsPerChannel**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de procesadores por canal de almacenamiento. El número de canales que se abrirán lo da (Recuento de procesadores lógicos en el **host/VirtualProcessorsPerChannel).**

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) de la clase [**\_ VirtualSystemManagementService de Msvm.**](msvm-virtualsystemmanagementservice.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md)
</dt> </dl>

 

 




