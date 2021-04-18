---
description: Representa la información de identificación de un monitor de vídeo, como el nombre del fabricante, el año de fabricación o el número de serie.
ms.assetid: 85c8c4b1-20e2-4c0b-9209-a3724509a2f0
title: Clase WmiMonitorID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorID
- WmiMonitorID.Active
- WmiMonitorID.InstanceName
- WmiMonitorID.ManufacturerName
- WmiMonitorID.ManufacturerNameLength
- WmiMonitorID.ProductCodeID
- WmiMonitorID.SerialNumberID
- WmiMonitorID.WeekOfManufacture
- WmiMonitorID.YearOfManufacture
- WmiMonitorID.UserFriendlyName
- WmiMonitorID.UserFriendlyNameLength
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.custom: project-verbatim
ms.openlocfilehash: 485b42a86ca67d15ec00be13992c17b31ed51608
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105718589"
---
# <a name="wmimonitorid-class"></a>Clase WmiMonitorID

La clase WMI **WmiMonitorID** representa la información de identificación de un monitor de vídeo, como el nombre del fabricante, el año de fabricación o el número de serie. Los datos de esta clase se corresponden con los datos del bloque de identificación de proveedor/producto de la definición de entrada de vídeo de la estándar de identificación extendida de vídeo (E-EDID) de la Asociación estándar de vídeo electrónica (VESA).

## <a name="syntax"></a>Sintaxis

``` syntax
class WmiMonitorID : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint16  ManufacturerName[];
  uint16  ManufacturerNameLength;
  uint16  ProductCodeID[];
  uint16  SerialNumberID[];
  uint8   WeekOfManufacture;
  uint16  YearOfManufacture;
  uint16  UserFriendlyName[];
  uint16  UserFriendlyNameLength;
};
```

## <a name="members"></a>Miembros

La clase **WmiMonitorID** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **WmiMonitorID** tiene estas propiedades.

<dl> <dt>

**Activo**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el monitor activo.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Nombre de la instancia de monitor específica.

</dd> <dt>

**ManufacturerName**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del fabricante.

</dd> <dt>

**ManufacturerNameLength**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Longitud del nombre del fabricante ubicada en la propiedad **ManufacturerName** .

</dd> <dt>

**ProductCodeID**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

IDENTIFICADOR de código de producto asignado por el proveedor.

</dd> <dt>

**SerialNumberID**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de serie.

</dd> <dt>

UserFriendlyName
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre descriptivo del monitor. El tamaño del nombre es la longitud especificada por la propiedad UserFriendlyNameLength.

</dd> <dt>

UserFriendlyNameLength
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de caracteres del nombre que se encuentra en la propiedad UserFriendlyName.

</dd> <dt>

**WeekOfManufacture**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Semana de fabricación por número de semana. El intervalo está comprendido entre 1 y 53. Cero (0) no está definido.

</dd> <dt>

**YearOfManufacture**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Año de fabricación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para obtener una explicación sobre cómo traducir las matrices que almacenan los IDENTIFICADOres de número de serie, consulte el artículo [información del monitor de informes con Configuration Manager](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) blog.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de PowerShell se recupera el número de serie de varios monitores.


```PowerShell
gwmi WmiMonitorID -Namespace root\wmi | ForEach-Object {($_.UserFriendlyName -ne 0 | foreach {[char]$_}) -join ""; ($_.SerialNumberID -ne 0 | foreach {[char]$_}) -join ""}
```



El siguiente código de VBScript también recupera información del ID. de monitor de un sistema.


```VB
Option Explicit

Dim strComputer, objWMIService, colItems, objItem

strComputer = "MyComputer"

Set objWMIService = GetObject("winmgmts:" _ 
  & "{impersonationLevel=impersonate,authenticationLevel=Pkt}!\\" _ 
  & strComputer & "\root\wmi") 

Set colItems = objWMIService.ExecQuery _
  ("SELECT * FROM WMIMonitorID")

For Each objItem In colItems
  Wscript.Echo objItem.InstanceName
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | \\WMI raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

