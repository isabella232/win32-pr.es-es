---
description: El objeto de configuración CIM permite la agrupación de conjuntos de parámetros (definidos en objetos de configuración de CIM) y dependencias \_ para uno o varios elementos del sistema \_ administrados.
ms.assetid: f597fe78-be50-4d31-b1eb-d219acaf1751
ms.tgt_platform: multiple
title: CIM_Configuration clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Configuration
- CIM_Configuration.Caption
- CIM_Configuration.Description
- CIM_Configuration.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c6df2338d46438bf3e1af371ebbce8b36f1a337f26a4785064119cca45bece46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924935"
---
# <a name="cim_configuration-class"></a>Cim \_ Configuration (clase)

El **objeto de \_ configuración CIM** permite la agrupación de conjuntos de parámetros (definidos en objetos de configuración [**de CIM) \_**](cim-setting.md) y dependencias para uno o varios elementos del sistema administrados. Este objeto representa un comportamiento determinado o un estado funcional deseado para los elementos del sistema administrados. El estado funcional deseado suele estar controlado por requisitos externos, como la hora o la ubicación. Por ejemplo, para conectarse a un sistema de correo desde casa, existe una dependencia en un módem; mientras que, existe una dependencia en un adaptador de red en el trabajo. Configuración para los dispositivos lógicos pertinentes (en este ejemplo, el módem y el adaptador de red DE MACS) se pueden definir y agregar mediante la configuración **\_ de CIM**. Por lo tanto, se pueden definir dos configuraciones Conectar "enviar a Mail" agrupando las dependencias pertinentes y los [**objetos de \_ configuración cim.**](cim-setting.md)

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{4C51D7AE-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_Configuration
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a>Miembros

La **clase \_ cim configuration** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ de configuración** CIM tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descripción textual del objeto **\_ de configuración cim.**

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto **\_ de configuración cim.**

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Etiqueta por la que se **\_ conoce** el objeto de configuración cim.

</dd> </dl>

## <a name="remarks"></a>Comentarios

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

