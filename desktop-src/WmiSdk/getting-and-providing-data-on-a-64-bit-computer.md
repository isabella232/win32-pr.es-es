---
description: Las aplicaciones cliente y los scripts que tienen acceso a los proveedores estándar de 32 bits de WMI continúan funcionando con normalidad cuando se ejecutan en un sistema operativo de 64 bits.
ms.assetid: 68819bea-a48d-4de1-a50d-f03ae04775f5
ms.tgt_platform: multiple
title: Obtener y proporcionar datos en un equipo de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7d8ff5430a7c47b652bfbcca05d2f53ba857d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567121"
---
# <a name="getting-and-providing-data-on-a-64-bit-computer"></a>Obtener y proporcionar datos en un equipo de 64 bits

Las aplicaciones cliente y los scripts que tienen acceso a los proveedores estándar de 32 bits de WMI continúan funcionando con normalidad cuando se ejecutan en un sistema operativo de 64 bits. Solo dos proveedores preinstalados, el [proveedor del registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) y el [proveedor de vistas](view-provider.md), tienen versiones de 64 bits que se ejecutan en paralelo con las versiones de 32 bits. Sin embargo, una aplicación de 32 bits que solicita instancias de Modelo de controlador de Windows de 32 bits (WDM) recibe las instancias de la clase WDM de 64 bits predeterminada en un sistema operativo de 64 bits.

## <a name="accessing-default-and-nondefault-provider-data"></a>Acceder a los datos de proveedor predeterminados y no predeterminados

Por lo general, los escritores de proveedores no incluyen las versiones de 32 y 64 bits de un proveedor en el mismo sistema operativo. Si no existe ningún proveedor de 64 bits, un proveedor de 32 bits puede continuar ejecutándose a través de las funciones de WOW64. Un proveedor de 64 bits puede proporcionar igualmente datos a una aplicación de 32 bits. Para obtener más información, vea [proporcionar datos WMI en una plataforma de 64 bits](providing-wmi-data-on-a-64-bit-platform.md).

Si existen dos versiones, las aplicaciones cliente y los scripts pueden usar los parámetros de contexto disponibles en la [API de com](com-api-for-wmi.md) y la [API de scripting](scripting-api-for-wmi.md) para conectarse explícitamente a un proveedor de WMI específico no predeterminado, si está disponible. Para obtener más información, consulte [solicitar datos WMI en una plataforma de 64 bits](requesting-wmi-data-on-a-64-bit-platform.md).

En el diagrama siguiente se muestran las conexiones predeterminadas y no predeterminadas, utilizando el registro como ejemplo para el que dos proveedores pueden existir en paralelo en una plataforma de 64 bits.

![conexiones predeterminadas y no predeterminadas en una plataforma de 64 bits](images/32-64bit-registry.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitar datos WMI en una plataforma de 64 bits](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[Proporcionar datos WMI en una plataforma de 64 bits](providing-wmi-data-on-a-64-bit-platform.md)
</dt> </dl>

 

 
