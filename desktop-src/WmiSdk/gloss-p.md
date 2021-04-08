---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d426673b-dea2-4f8b-9259-6a17543f70c0
ms.tgt_platform: multiple
title: P (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dd72fca871352f8a31652eb72f693da43d1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002947"
---
# <a name="p-wmi"></a>P (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [o](gloss-o.md) p [Q](gloss-q.md) [R](gloss-r.md) [s](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**contador de rendimiento**
</dt> <dd>

Propiedad de una clase de rendimiento que se deriva de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) que almacena los datos de rendimiento.

</dd> <dt>

<span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**objeto de rendimiento**
</dt> <dd>

Objeto de una biblioteca de rendimiento que almacena los datos en los contadores. Estos objetos están visibles en la utilidad [*monitor de sistema*](gloss-s.md) . Algunos ejemplos son los objetos de disco lógico y de caché. Cuando el proceso [*ADAP*](gloss-a.md) lo transfiere a WMI, cada objeto se convierte en dos clases de rendimiento de WMI. Una clase, que contiene datos sin procesar, se deriva de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata). La otra clase se deriva de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) y contiene los mismos datos visibles en el monitor de sistema calculados por el proveedor de contadores cocidos.

</dd> <dt>

<span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**consumidor permanente**
</dt> <dd>

[*Consumidor de eventos*](gloss-e.md) cuyo registro se mantiene hasta que se cancela explícitamente. Vea también [*consumidor temporal*](gloss-t.md).

</dd> <dt>

<span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**consumidor físico**
</dt> <dd>

Objeto COM implementado por un proveedor de [*consumidor de eventos*](gloss-e.md) que incluye un [*receptor*](gloss-s.md) para recibir notificaciones de eventos.

</dd> <dt>

<span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**propiedad**
</dt> <dd>

Un par de nombre y valor que describe una unidad de datos para una clase. Los valores de propiedad deben tener un tipo de datos [*Managed Object Format válido (MOF)*](gloss-m.md) . Consulte también [*propiedad Reference*](gloss-r.md).

</dd> <dt>

<span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**proveedor de propiedades**
</dt> <dd>

Un servidor COM que admite la recuperación y modificación de las propiedades de WMI. Los proveedores de propiedades implementan las interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) y [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) .

</dd> <dt>

<span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**presta**
</dt> <dd>

Un servidor COM que se comunica con objetos administrados para obtener acceso a datos y notificaciones de eventos, como el registro o un dispositivo SNMP. Los proveedores reenvían estos datos al [*Administrador de objetos CIM*](gloss-c.md) para la integración y la interpretación.

</dd> <dt>

<span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**método de proveedor**
</dt> <dd>

Método que implementa un *proveedor* WMI.

</dd> </dl>

 

 
