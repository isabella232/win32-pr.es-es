---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 50397050-3b5c-4683-972c-95d9f661b365
ms.tgt_platform: multiple
title: D (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d469b94ec6649c64722fb414880d2e79fc3c88b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082756"
---
# <a name="d-wmi"></a>D (WMI)

[A](gloss-a.md) B [C](gloss-c.md) D [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [o](gloss-o.md) [p](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [s](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**DateTime**
</dt> <dd>

Vea [*CIM DateTime*](gloss-c.md).

</dd> <dt>

<span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**proveedor desacoplado**
</dt> <dd>

Proveedor hospedado en un proceso independiente de WMI. Los proveedores desacoplados son la forma recomendada de instrumentar una aplicación, ya que el proveedor puede controlar su propia duración en lugar de iniciarse cada vez que un usuario tiene acceso al proveedor a través de WMI.

</dd> <dt>

<span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**acceso directo**
</dt> <dd>

Una manera de tener acceso a las propiedades y métodos proporcionados por WMI en un script como si fueran propiedades y métodos de automatización de [**SWbemObject**](swbemobject.md).

Acceso no directo: `VolumeName = MyDisk.Properties_("VolumeName")`

Acceso directo: `VolumeName = MyDisk.VolumeName`

</dd> <dt>

<span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**Distributed Management Task Force (DMTF)**
</dt> <dd>

Una organización internacional de estándares que trabaja con proveedores de tecnología clave, incluido Microsoft, para liderar el desarrollo, la adopción y la unificación de estándares de administración e iniciativas para entornos de escritorio, empresariales y de Internet.

</dd> <dt>

<span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**DTMF**
</dt> <dd>

Consulte *Distributed Management Task Force (DMTF)*.

</dd> <dt>

<span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**clase dinámica**
</dt> <dd>

Una clase CIM cuya definición se proporciona a través de un [*proveedor*](gloss-p.md) en tiempo de ejecución, según sea necesario. Las clases dinámicas representan [*objetos administrados*](gloss-m.md) específicos del proveedor y no se almacenan en el [*repositorio CIM*](gloss-c.md). Las clases dinámicas solo admiten *instancias dinámicas*.

</dd> <dt>

<span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**instancia dinámica**
</dt> <dd>

Instancia de una clase CIM suministrada por un [*proveedor*](gloss-p.md) cuando es necesario. No se almacena en el [*repositorio CIM*](gloss-c.md). Las instancias dinámicas se pueden proporcionar para clases estáticas o dinámicas. La compatibilidad dinámica con instancias de una clase permite a un proveedor proporcionar valores de [*propiedad*](gloss-p.md) actualizados.

</dd> </dl>

 

 



