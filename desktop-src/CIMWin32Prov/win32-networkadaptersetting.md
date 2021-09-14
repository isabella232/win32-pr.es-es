---
description: La clase WMI de asociación NetworkAdapterSetting de Win32 relaciona \_ un adaptador de red y sus opciones de configuración.
ms.assetid: 6fc646c3-05f9-4c92-8598-07ea20fffaca
ms.tgt_platform: multiple
title: Win32_NetworkAdapterSetting clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterSetting
- Win32_NetworkAdapterSetting.Setting
- Win32_NetworkAdapterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c51ef9ed790c902a6a662dc3ebc45df97fa29721
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062561"
---
# <a name="win32_networkadaptersetting-class"></a>Clase \_ NetworkAdapterSetting de Win32

La clase WMI **de \_ asociación NetworkAdapterSetting** [de](../wmisdk/retrieving-a-class.md) Win32 relaciona un adaptador de red y sus opciones de configuración.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterSetting : Win32_DeviceSettings
{
  Win32_NetworkAdapterConfiguration REF Setting;
  Win32_NetworkAdapter              REF Element;
};
```

## <a name="members"></a>Members

La **clase \_ NetworkAdapterSetting de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ NetworkAdapterSetting de Win32** tiene estas propiedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ NetworkAdapter**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapter")
</dt> </dl>

Un [**\_ NetworkAdapter de Win32**](win32-networkadapter.md) que describe las propiedades del adaptador de red que usa una configuración de adaptador de red determinada.

</dd> <dt>

**Configuración**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ NetworkAdapterConfiguration de Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration")
</dt> </dl>

Un [**objeto \_ NetworkAdapterConfiguration de Win32**](win32-networkadapterconfiguration.md) que describe los valores de configuración utilizados en el adaptador de red.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ NetworkAdapterSetting de Win32** se deriva de [**Win32 \_ DeviceSettings.**](win32-devicesettings.md)

Para obtener información sobre cómo usar clases de asociación, vea [ASSOCIATORS OF (Instrucción](../wmisdk/associators-of-statement.md)).

## <a name="examples"></a>Ejemplos

En el ejemplo de VBScript siguiente se **usa \_ NetworkAdapterSetting de Win32** para identificar la dirección IP en la conexión de área local.


```VB
strComputer = "."
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colNics = objWMIService.ExecQuery _
    ("Select * From Win32_NetworkAdapter " _
        & "Where NetConnectionID = " & _
        "'Local Area Connection'")
 
For Each objNic in colNics
    Set colNicConfigs = objWMIService.ExecQuery _
      ("ASSOCIATORS OF " _
          & "{Win32_NetworkAdapter.DeviceID='" & _
      objNic.DeviceID & "'}" & _
      " WHERE AssocClass=Win32_NetworkAdapterSetting")
    For Each objNicConfig In colNicConfigs
        For Each strIPAddress in objNicConfig.IPAddress
            Wscript.Echo "IP Address: " &  strIPAddress
        Next
    Next
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Dispositivo \_ Win32Settings**](win32-devicesettings.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> <dt>

[Tareas wmi: redes](../wmisdk/wmi-tasks--networking.md)
</dt> </dl>

 

 
