---
description: El proveedor view es un proveedor de instancias y métodos que crea nuevas clases basadas en instancias de otras clases.
ms.assetid: e1992e10-647b-4747-8f3d-b437ef7f3770
ms.tgt_platform: multiple
title: Proveedor de vistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e49154504dfb2f71ec19c2275851befbdbf9a48
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889169"
---
# <a name="view-provider"></a>Proveedor de vistas

El proveedor view es un proveedor de instancias y métodos que crea nuevas clases basadas en instancias de otras clases. Puede usar el proveedor view para tomar propiedades de diferentes clases de origen, espacios de nombres diferentes o equipos diferentes y combinar las propiedades como una sola clase.

Como proveedor de instancias y métodos, el proveedor view admite la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) estándar y los siguientes [**métodos IWbemServices:**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)

-   [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

Para obtener más información sobre los calificadores que se usan para definir clases de proveedor de vistas, vea [Calificadores específicos del proveedor de vistas](qualifiers-specific-to-the-view-provider.md).

Para obtener más información sobre las vistas, vea [Vincular clases juntas.](linking-classes-together.md)

Hay dos versiones del proveedor view disponibles en plataformas de 64 bits. Para obtener más información, vea Obtener y proporcionar datos en un equipo [de 64 bits.](getting-and-providing-data-on-a-64-bit-computer.md)

El proveedor de vistas se implementa en ViewProv.dll.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedores WMI](wmi-providers.md)
</dt> </dl>

 

 



