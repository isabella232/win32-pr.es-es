---
description: La clase PhysicalPackage de CIM \_ representa elementos físicos que contienen u hospedan otros componentes. Algunos ejemplos son un gabinete de bastidor o una tarjeta adaptadora.
ms.assetid: 9182d413-aa7e-4c2f-94fe-12e99980520c
ms.tgt_platform: multiple
title: CIM_PhysicalPackage clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalPackage
- CIM_PhysicalPackage.Caption
- CIM_PhysicalPackage.CreationClassName
- CIM_PhysicalPackage.Depth
- CIM_PhysicalPackage.Description
- CIM_PhysicalPackage.Height
- CIM_PhysicalPackage.HotSwappable
- CIM_PhysicalPackage.InstallDate
- CIM_PhysicalPackage.Manufacturer
- CIM_PhysicalPackage.Model
- CIM_PhysicalPackage.Name
- CIM_PhysicalPackage.OtherIdentifyingInfo
- CIM_PhysicalPackage.PartNumber
- CIM_PhysicalPackage.PoweredOn
- CIM_PhysicalPackage.Removable
- CIM_PhysicalPackage.Replaceable
- CIM_PhysicalPackage.SerialNumber
- CIM_PhysicalPackage.SKU
- CIM_PhysicalPackage.Status
- CIM_PhysicalPackage.Tag
- CIM_PhysicalPackage.Version
- CIM_PhysicalPackage.Weight
- CIM_PhysicalPackage.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 683331fd9455fe9dd2e53967ff26c8251deb40bc36c3857af448532f92ed80d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118677537"
---
# <a name="cim_physicalpackage-class"></a>\_Clase PhysicalPackage de CIM

La **clase \_ PhysicalPackage** de CIM representa elementos físicos que contienen u hospedan otros componentes. Algunos ejemplos son un gabinete de bastidor o una tarjeta adaptadora.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. ACTUALMENTE, WMI solo admite los [esquemas de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract, UUID("{FAF76B6E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalPackage : CIM_PhysicalElement
{
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a>Miembros

La **clase \_ PhysicalPackage** de CIM tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ Cim PhysicalPackage** tiene estos métodos.



| Método                                                                   | Descripción                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCompatible**](iscompatible-method-in-class-cim-physicalpackage.md) | Comprueba si el elemento físico al que se hace referencia puede incluirse en el paquete físico o insertarlo en este. Wmi no implementa.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ Cim PhysicalPackage** tiene estas propiedades.

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

**Profundidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")
</dt> </dl>

Profundidad del paquete físico, en pulgadas.

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

**Height**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")
</dt> </dl>

Alto del paquete físico, en pulgadas.

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el paquete se puede intercambiar en caliente. Un paquete físico se puede intercambiar en caliente si el elemento se puede reemplazar por uno físicamente diferente (pero equivalente) mientras el paquete que lo contiene está activado. Por ejemplo, un componente de ventilador se puede diseñar para intercambiarse en caliente. Todos los componentes que se pueden intercambiar en caliente son intrínsecamente extraíbles y reemplazables.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Fecha de instalación")
</dt> </dl>

Fecha y hora en que se instaló el objeto. Esta propiedad no necesita un valor para indicar que el objeto está instalado.

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

Nombre de la organización que produjo el elemento físico. Para obtener más información, vea la **propiedad Vendor** del [**producto \_ CIM.**](cim-product.md)

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

Etiqueta por la que se conoce el objeto. Cuando se encuentra en subclases, esta propiedad se puede invalidar para que sea una propiedad de clave.

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

**Partnumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Número de pieza asignado por la organización que produjo o fabricó el elemento físico.

Esta propiedad se hereda de [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**PoweredOn**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el elemento físico está encendido.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Extraíble**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el paquete está diseñado para su entrada y salida del contenedor físico en el que se encuentra normalmente, sin afectar a la función del empaquetado general. Un paquete se considera extraíble incluso si la alimentación debe estar desactivada para realizar la eliminación. Si la alimentación puede estar encendido y se ha quitado el paquete, el elemento es extraíble y se puede intercambiar en caliente. Por ejemplo, un chip de procesador actualizable es extraíble.

</dd> <dt>

**Reemplazable**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** es posible reemplazar el elemento por uno físicamente diferente. Por ejemplo, algunos sistemas informáticos permiten que el chip del procesador principal se actualice a una de las especificaciones de reloj más altas. En este caso, se dice que el procesador es reemplazable. Todos los componentes extraíbles son inherentemente reemplazables.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Número asignado por el fabricante que se usa para identificar el elemento físico.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Número de unidad de mantenimiento de existencias para el elemento físico.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Estado actual del objeto.

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

**Unknown** ("Unknown")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Error de pred** ("error previo")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Starting** ("Starting")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detención** ("Detención")


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

Calificadores: [**\_ Clave CIM,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Cadena arbitraria que identifica de forma única el elemento físico y actúa como clave del elemento. Esta propiedad puede contener información, como datos de etiqueta de recurso o número de serie. La clave de [**CIM \_ PhysicalElement**](cim-physicalelement.md) se coloca muy alta en la jerarquía de objetos para identificar de forma independiente el hardware o la entidad, independientemente de la colocación física en (o en) gabinetes, adaptadores, y así sucesivamente. Por ejemplo, un componente extraíble que se puede intercambiar en caliente se puede tomar de su paquete que contiene (ámbito) y no se puede usar temporalmente. El objeto sigue existiendo e incluso se puede insertar en un contenedor de ámbito diferente. La clave de un elemento físico es una cadena arbitraria que se define independientemente de la ubicación o la jerarquía orientada a la ubicación.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Versión del elemento físico.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Peso**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("libras")
</dt> </dl>

Peso del paquete físico, en kilos.

</dd> <dt>

**Width**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")
</dt> </dl>

Ancho del paquete físico, en pulgadas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ PhysicalPackage** de CIM se deriva de [**CIM \_ PhysicalElement**](cim-physicalelement.md).

WMI no implementa esta clase. Para las clases WMI que se derivan de **\_ CIM PhysicalPackage,** vea [Clases win32.](win32-provider.md)

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ PhysicalElement**](cim-physicalelement.md)
</dt> </dl>

 

