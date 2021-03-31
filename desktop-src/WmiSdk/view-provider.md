---
description: El proveedor de vistas es una instancia y un proveedor de métodos que crea nuevas clases basadas en instancias de otras clases.
ms.assetid: e1992e10-647b-4747-8f3d-b437ef7f3770
ms.tgt_platform: multiple
title: Ver proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e49154504dfb2f71ec19c2275851befbdbf9a48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911481"
---
# <a name="view-provider"></a>Ver proveedor

El proveedor de vistas es una instancia y un proveedor de métodos que crea nuevas clases basadas en instancias de otras clases. Puede usar el proveedor de vistas para tomar propiedades de diferentes clases de origen, espacios de nombres diferentes o equipos diferentes y combinar las propiedades como una sola clase.

Como proveedor de instancias y métodos, el proveedor de vistas admite la interfaz estándar [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) y los siguientes métodos [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) :

-   [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

Para obtener más información sobre los calificadores que se usan para definir las clases de proveedor de vistas, vea [calificadores específicos del proveedor de vistas](qualifiers-specific-to-the-view-provider.md).

Para obtener más información acerca de las vistas, vea [vincular clases juntas](linking-classes-together.md).

Dos versiones del proveedor de vistas están disponibles en las plataformas de 64 bits. Para obtener más información, consulte [obtener y proporcionar datos en un equipo de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md).

El proveedor de vistas se implementa en ViewProv.dll.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedores WMI](wmi-providers.md)
</dt> </dl>

 

 



