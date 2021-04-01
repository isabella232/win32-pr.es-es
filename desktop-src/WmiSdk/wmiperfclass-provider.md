---
description: A partir de Windows Vista, este proveedor crea las clases de contador de rendimiento de WMI.
ms.assetid: 5bb3d5e0-cdeb-4fea-a8ca-cf934e056206
ms.tgt_platform: multiple
title: Proveedor WmiPerfClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941422211ac9892406181ac0271e0d50239eef1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082752"
---
# <a name="wmiperfclass-provider"></a>Proveedor WmiPerfClass

A partir de Windows Vista, este proveedor crea las [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes)de WMI. El proveedor [WMIPerfInst](wmiperfinst-provider.md) proporciona los datos de forma dinámica a estas clases de rendimiento de WMI. El proceso de detección automática/purga (ADAP) ya no transfiere objetos de contador de rendimiento a clases de rendimiento de WMI en el repositorio WMI. Para obtener más información, consulte [bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md).

Para obtener más información, consulte [bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md).

Aunque no se recomienda desarrollar nuevos objetos de rendimiento mediante la creación de un proveedor de alto rendimiento de WMI y depender del proceso del [*adaptador de ADAP inverso*](gloss-r.md) para transferir los datos a las bibliotecas de rendimiento, la excepción es el desarrollo de un controlador de modelo de controlador de Windows que proporciona datos de rendimiento. Aunque el proceso de adaptador inverso sigue funcionando por compatibilidad con versiones anteriores, el método recomendado es usar los [contadores de rendimiento versión 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).

El nombre de instancia [**\_ \_ Win32Provider**](--win32provider.md) de este proveedor es "WmiPerfClass".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedores WMI](wmi-providers.md)
</dt> <dt>

[Bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> </dl>

 

 
