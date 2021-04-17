---
description: Dado que WMI carga un proveedor de alto rendimiento en el proceso en WMI o en una aplicación cliente, debe diseñar el proveedor de alto rendimiento como un servidor en proceso.
ms.assetid: c37e3652-8c76-4125-ba62-ae860858797e
ms.tgt_platform: multiple
title: Implementar la interfaz High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea6e7f75e1031caacbb7379fba025baceb7b1a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697422"
---
# <a name="implementing-the-high-performance-interface"></a>Implementar la interfaz High-Performance

Dado que WMI carga un proveedor de alto rendimiento en el proceso en WMI o en una aplicación cliente, debe diseñar el proveedor de alto rendimiento como un servidor en proceso. Además, debe implementar los métodos de proveedor de alto rendimiento en las interfaces [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) e [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) .

Debe implementar un proveedor de alto rendimiento como un servidor en proceso. Una característica que debe tener en cuenta al implementar la seguridad de un servidor en proceso es cómo el proveedor identifica su propia ubicación. Cuando se carga en proceso en WMI, WMI crea instancias del proveedor mediante un CLSID. Cuando se carga en proceso en una aplicación cliente, la aplicación cliente crea una instancia del proveedor con la propiedad **ClientLoadableCLSID** . Al asignar valores diferentes a un CLSID y a un **ClientLoadableCLSID**, se permite al proveedor determinar si se carga en proceso en WMI o en una aplicación cliente. Si se encuentra en un proceso WMI, el proveedor debe realizar cualquier suplantación de cliente necesaria mediante **ClientLoadableCLSID**. Si se encuentra en un proceso de cliente, el proveedor hereda el token de acceso del subproceso en el que se llama. Para obtener más información sobre cómo implementar un servidor en proceso, vea la [sección com](https://msdn.microsoft.com/library/aa139695.aspx) de MSDN.

Como servidor en proceso, un proveedor de alto rendimiento usa un objeto actualizador para mantener los datos actualizados para el cliente remoto. En la tabla siguiente se enumeran los métodos que debe implementar para un proveedor de alto rendimiento.



| Método                                                                                              | Característica                                           |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [**IWbemHiPerfProvider:: QueryInstances**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)                   | Consultas                                           |
| [**IWbemHiPerfProvider:: GetObjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)                           | Recuperación de objetos                                  |
| [**IWbemHiPerfProvider:: CreateRefresher**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)                 | Crea un actualizador                               |
| [**IWbemHiPerfProvider:: CreateRefreshableObject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject) | Crea un objeto de instancia actualizable.             |
| [**IWbemHiPerfProvider:: CreateRefreshableEnum**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)     | Crea un enumerador actualizable                  |
| [**IWbemHiPerfProvider:: StopRefreshing**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)                   | Detiene la actualización de un enumerador o un objeto de instancia |
| [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)                                           | Crea un actualizador                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear un proveedor de instancias en un proveedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



