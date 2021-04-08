---
description: A partir de Windows 7, Instrumental de administración de Windows (WMI) implementa un mecanismo estándar para detectar perfiles mediante el esquema CIM.
ms.assetid: e748b623-5ff3-464d-ba09-96cf226de7b6
ms.tgt_platform: multiple
title: Cruce seguro de la asociación entre espacios de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe2bbb408c4d89a7093adf45f3daf276df294ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908680"
---
# <a name="cross-namespace-association-traversal"></a>Cruce seguro de la asociación entre espacios de nombres

A partir de Windows 7, Instrumental de administración de Windows (WMI) implementa un mecanismo estándar para detectar perfiles mediante el esquema CIM.

WMI admite el registro transversal de asociación entre espacios de nombres y el perfil de asociación. Para obtener más información sobre el registro de perfiles y la implementación estándar de CIM de cruce seguro de la asociación, vea DSP1033 ( [https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf) )

Para admitir esta característica, la infraestructura de WMI hizo lo siguiente:

-   Se creó el espacio de nombres de interoperabilidad: \\ \\ interoperabilidad raíz.
-   Cruce seguro de la Asociación de espacios de nombres cruzados permitido. Las asociaciones que cruzan los espacios de nombres admiten el filtrado en el nivel de clase de asociación y en el nivel de espacio de nombres implementado.
-   Se han agregado las clases [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)), [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)y [**CIM \_ ReferencedProfile**](cim-referencedprofile.md) .
-   Compatibilidad con la versión de esquema CIM 2.17.1. Para obtener más información, consulte [compatibilidad con esquemas CIM](cim-schema-compatibility.md).

## <a name="interop-namespace"></a>Espacio de nombres Interop

El espacio de nombres Interop proporciona una ubicación común para que una aplicación cliente detecte todos los perfiles que se admiten en un equipo. Los perfiles se pueden usar para administrar diversos aspectos de un sistema operativo, una matriz de almacenamiento o una base de datos.

Todas las clases y objetos de interoperabilidad se deben definir en el \\ espacio de nombres de interoperabilidad raíz.

## <a name="cim-classes"></a>Clases CIM

Las clases CIM descritas en la lista siguiente admiten el cruce seguro de la asociación entre espacios de nombres.

<dl> <dt>

<span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))
</dt> <dd>

Se utiliza para identificar la especificación de perfil que se anuncia como implementada. Esta clase especifica información que incluye el nombre del perfil, la organización y la versión con la que es compatible la implementación.

</dd> <dt>

<span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**\_ELEMENTCONFORMSTOPROFILE CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dd>

Se utiliza para asociar instancias de elementos de administración que se definen en perfiles con la clase [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) que identifica las especificaciones de perfil determinadas que se implementan.

</dd> <dt>

<span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**\_REFERENCEDPROFILE CIM**](cim-referencedprofile.md)
</dt> <dd>

Se utiliza para representar la relación entre los perfiles.

</dd> </dl>

## <a name="implementing-cross-namespace-association-traversal"></a>Implementación del cruce seguro de la asociación entre espacios de nombres

El servicio WMI permite el cruce seguro de la asociación entre espacios de nombres. WMI proporciona el espacio de nombres de interoperabilidad para registrar perfiles y asociarlos a perfiles que se implementan en distintos espacios de nombres. Sin embargo, para usar el recorrido de asociación, los implementadores deben crear instancias de las clases de perfil en la interoperabilidad y en el espacio de nombres implementado. Para obtener más información, consulte [escribir un proveedor de Asociación para la interoperabilidad](writing-an-association-provider-for-interop.md).

Las asociaciones que cruzan espacios de nombres dentro del mismo entorno de administración deben crearse en los espacios de nombres de interoperabilidad e implementados. De lo contrario, el cruce seguro de la asociación no funcionará. Por ejemplo, el proveedor de asociaciones de Perfil de energía se debe registrar con los espacios de nombres root/Interop y root/cimv2/Power. El cruce seguro de la asociación debe ser capaz de producirse desde el espacio de nombres de nuevo al otro. Para obtener ejemplos de cruce seguro de la asociación, vea [acceso a datos en el espacio de nombres de interoperabilidad](accessing-data-in-the-interop-namespace.md).

* * Windows Vista: * *

Después de actualizar a Windows 7, si hay perfiles de dispositivo de interoperabilidad que se instalaron previamente en el espacio de nombres root/Interop, no se instalará ningún perfil de Windows 7. Estos objetos de Perfil de terceros sobrescriben el esquema de interoperabilidad de Windows 7 para mantener la funcionalidad. Además, se registra el ID. de evento 5631 de la aplicación WMI.

Para obtener los perfiles de interoperabilidad de Windows 7, se debe compilar la versión de Windows 7 del archivo Interop. mof y los archivos MFL relacionados. Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[**\_ELEMENTCONFORMSTOPROFILE CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[**\_REFERENCEDPROFILE CIM**](cim-referencedprofile.md)
</dt> <dt>

[Compatibilidad con esquemas CIM](cim-schema-compatibility.md)
</dt> <dt>

[Escribir un proveedor de Asociación para la interoperabilidad](writing-an-association-provider-for-interop.md)
</dt> <dt>

[Obtener acceso a los datos en el espacio de nombres Interop](accessing-data-in-the-interop-namespace.md)
</dt> </dl>

 

 
