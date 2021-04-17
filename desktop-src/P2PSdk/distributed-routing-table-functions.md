---
description: La API de la tabla de enrutamiento distribuida (DRT) emplea las siguientes funciones.
ms.assetid: 1ceff217-d410-47fa-99a2-8588f001859e
title: Funciones de tabla de enrutamiento distribuido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd48c3a60f458285ce5f607f9ab6bcf7a557cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667445"
---
# <a name="distributed-routing-table-functions"></a>Funciones de tabla de enrutamiento distribuido

La API de la tabla de enrutamiento distribuida (DRT) emplea las siguientes funciones.

## <a name="lifetime-management-functions"></a>Funciones de administración de la duración



| Función                                           | Descripción                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen)                         | Crea una instancia de DRT local mediante los criterios especificados por la estructura de [**\_ configuración de DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .  |
| [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose)                       | Cierra y quita la instancia local de DRT.                                                              |
| [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata)         | Recupera los datos de evento asociados a un evento señalado.                                                         |
| [**DrtGetEventDataSize**](/windows/desktop/api/drt/nf-drt-drtgeteventdatasize) | Devuelve el tamaño de la estructura de [**\_ \_ datos de eventos de DRT**](/windows/desktop/api/drt/ns-drt-drt_event_data) asociada a un evento señalado. |



 

## <a name="module-management-functions"></a>Funciones de administración de módulos



| Función                                                                           | Descripción                                                                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**DrtCreatePnrpBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver)           | Crea una resolución de bootstrap basada en el protocolo PNRP.                                                                              |
| [**DrtDeletePnrpBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtdeletepnrpbootstrapresolver)           | Elimina una resolución de bootstrap basada en el protocolo PNRP.                                                                              |
| [**DrtCreateDnsBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtcreatednsbootstrapresolver)             | Crea un proveedor de arranque que se pondrá en contacto con un host conocido por nombre.                                                             |
| [**DrtDeleteDnsBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtdeletednsbootstrapresolver)             | Elimina un proveedor de arranque que se pondrá en contacto con un host conocido por nombre.                                                             |
| [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)                     | Crea un transporte basado en el protocolo UDP de IPv6.                                                                                   |
| [**DrtDeleteIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtdeleteipv6udptransport)                     | Elimina un transporte basado en el protocolo UDP de IPv6.                                                                                   |
| [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) | Crea un proveedor de seguridad de clave derivada para DRT.                                                                                  |
| [**DrtCreateDerivedKey**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkey)                                 | Crea una clave que puede ser utilizada por [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) cuando DRT usa un proveedor de seguridad de clave derivado. |
| [**DrtDeleteDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider) | Elimina un proveedor de seguridad de clave derivada para DRT.                                                                                  |
| [**DrtCreateNullSecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider)             | Crea un proveedor de seguridad null. Este proveedor de seguridad no requiere que los nodos autentiquen las claves.                                 |
| [**DrtDeleteNullSecurityProvider**](/windows/desktop/api/drt/nf-drt-drtdeletenullsecurityprovider)             | Elimina un proveedor de seguridad null.                                                                                                     |



 

## <a name="registration-functions"></a>Funciones de registro



| Función                                     | Descripción                                                    |
|----------------------------------------------|----------------------------------------------------------------|
| [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey)     | Registra una clave en la DRT.                                    |
| [**DrtUpdateKey**](/windows/desktop/api/drt/nf-drt-drtupdatekey)         | Actualiza los datos de aplicación asociados a una clave registrada. |
| [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) | Anula el registro de una clave de DRT.                                |



 

## <a name="search-functions"></a>Funciones de búsqueda



| Función                                                 | Descripción                                                                                                                                                                                                             |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch)                 | Busca una clave en el DRT mediante los criterios especificados en la estructura de [**\_ \_ información de búsqueda de DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) .                                                                                                      |
| [**DrtContinueSearch**](/windows/desktop/api/drt/nf-drt-drtcontinuesearch)           | Continúa una \_ \_ \_ búsqueda de la ruta de acceso de retorno de búsqueda de DRT para una clave en la DRT. Esta función solo se usa cuando la marca **fIterative** está establecida en **true** en la estructura [**de \_ \_ información de búsqueda de DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) asociada. |
| [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)         | Recupera los resultados de la búsqueda.                                                                                                                                                                                         |
| [**DrtGetSearchResultSize**](/windows/desktop/api/drt/nf-drt-drtgetsearchresultsize) | Devuelve el tamaño del siguiente resultado de búsqueda disponible.                                                                                                                                                                   |
| [**DrtGetSearchPath**](/windows/desktop/api/drt/nf-drt-drtgetsearchpath)             | Devuelve una lista de nodos contactados durante la operación de búsqueda.                                                                                                                                                          |
| [**DrtGetSearchPathSize**](/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize)     | Devuelve el tamaño de la ruta de acceso de búsqueda, que representa el número de nodos que se usan en la operación de búsqueda.                                                                                                             |
| [**DrtEndSearch**](/windows/desktop/api/drt/nf-drt-drtendsearch)                     | Cancela una búsqueda de una clave en un DRT y, como resultado, se detiene el [**\_ \_ resultado**](/windows/desktop/api/drt/ns-drt-drt_search_result) de la devolución de resultados a través de la búsqueda de DRT. Se puede llamar a esta API en cualquier momento después de la emisión de una búsqueda.              |



 

## <a name="instance-name-functions"></a>Funciones de nombre de instancia



| Función                                                 | Descripción                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**DrtGetInstanceName**](/windows/desktop/api/drt/nf-drt-drtgetinstancename)         | Obtiene el nombre asociado a una instancia de DRT.                    |
| [**DrtGetInstanceNameSize**](/windows/desktop/api/drt/nf-drt-drtgetinstancenamesize) | Devuelve el tamaño del nombre de la instancia de la tabla de enrutamiento distribuido. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumeraciones de tabla de enrutamiento distribuido](distributed-routing-table-enumerations.md)
</dt> <dt>

[Estructuras de tabla de enrutamiento distribuido](distributed-routing-table-structures.md)
</dt> <dt>

[Referencia de Table API de enrutamiento distribuido](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



