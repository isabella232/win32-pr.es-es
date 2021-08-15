---
description: Las aplicaciones cliente y los scripts que acceden a proveedores estándar de WMI de 32 bits siguen funcionando con normalidad cuando se ejecutan en un sistema operativo de 64 bits.
ms.assetid: 68819bea-a48d-4de1-a50d-f03ae04775f5
ms.tgt_platform: multiple
title: Obtener y proporcionar datos en un equipo de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46163290d1212fd66bef48dba177034769360e8d7c6249dfdf40327ce2adc32c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819388"
---
# <a name="getting-and-providing-data-on-a-64-bit-computer"></a>Obtener y proporcionar datos en un equipo de 64 bits

Las aplicaciones cliente y los scripts que acceden a proveedores estándar de WMI de 32 bits siguen funcionando con normalidad cuando se ejecutan en un sistema operativo de 64 bits. Solo dos proveedores preinstalados, el proveedor del Registro del sistema y el proveedor de vistas [,](view-provider.md)tienen versiones de 64 bits que se ejecutan en paralelo con las versiones de 32 bits. [](/previous-versions/windows/desktop/regprov/system-registry-provider) Sin embargo, una aplicación de 32 bits que solicita instancias de Windows Driver Model (WDM) de 32 bits recibe las instancias predeterminadas de la clase WDM de 64 bits en un sistema operativo de 64 bits.

## <a name="accessing-default-and-nondefault-provider-data"></a>Acceso a datos de proveedor predeterminados y no predeterminados

Por lo general, los escritores de proveedores no incluyen las versiones de 32 y 64 bits de un proveedor en el mismo sistema operativo. Si no existe ningún proveedor de 64 bits, un proveedor de 32 bits puede seguir funcionando a través de las instalaciones de WOW64. Un proveedor de 64 bits también puede proporcionar datos a una aplicación de 32 bits. Para obtener más información, vea Proporcionar datos WMI en una plataforma [de 64 bits.](providing-wmi-data-on-a-64-bit-platform.md)

Si existen dos versiones, las aplicaciones cliente y los scripts pueden usar los parámetros de contexto disponibles en la [API COM](com-api-for-wmi.md) y [scripting API](scripting-api-for-wmi.md) para conectarse explícitamente a un proveedor WMI no predeterminado específico, si está disponible. Para obtener más información, vea Solicitud de datos WMI en una plataforma [de 64 bits.](requesting-wmi-data-on-a-64-bit-platform.md)

En el diagrama siguiente se muestran las conexiones predeterminadas y no predeterminadas, usando el Registro como ejemplo para el que pueden existir dos proveedores en paralelo en una plataforma de 64 bits.

![conexiones predeterminadas y no predeterminadas en una plataforma de 64 bits](images/32-64bit-registry.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitud de datos WMI en una plataforma de 64 bits](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[Proporcionar datos WMI en una plataforma de 64 bits](providing-wmi-data-on-a-64-bit-platform.md)
</dt> </dl>

 

 
