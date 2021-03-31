---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d6528e81-2082-4180-a21e-d12ffe3c9c9c
title: C (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f4f66a29a64e85418767fe561d0068cdcce381a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809817"
---
# <a name="c-volume-shadow-copy-service"></a>C (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q [R](vssgloss-r.md) [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**entidad de certificación**
</dt> <dd>

Una entidad de confianza para emitir certificados que impongan que el destinatario individual, equipo u organización que solicita el certificado cumple las condiciones de una directiva establecida.

</dd> <dt>

<span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**instantánea accesible para el cliente**
</dt> <dd>

Una instantánea creada por el proveedor del sistema para admitir Instantáneas para carpetas compartidas y otros mecanismos de reversión, que permiten a los clientes ver las versiones anteriores de los archivos y deshacer los errores sin necesidad de una restauración completa. Una instantánea accesible para el cliente se crea mediante el **valor \_ \_ \_ accesible del cliente de VSS CTX** de la enumeración de [**\_ \_ \_ contexto de instantáneas de VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) . Además, el \_ \_ \_ valor accesible del cliente de atributo VOLSNAP \_ de VSS de la enumeración de [**\_ \_ \_ \_ atributos de instantáneas de volumen de VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) se establece automáticamente para las instantáneas accesibles para el cliente. Vea también [*instantáneas para carpetas compartidas*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**pone**
</dt> <dd>

Grupo de archivos, definido por un escritor, que se debe administrar como una unidad durante las operaciones de copia de seguridad y restauración. Vea también [*componente de base de datos*](vssgloss-d.md), [*componente de grupo de archivos*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**dependencia de componentes**
</dt> <dd>

Una situación en la que no se puede hacer una copia de seguridad de un componente (y el conjunto de componentes que define) administrado por un escritor no se puede realizar ni restaurar independientemente de los componentes administrados por otros escritores. Una dependencia no indica un orden de preferencia entre el componente con las dependencias documentadas y los componentes de los que depende: una dependencia simplemente indica que el componente y los componentes de los que depende deben ser siempre copiados o restaurados juntos.

</dd> <dt>

<span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**modo de componente**
</dt> <dd>

Modo en el que una operación de copia de seguridad o restauración hace uso de la información del componente de un escritor. Vea también [*componente seleccionable*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**conjunto de componentes**
</dt> <dd>

Grupo de componentes con al menos un componente seleccionable (para copia de seguridad o restauración) y varios componentes no seleccionables organizados en una jerarquía por sus rutas de acceso lógicas. La participación implícita en una operación de copia de seguridad o restauración depende de la inclusión explícita del componente seleccionable de nivel superior. En el documento componentes de copia de seguridad solo se incluye la información de componentes de este componente seleccionable. Un conjunto de componentes puede incluir subcomponentes seleccionables y no seleccionables. Vea también [*ruta de acceso lógica*](vssgloss-l.md), [*componente seleccionable*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**copia instantánea en escritura**
</dt> <dd>

Una instantánea que se crea al guardar solo las diferencias del volumen original.

</dd> <dt>

<span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**estado coherente con el bloqueo**
</dt> <dd>

El estado de los discos equivalente a lo que se encontraría después de un error catastrófico que apaga repentinamente el sistema. Una restauración de este conjunto de instantáneas sería equivalente a un reinicio después de un apagado brusco. Este es el estado predeterminado de los datos de los que se ha realizado una copia sombra sin la compatibilidad de escritores.

</dd> </dl>

 

 



