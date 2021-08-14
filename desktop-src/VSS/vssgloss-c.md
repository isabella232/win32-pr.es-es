---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d6528e81-2082-4180-a21e-d12ffe3c9c9c
title: C (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e10734fa1676980473b53cb16f5cf1166d5b2ff2813f9bf59159c37116514c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751451"
---
# <a name="c-volume-shadow-copy-service"></a>C (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) H [](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**entidad de certificación**
</dt> <dd>

Una entidad que confía en emitir certificados que declaran que el destinatario individual, la máquina u organización que solicita el certificado cumple las condiciones de una directiva establecida.

</dd> <dt>

<span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**instantánea accesible para el cliente**
</dt> <dd>

Una instantánea creada por el proveedor del sistema para admitir Instantáneas para carpetas compartidas y otros mecanismos de reversión, que permiten a los clientes ver versiones anteriores de archivos y deshacer errores sin necesidad de una restauración completa. Se crea una instantánea accesible desde el cliente mediante el valor **ACCESIBLE DE CLIENTE DE VSS \_ \_ \_ CTX** de la [**\_ enumeración \_ SNAPSHOT CONTEXT \_ de VSS.**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) Además, el valor ACCESIBLE DEL CLIENTE DE ATTR DE VSS VOLSNAP de la enumeración ATRIBUTOS DE INSTANTÁNEAS DE VOLUMEN DE VSS se establece automáticamente para instantáneas accesibles \_ \_ para el \_ \_ cliente. [**\_ \_ \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) Consulte también [*Instantáneas para carpetas compartidas*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**Componente**
</dt> <dd>

Un grupo de archivos, definido por un escritor, que se debe controlar como una unidad durante las operaciones de copia de seguridad y restauración. Vea también componente [*de base de datos*](vssgloss-d.md), componente de grupo de [*archivos*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**dependencia de componentes**
</dt> <dd>

Una situación en la que un componente (y el conjunto de componentes que define) administrado por un escritor no se puede realizar una copia de seguridad o restaurar independientemente de los componentes administrados por otros escritores. Una dependencia no indica un orden de preferencia entre el componente con las dependencias documentadas y los componentes de los que depende: una dependencia simplemente indica que el componente y los componentes de los que depende siempre deben realizarse o restaurarse juntos.

</dd> <dt>

<span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**modo de componente**
</dt> <dd>

Modo en el que una operación de copia de seguridad o restauración usa la información de componentes de un escritor. Consulte también [*el componente seleccionable*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**conjunto de componentes**
</dt> <dd>

Un grupo de componentes con al menos un componente seleccionable (para copia de seguridad o restauración) y una serie de componentes no seleccionables organizados en una jerarquía por sus rutas de acceso lógicas. La participación implícita en una operación de copia de seguridad o restauración depende de la inclusión explícita del componente seleccionable de nivel superior. Solo la información de componente de este componente seleccionable se incluye en el documento Componentes de copia de seguridad. Un conjunto de componentes puede incluir subcomponentes seleccionables y no seleccionables. Vea también [*ruta de acceso lógica*](vssgloss-l.md), componente [*seleccionable*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**instantánea de copia en escritura**
</dt> <dd>

Instantánea creada guardando solo las diferencias con respecto al volumen original.

</dd> <dt>

<span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**estado coherente con el bloqueo**
</dt> <dd>

El estado de los discos equivalente al que se encontraría después de un error catastrófico que apaga repentinamente el sistema. Una restauración desde este conjunto de instantáneas sería equivalente a un reinicio después de un apagado brusco. Este es el estado predeterminado de los datos que se han copiado en la sombra sin la compatibilidad de los escritores.

</dd> </dl>

 

 



