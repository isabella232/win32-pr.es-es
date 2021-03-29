---
description: Las interfaces COM multidifusión permiten el acceso a la instalación de redes para asignar, renovar y liberar concesiones en direcciones de multidifusión.
ms.assetid: d4da9616-bdb4-4919-96aa-9e45582b05dd
title: Interfaces COM multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01370372e3ea05b27dc789f90918b148075c28f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808299"
---
# <a name="multicast-com-interfaces"></a>Interfaces COM multidifusión

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

Las interfaces COM multidifusión permiten el acceso a la instalación de la red para asignar, renovar y liberar concesiones en direcciones de multidifusión. Encapsulan un conjunto de definiciones de la estructura de datos y la función. Las interfaces COM liberan al programador de la carga de comprender y manipular estas estructuras de datos. Además, dado que el propio TAPI 3 está basado en COM, estas interfaces hacen que se pueda tener acceso a la asignación de direcciones de multidifusión de forma coherente con el resto de los recursos proporcionados por TAPI 3. Las aplicaciones escritas con Visual Basic, Java o lenguajes de scripting que normalmente no pueden tener acceso directamente a la API de Windows pueden utilizar estas interfaces.

La asignación de direcciones de multidifusión es actualmente el asunto de un grupo de trabajo de IETF. Para obtener acceso a la información actual, consulte "MDHCP" o "MADCAP" y "borrador de Internet" mediante cualquier motor de búsqueda de Internet. Además de MADCAP, la arquitectura propuesta incluye un protocolo para la coordinación entre servidores en un dominio o como, así como un protocolo para la coordinación entre dominios. Aunque esta arquitectura está evolucionando actualmente, el cliente no tiene que preocuparse por los detalles de este esquema.

Actualmente, este componente solo admite direcciones IP versión 4.

> [!Note]  
> El protocolo utilizado para estas interfaces se llama actualmente MADCAP. En versiones anteriores, se conocía como MDHCP.

 

El objeto de multidifusión se crea llamando a **CoCreateInstance** en la interfaz [**IMcastAddressAllocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation) . La interfaz **IMcastAddressAllocation** expone el método [**EnumerateScopes**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes) , que permite a una aplicación obtener una lista de todos los ámbitos de multidifusión disponibles.

Una vez que se ha obtenido un ámbito de trabajo, se usa el método [**RequestAddress**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-requestaddress) para solicitar una dirección de multidifusión desde el servidor. Si la solicitud es correcta, se devuelve un puntero [**IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo) . El método [**EnumerateAddresses**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastleaseinfo-enumerateaddresses) expuesto por esta interfaz se puede usar para obtener las direcciones.

Cada objeto multimedia asociado a la Conferencia expone una interfaz [**ITConnection**](itconnection.md) . El método [**ITConnection:: SetAddressInfo**](itconnection-setaddressinfo.md) permite la asignación de las direcciones de multidifusión obtenidas en el medio de la Conferencia. La dirección debe establecerse para cada interfaz **ITConnection** de cada objeto multimedia asociado a la Conferencia.

 

 



