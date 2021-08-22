---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d426673b-dea2-4f8b-9259-6a17543f70c0
ms.tgt_platform: multiple
title: P (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230d3dba8be620b0d2d473dbf23960fff79cb7c76abc8a686c47a630605318d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050793"
---
# <a name="p-wmi"></a>P (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G H [](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) M [N](gloss-m.md) [O](gloss-n.md) [](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**contador de rendimiento**
</dt> <dd>

Propiedad de una clase de rendimiento derivada de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) que almacena datos de rendimiento.

</dd> <dt>

<span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**objeto de rendimiento**
</dt> <dd>

Objeto de una biblioteca de rendimiento que almacena datos en contadores. Estos objetos están visibles en la utilidad [*Monitor de*](gloss-s.md) sistema. Algunos ejemplos son los objetos Caché y Disco lógico. Cuando el proceso [*de ADAP*](gloss-a.md) transfiere a WMI, cada objeto se convierte en dos clases de rendimiento WMI. Una clase, que contiene datos sin procesar, se deriva de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata). La otra clase se deriva de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) y contiene los mismos datos visibles en el Monitor del sistema calculados por el proveedor cooked Counter.

</dd> <dt>

<span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**consumidor permanente**
</dt> <dd>

Consumidor [*de eventos*](gloss-e.md) cuyo registro dura hasta que se cancela explícitamente. Consulte también el [*consumidor temporal*](gloss-t.md).

</dd> <dt>

<span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**consumidor físico**
</dt> <dd>

Objeto COM implementado por un proveedor de consumidores [*de eventos*](gloss-e.md) que incluye un [*receptor*](gloss-s.md) para recibir notificaciones de eventos.

</dd> <dt>

<span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**Propiedad**
</dt> <dd>

Par nombre-valor que describe una unidad de datos para una clase. Los valores de propiedad deben tener un [*tipo de datos Managed Object Format (MOF)*](gloss-m.md) válido. Consulte también la [*propiedad de referencia*](gloss-r.md).

</dd> <dt>

<span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**proveedor de propiedades**
</dt> <dd>

Un servidor COM que admite la recuperación y modificación de propiedades WMI. Los proveedores de propiedades [**implementan las interfaces IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) [**e IWbemPropertyProvider.**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider)

</dd> <dt>

<span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**Proveedor**
</dt> <dd>

Un servidor COM que se comunica con objetos administrados para acceder a datos y notificaciones de eventos, como el registro o un dispositivo SNMP. Los proveedores reenvía estos datos al [*Administrador de objetos CIM*](gloss-c.md) integración e interpretación.

</dd> <dt>

<span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**método de proveedor**
</dt> <dd>

Método que implementa un *proveedor* WMI.

</dd> </dl>

 

 
