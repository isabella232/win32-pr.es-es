---
description: La clase WMI de asociación ComClassAutoEmulator de Win32 relaciona una clase de Modelo de objetos componentes (COM) y otra clase COM que \_ emula automáticamente.
ms.assetid: e060ba26-98e7-47cb-bf21-1ca80d0e8a07
ms.tgt_platform: multiple
title: Win32_ComClassAutoEmulator clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassAutoEmulator
- Win32_ComClassAutoEmulator.NewVersion
- Win32_ComClassAutoEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9442036d43859caa5fa277109c7e85553e7d42f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160310"
---
# <a name="win32_comclassautoemulator-class"></a>Clase \_ ComClassAutoEmulator de Win32

La clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) de asociación **\_ ComClassAutoEmulator de Win32** relaciona una clase de Modelo de objetos componentes (COM) y otra clase COM que emula automáticamente.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5D-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassAutoEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a>Members

La **clase \_ ComClassAutoEmulator de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ComClassAutoEmulator de Win32** tiene estas propiedades.

<dl> <dt>

**NewVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ ClassicCOMClass**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")
</dt> </dl>

Referencia a la instancia de que representa el componente COM que puede emular automáticamente el componente COM asociado. Esta información se obtiene a través de la entrada del Registro AutoTreatAs.

</dd> <dt>

**OldVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ ClassicCOMClass**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")
</dt> </dl>

Referencia a la instancia de que representa el componente COM emulado automáticamente por otro componente.

</dd> </dl>

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

 

