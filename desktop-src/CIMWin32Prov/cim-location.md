---
description: La clase \_ CIM Location representa la posición y la dirección de un elemento físico.
ms.assetid: c1ec467c-a338-4beb-a8fe-1ebc5b05c754
ms.tgt_platform: multiple
title: CIM_Location clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Location
- CIM_Location.Address
- CIM_Location.Name
- CIM_Location.PhysicalPosition
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: aad8fb6ee174cd8619dea4243839f0dd8c555679f6ba176a09099e8a75e8a7df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923335"
---
# <a name="cim_location-class"></a>Cim \_ Location (clase)

La **clase \_ CIM Location** representa la posición y la dirección de un elemento físico.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{FAF76B67-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Location
{
  string Address;
  string Name;
  string PhysicalPosition;
};
```

## <a name="members"></a>Miembros

La **clase \_ CIM Location** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM Location** tiene estas propiedades.

<dl> <dt>

**Dirección**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

Cadena de forma libre que indica una calle u otro tipo de dirección para la ubicación del elemento físico.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Cadena de forma libre que define una etiqueta para la ubicación y forma parte de la clave del objeto.

</dd> <dt>

**PhysicalPosition**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Cadena de forma libre que indica la ubicación de un elemento físico. Puede especificar información de ranura en un panel de hospedaje, sitio de montaje en un gabinete o información de latitud y longitud. Forma parte de la clave del objeto **\_ Cim Location.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

WMI no implementa esta clase. Para las clases derivadas de la ubicación cim , vea [Clases win32](win32-provider.md). **\_**

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

