---
description: Las interfaces COM de multidifusión permiten el acceso a la instalación de redes para asignar, renovar y liberar concesiones en direcciones de multidifusión.
ms.assetid: d4da9616-bdb4-4919-96aa-9e45582b05dd
title: Interfaces COM de multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01370372e3ea05b27dc789f90918b148075c28f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361762"
---
# <a name="multicast-com-interfaces"></a>Interfaces COM de multidifusión

\[Los controles e interfaces de la conferencia de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

Las interfaces COM de multidifusión permiten el acceso a las instalaciones de la red para asignar, renovar y liberar concesiones en direcciones de multidifusión. Encapsulan un conjunto de definiciones de función y estructura de datos. Las interfaces COM liberan al programador de la carga de comprender y manipular estas estructuras de datos. Además, dado que TAPI 3 está basado en COM, estas interfaces hacen que la asignación de direcciones de multidifusión sea accesible de forma coherente con las demás instalaciones proporcionadas por TAPI 3. Las aplicaciones escritas mediante Visual Basic, Java o lenguajes de scripting que normalmente no pueden acceder directamente a Windows API pueden usar estas interfaces.

La asignación de direcciones de multidifusión es actualmente el asunto de un grupo de trabajo de IETF. Para acceder a la información actual, consulte "MDHCP" o "MADCAP" y "Borrador de Internet" mediante cualquier motor de búsqueda de Internet. Además de MADCAP, la arquitectura propuesta incluye un protocolo para la coordinación de servidor a servidor dentro de un dominio o AS, así como un protocolo para la coordinación entre dominios. Aunque esta arquitectura está evolucionando actualmente, el cliente no necesita preocuparse por los detalles de este esquema.

Actualmente, este componente solo admite direcciones IP de la versión 4.

> [!Note]  
> El protocolo usado para estas interfaces se denomina actualmente MADCAP. En versiones anteriores se conocía como MDHCP.

 

El objeto de multidifusión se crea mediante una llamada **a CoCreateInstance** en la [**interfaz IMcastAddressAllocation.**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation) La **interfaz IMcastAddressAllocation** expone el método [**EnumerateScopes,**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes) que permite a una aplicación obtener una lista de todos los ámbitos de multidifusión disponibles.

Una vez que se ha obtenido un ámbito de trabajo, el [**método RequestAddress**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-requestaddress) se usa para solicitar una dirección de multidifusión del servidor. Si la solicitud se realiza correctamente, se devuelve un puntero [**IMcastLeaseInfo.**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo) A continuación, se puede usar el [**método EnumerateAddresses**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastleaseinfo-enumerateaddresses) expuesto por esta interfaz para obtener las direcciones.

Cada objeto Media asociado a la conferencia expone una [**interfaz ITConnection.**](itconnection.md) El [**método ITConnection::SetAddressInfo**](itconnection-setaddressinfo.md) permite la asignación de las direcciones de multidifusión obtenidas a los medios de la conferencia. La dirección debe establecerse para cada **interfaz ITConnection** de cada objeto Media asociado a la conferencia.

 

 



