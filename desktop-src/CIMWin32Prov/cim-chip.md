---
description: La clase chip CIM representa el tipo de hardware de circuito integrado, incluidos los \_ ASIC, procesadores, chips de memoria, entre otros.
ms.assetid: 3c2b0023-5d02-49b9-90f5-d66eb8a103f0
ms.tgt_platform: multiple
title: CIM_Chip clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chip
- CIM_Chip.Caption
- CIM_Chip.Description
- CIM_Chip.InstallDate
- CIM_Chip.Name
- CIM_Chip.Status
- CIM_Chip.CreationClassName
- CIM_Chip.Manufacturer
- CIM_Chip.Model
- CIM_Chip.OtherIdentifyingInfo
- CIM_Chip.PartNumber
- CIM_Chip.PoweredOn
- CIM_Chip.SerialNumber
- CIM_Chip.SKU
- CIM_Chip.Tag
- CIM_Chip.Version
- CIM_Chip.HotSwappable
- CIM_Chip.Removable
- CIM_Chip.Replaceable
- CIM_Chip.FormFactor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 953ae371edca42409246307b21aad69a02cf4a66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255914"
---
# <a name="cim_chip-class"></a>Cim \_ Chip (clase)

La **clase chip CIM \_** representa el tipo de hardware de circuito integrado, incluidos los ASIC, procesadores, chips de memoria, entre otros.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract, UUID("{FAF76B7A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chip : CIM_PhysicalComponent
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  uint16   FormFactor;
};
```

## <a name="members"></a>Members

La **clase \_ Cim Chip** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ chip CIM** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descripción textual del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**\_ clave CIM,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre de la clase o subclase usada en la creación de una instancia de . Cuando se usa con otras propiedades clave de la clase , esta propiedad permite identificar de forma única todas las instancias de la clase y sus subclases.

Esta propiedad se hereda de [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descripción textual del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**FormFactor**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Factor de forma de implementación del chip. Se pueden especificar los valores siguientes.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="SIP"></span><span id="sip"></span>

**SIP** (2)


</dt> <dd></dd> <dt>

<span id="DIP"></span><span id="dip"></span>

**DIP** (3)


</dt> <dd></dd> <dt>

<span id="ZIP"></span><span id="zip"></span>

**ZIP** (4)


</dt> <dd></dd> <dt>

<span id="SOJ"></span><span id="soj"></span>

**SOJ** (5)


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

**Propietario** (6)


</dt> <dd></dd> <dt>

<span id="SIMM"></span><span id="simm"></span>

**SIMM** (7)


</dt> <dd></dd> <dt>

<span id="DIMM"></span><span id="dimm"></span>

**DIM** (8)


</dt> <dd></dd> <dt>

<span id="TSOP"></span><span id="tsop"></span>

**TSOP** (9)


</dt> <dd></dd> <dt>

<span id="PGA"></span><span id="pga"></span>

**PGA** (10)


</dt> <dd></dd> <dt>

<span id="RIMM"></span><span id="rimm"></span>

**RIMM** (11)


</dt> <dd></dd> <dt>

<span id="SODIMM"></span><span id="sodimm"></span>

**SODIMM** (12)


</dt> <dd></dd> <dt>

<span id="SRIMM"></span><span id="srimm"></span>

**SRIMM** (13)


</dt> <dd></dd> <dt>

<span id="SMD"></span><span id="smd"></span>

**SMD** (14)


</dt> <dd></dd> <dt>

<span id="SSMP"></span><span id="ssmp"></span>

**SSMP** (15)


</dt> <dd></dd> <dt>

<span id="QFP"></span><span id="qfp"></span>

**QFP** (16)


</dt> <dd></dd> <dt>

<span id="TQFP"></span><span id="tqfp"></span>

**TQFP** (17)


</dt> <dd></dd> <dt>

<span id="SOIC"></span><span id="soic"></span>

**SOIC** (18)


</dt> <dd></dd> <dt>

<span id="LCC"></span><span id="lcc"></span>

**LCC** (19)


</dt> <dd></dd> <dt>

<span id="PLCC"></span><span id="plcc"></span>

**PLCC** (20)


</dt> <dd></dd> <dt>

<span id="BGA"></span><span id="bga"></span>

**BGA** (21)


</dt> <dd></dd> <dt>

<span id="FPBGA"></span><span id="fpbga"></span>

**FPBGA** (22)


</dt> <dd></dd> <dt>

<span id="LGA"></span><span id="lga"></span>

**LGA** (23)


</dt> <dd></dd> <dt>

<span id="FB-DIMM"></span><span id="fb-dimm"></span>

**FB-DIM** (24)


</dt> <dd></dd> </dl>

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el paquete se puede intercambiar en caliente. Un paquete físico se puede intercambiar en caliente si el elemento se puede reemplazar por uno físicamente diferente (pero equivalente) mientras el paquete que lo contiene está activado. Por ejemplo, un componente de ventilador se puede diseñar para intercambiarse en caliente. Todos los componentes que se pueden intercambiar en caliente son intrínsecamente extraíbles y reemplazables.

Esta propiedad se hereda de [**CIM \_ PhysicalComponent.**](cim-physicalcomponent.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Fecha de instalación")
</dt> </dl>

Indica cuándo se instaló el objeto. La falta de un valor no indica que el objeto no está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre de la organización responsable de generar el elemento físico. Para obtener más información, vea la **propiedad Vendor** del [**producto \_ CIM.**](cim-product.md)

Esta propiedad se hereda de [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Modelo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Nombre por el que se suele conocer el elemento físico.

Esta propiedad se hereda de [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nombre")
</dt> </dl>

Etiqueta por la que se conoce el objeto. Cuando se subclasifica, esta propiedad se puede invalidar para que sea una propiedad de clave.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Datos adicionales, más allá de la información de etiquetas de recurso, que se pueden usar para identificar un elemento físico. Un ejemplo son los datos de código de barras asociados a un elemento, que también tiene una etiqueta de recurso. Tenga en cuenta que si solo hay datos de código de barras disponibles y es único y se puede usar como clave de elemento, esta propiedad sería NULL y los datos del código de barra se usarían como clave de clase en la **propiedad Tag.**

Esta propiedad se hereda de [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Número de pieza asignado por la organización responsable de producir o fabricación del elemento físico.

Esta propiedad se hereda de [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**PoweredOn**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el elemento físico está encendido. De lo contrario, está desactivado actualmente.

Esta propiedad se hereda de [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Extraíble**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** este elemento está diseñado para su entrada y salida del contenedor físico en el que se encuentra normalmente, sin afectar a la función del empaquetado general. Un paquete se considera extraíble incluso si la alimentación debe estar desactivada para realizar la eliminación. Si la energía puede estar encendido y el paquete quitado, el elemento es extraíble y se puede intercambiar en caliente. Por ejemplo, un chip de procesador actualizable es extraíble.

Esta propiedad se hereda de [**CIM \_ PhysicalComponent.**](cim-physicalcomponent.md)

</dd> <dt>

**Reemplazable**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** es posible reemplazar el elemento por uno físicamente diferente. Por ejemplo, algunos sistemas informáticos permiten actualizar el chip del procesador principal a una de las especificaciones de reloj más altas. En este caso, se dice que el procesador es reemplazable. Todos los componentes extraíbles se pueden reemplazar de forma inherente.

Esta propiedad se hereda de [**CIM \_ PhysicalComponent.**](cim-physicalcomponent.md)

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Número asignado por el fabricante usado para identificar el elemento físico.

Esta propiedad se hereda de [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Número de unidad de mantenimiento de existencias para este elemento físico.

Esta propiedad se hereda de [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Cadena que indica el estado actual del objeto. Se puede definir el estado operativo y no operativo. El estado operativo puede incluir "Ok", "Degraded" y "Pred Fail". "Error previo" indica que un elemento funciona correctamente, pero predice un error (por ejemplo, una unidad de disco duro habilitada para SMART).

El estado no operativo puede incluir "Error", "Starting", "Stopping" y "Service". El "servicio" se puede aplicar durante la resilvering del reflejo del disco, volver a cargar una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "correcto" ni está en uno de los demás estados.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Los valores son los siguientes:

<dt>

<span id="OK"></span><span id="ok"></span>

**Ok** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Error** ("Error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("Degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** ("Desconocido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Error de pred** ("error previo")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**A partir** de ("Starting")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detención** ("Deteniendo")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servicio** ("Servicio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Estresado** ("estresado")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sin contacto** ("Sin contacto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comm perdido** ("Comm perdido")


</dt> <dd></dd> </dl>

</dd> <dt>

**Tag**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**\_ clave CIM,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identifica de forma única el elemento físico y actúa como clave del elemento. Esta propiedad puede contener información, como datos de etiqueta de recurso o número de serie. La clave de [**CIM \_ PhysicalElement**](cim-physicalelement.md) se coloca muy alta en la jerarquía de objetos para identificar de forma independiente el hardware o la entidad, independientemente de la ubicación física en (o en) gabinetes, adaptadores, y así sucesivamente. Por ejemplo, un componente extraíble que se puede intercambiar en caliente se puede tomar de su paquete que contiene (ámbito) y no usarse temporalmente. El objeto sigue existiendo e incluso se puede insertar en un contenedor de ámbito diferente. La clave de un elemento físico es una cadena arbitraria que se define independientemente de la ubicación o la jerarquía orientada a la ubicación.

Esta propiedad se hereda de [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Indica la versión del elemento físico.

Esta propiedad se hereda de [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ CIM Chip** se deriva de CIM [**\_ PhysicalComponent**](cim-physicalcomponent.md).

WMI no implementa esta clase. Para obtener más información sobre las clases derivadas del **\_ chip CIM,** vea [Clases Win32](win32-provider.md).

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

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

[**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)
</dt> </dl>

 

