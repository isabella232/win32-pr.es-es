---
description: A partir de Windows 7, Windows Management Instrumentation (WMI) implementó un mecanismo estándar para detectar perfiles mediante el esquema CIM.
ms.assetid: e748b623-5ff3-464d-ba09-96cf226de7b6
ms.tgt_platform: multiple
title: Recorrido de asociación entre espacios de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe2bbb408c4d89a7093adf45f3daf276df294ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575377"
---
# <a name="cross-namespace-association-traversal"></a>Recorrido de asociación entre espacios de nombres

A partir de Windows 7, Windows Management Instrumentation (WMI) implementó un mecanismo estándar para detectar perfiles mediante el esquema CIM.

WMI admite el recorrido de asociación entre espacios de nombres y el registro de perfil de asociación. Para obtener más información sobre el registro de perfiles y la implementación estándar CIM del recorrido de asociación, vea DSP1033 ( [https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf) )

Para admitir esta característica, la infraestructura WMI hizo lo siguiente:

-   Creó el espacio de nombres de \\ \\ interoperabilidad: interoperabilidad raíz.
-   Recorrido de asociación entre espacios de nombres permitido. Las asociaciones que cruzan espacios de nombres admiten el filtrado en el nivel de clase de asociación y en el nivel de espacio de nombres implementado.
-   Se han agregado [**las clases \_ CIM RegisteredProfile**](/previous-versions//ee309375(v=vs.85)), [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)y [**CIM \_ ReferencedProfile.**](cim-referencedprofile.md)
-   Compatibilidad con el esquema CIM implementado versión 2.17.1. Para obtener más información, vea [Cim Schema Compatibility](cim-schema-compatibility.md).

## <a name="interop-namespace"></a>Espacio de nombres de interoperabilidad

El espacio de nombres de interoperabilidad proporciona una ubicación común para que una aplicación cliente detecte todos los perfiles que se admiten en un equipo. Los perfiles se pueden usar para administrar varios aspectos de un sistema operativo, una matriz de almacenamiento o una base de datos.

Todas las clases y objetos de interoperabilidad deben definirse en el espacio de nombres \\ de interoperabilidad raíz.

## <a name="cim-classes"></a>Clases CIM

Las clases CIM descritas en la lista siguiente admiten el recorrido de asociación entre espacios de nombres.

<dl> <dt>

<span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))
</dt> <dd>

Se usa para identificar la especificación de perfil que se anuncia como implementada. Esta clase especifica información que incluye el nombre del perfil, la organización y la versión con la que la implementación es compatible.

</dd> <dt>

<span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**Elemento \_ CIMConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dd>

Se usa para asociar instancias de elementos de administración que se definen en perfiles con la clase [**\_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) de CIM que identifica las especificaciones de perfil concretas que se implementan.

</dd> <dt>

<span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**CIM \_ ReferencedProfile**](cim-referencedprofile.md)
</dt> <dd>

Se usa para representar la relación entre los perfiles.

</dd> </dl>

## <a name="implementing-cross-namespace-association-traversal"></a>Implementación del recorrido de asociación entre espacios de nombres

El servicio WMI permite el recorrido de asociación entre espacios de nombres. WMI proporciona el espacio de nombres de interoperabilidad para registrar perfiles y asociarlos a perfiles que se implementan en espacios de nombres diferentes. Sin embargo, para usar el recorrido de asociación, los implementadores deben crear instancias de las clases de perfil tanto en la interoperabilidad como en el espacio de nombres implementado. Para obtener más información, vea [Escribir un proveedor de asociación para la interoperabilidad.](writing-an-association-provider-for-interop.md)

Se deben crear instancias de las asociaciones que cruzan espacios de nombres dentro del mismo entorno de administración tanto en los espacios de nombres de interoperabilidad como en los espacios de nombres implementados. De lo contrario, el recorrido de asociación no funcionará. Por ejemplo, el proveedor de asociación de perfiles de energía debe registrarse con los espacios de nombres root/interop y root/cimv2/power. El recorrido de asociación debe poder producirse desde cualquier espacio de nombres de vuelta al otro. Para obtener ejemplos de recorrido de asociación, vea [Accessing Data in the Interop Namespace](accessing-data-in-the-interop-namespace.md).

**Windows Vista: **

Después de actualizar a Windows 7, si hay perfiles de dispositivo de interoperabilidad que se instalaron previamente en el espacio de nombres raíz o de interoperabilidad, no se instalará ningún perfil Windows 7. Estos objetos de perfil de terceros sobrescriben Windows esquema de interoperabilidad 7 para mantener la funcionalidad. Además, se registra el identificador de evento 5631 de la aplicación WMI.

Para obtener los Windows de interoperabilidad de Windows 7, se debe compilar la versión Windows 7 del archivo Interop.mof y los archivos MFL relacionados. Para obtener más información, [vea Compilar archivos MOF.](compiling-mof-files.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[**Elemento \_ CIMConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[**CIM \_ ReferencedProfile**](cim-referencedprofile.md)
</dt> <dt>

[Compatibilidad de esquemas CIM](cim-schema-compatibility.md)
</dt> <dt>

[Escribir un proveedor de asociación para la interoperabilidad](writing-an-association-provider-for-interop.md)
</dt> <dt>

[Acceso a datos en el espacio de nombres interop](accessing-data-in-the-interop-namespace.md)
</dt> </dl>

 

 
