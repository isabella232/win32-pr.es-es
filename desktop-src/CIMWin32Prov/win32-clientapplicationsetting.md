---
description: La clase WMI de asociación ClientApplicationSetting de Win32 relaciona un archivo ejecutable y una aplicación de Modelo de objetos componentes (COM) que contiene las opciones de configuración COM para \_ el archivo ejecutable.
ms.assetid: c43d80ee-0f29-4452-b51f-f18543bc1d35
ms.tgt_platform: multiple
title: Win32_ClientApplicationSetting clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClientApplicationSetting
- Win32_ClientApplicationSetting.Application
- Win32_ClientApplicationSetting.Client
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fda1f1305904fa919bb2080fe5de02f0e5850a8a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160329"
---
# <a name="win32_clientapplicationsetting-class"></a>Clase \_ ClientApplicationSetting de Win32

La clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) de asociación **\_ ClientApplicationSetting de Win32** relaciona un archivo ejecutable y una aplicación de Modelo de objetos componentes (COM) que contiene las opciones de configuración COM para el archivo ejecutable.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5E-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClientApplicationSetting
{
  Win32_DCOMApplication REF Application;
  CIM_DataFile          REF Client;
};
```

## <a name="members"></a>Members

La **clase \_ ClientApplicationSetting de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ClientApplicationSetting de Win32** tiene estas propiedades.

<dl> <dt>

**Aplicación**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ DCOMApplication**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")
</dt> </dl>

Referencia a la instancia de que representa la aplicación COM que contiene las opciones de configuración del archivo ejecutable.

</dd> <dt>

**Cliente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ DataFile**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| \_ DataFile")
</dt> </dl>

Referencia a la instancia de que representa el archivo ejecutable que usa la configuración COM.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**Win32 \_ ClientApplicationSetting** no admite la enumeración .

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

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

