---
description: Dado que WMI carga un proveedor de alto rendimiento en proceso en WMI o en una aplicación cliente, debe diseñar el proveedor de alto rendimiento como un servidor en proceso.
ms.assetid: c37e3652-8c76-4125-ba62-ae860858797e
ms.tgt_platform: multiple
title: Implementación de la interfaz High-Performance interfaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecec9a7b5e5399765adaa7a0e195825493d930ece46c30af3e788795fe08ebf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118108626"
---
# <a name="implementing-the-high-performance-interface"></a>Implementación de la interfaz High-Performance interfaz

Dado que WMI carga un proveedor de alto rendimiento en proceso en WMI o en una aplicación cliente, debe diseñar el proveedor de alto rendimiento como un servidor en proceso. Además, debe implementar los métodos de proveedor de alto rendimiento en las interfaces [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) [**e IWbemRefresher.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)

Debe implementar un proveedor de alto rendimiento como servidor en proceso. Una característica que debe tener en cuenta al implementar la seguridad de un servidor en proceso es cómo el proveedor identifica su propia ubicación. Cuando se carga en proceso en WMI, WMI crea una instancia del proveedor mediante un CLSID. Cuando se carga en proceso en una aplicación cliente, la aplicación cliente crea una instancia del proveedor con la **propiedad ClientLoadableCLSID.** Al proporcionar valores diferentes a un CLSID y a **ClientLoadableCLSID,** permite que el proveedor determine si se carga en proceso en WMI o en una aplicación cliente. Si se encuentra en un proceso WMI, el proveedor debe realizar cualquier suplantación de cliente necesaria mediante **ClientLoadableCLSID**. Si se encuentra en un proceso de cliente, el proveedor hereda el token de acceso del subproceso en el que se llama. Para obtener más información sobre cómo implementar un servidor en proceso, vea la [sección COM](https://msdn.microsoft.com/library/aa139695.aspx) de MSDN.

Como servidor en proceso, un proveedor de alto rendimiento usa un objeto de actualización para mantener los datos actualizados para el cliente remoto. En la tabla siguiente se enumeran los métodos que debe implementar para un proveedor de alto rendimiento.



| Método                                                                                              | Característica                                           |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [**IWbemHiPerfProvider::QueryInstances**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)                   | Consultas                                           |
| [**IWbemHiPerfProvider::GetObjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)                           | Recuperación de objetos                                  |
| [**IWbemHiPerfProvider::CreateRefresher**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)                 | Crea un actualizador.                               |
| [**IWbemHiPerfProvider::CreateRefreshableObject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject) | Crea un objeto de instancia actualizable.             |
| [**IWbemHiPerfProvider::CreateRefreshableEnum**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)     | Crea un enumerador actualizable                  |
| [**IWbemHiPerfProvider::StopRefreshing**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)                   | Detiene la actualización de un enumerador o un objeto de instancia |
| [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)                                           | Crea un actualizador.                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Convertir un proveedor de instancias en un High-Performance personalizado](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



