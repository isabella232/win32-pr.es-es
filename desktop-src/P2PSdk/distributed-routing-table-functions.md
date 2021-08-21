---
description: La API de tabla de enrutamiento distribuido (DRT) utiliza las siguientes funciones.
ms.assetid: 1ceff217-d410-47fa-99a2-8588f001859e
title: Funciones de tabla de enrutamiento distribuido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00501a1a04a3acba23fe55f90acfbf7ca8fee7427c36ea1d36d8800fb8787321
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776355"
---
# <a name="distributed-routing-table-functions"></a>Funciones de tabla de enrutamiento distribuido

La API de tabla de enrutamiento distribuido (DRT) utiliza las siguientes funciones.

## <a name="lifetime-management-functions"></a>Funciones de administración de duración



| Función                                           | Descripción                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen)                         | Crea una instancia de DRT local con los criterios especificados por la [**estructura SETTINGS \_ de DRT.**](/windows/desktop/api/drt/ns-drt-drt_settings)  |
| [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose)                       | Cierra y quita la instancia local del DRT.                                                              |
| [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata)         | Recupera los datos de evento asociados a un evento señalado.                                                         |
| [**DrtGetEventDataSize**](/windows/desktop/api/drt/nf-drt-drtgeteventdatasize) | Devuelve el tamaño de la estructura [**DRT \_ EVENT \_ DATA**](/windows/desktop/api/drt/ns-drt-drt_event_data) asociada a un evento señalado. |



 

## <a name="module-management-functions"></a>Funciones de administración de módulos



| Función                                                                           | Descripción                                                                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**DrtCreatePnrpBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver)           | Crea un solucionador de arranque basado en el protocolo PNRP.                                                                              |
| [**DrtDeletePnrpBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtdeletepnrpbootstrapresolver)           | Elimina un solucionador de arranque basado en el protocolo PNRP.                                                                              |
| [**DrtCreateDnsBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtcreatednsbootstrapresolver)             | Crea un proveedor de arranque que se pondrá en contacto con un host conocido por su nombre.                                                             |
| [**DrtDeleteDnsBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtdeletednsbootstrapresolver)             | Elimina un proveedor de arranque que se pondrá en contacto con un host conocido por nombre.                                                             |
| [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)                     | Crea un transporte basado en el protocolo UDP IPv6.                                                                                   |
| [**DrtDeleteIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtdeleteipv6udptransport)                     | Elimina un transporte basado en el protocolo UDP IPv6.                                                                                   |
| [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) | Crea un proveedor de seguridad de claves derivadas para el DRT.                                                                                  |
| [**DrtCreateDerivedKey**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkey)                                 | Crea una clave que [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) puede usar cuando el DRT usa un proveedor de seguridad de claves derivado. |
| [**DrtDeleteDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider) | Elimina un proveedor de seguridad de claves derivadas para el DRT.                                                                                  |
| [**DrtCreateNullSecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider)             | Crea un proveedor de seguridad NULL. Este proveedor de seguridad no requiere nodos para autenticar claves.                                 |
| [**DrtDeleteNullSecurityProvider**](/windows/desktop/api/drt/nf-drt-drtdeletenullsecurityprovider)             | Elimina un proveedor de seguridad null.                                                                                                     |



 

## <a name="registration-functions"></a>Funciones de registro



| Función                                     | Descripción                                                    |
|----------------------------------------------|----------------------------------------------------------------|
| [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey)     | Registra una clave en el DRT.                                    |
| [**DrtUpdateKey**](/windows/desktop/api/drt/nf-drt-drtupdatekey)         | Actualiza los datos de aplicación asociados a una clave registrada. |
| [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) | Anula el registro de una clave del DRT.                                |



 

## <a name="search-functions"></a>Funciones de búsqueda



| Función                                                 | Descripción                                                                                                                                                                                                             |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch)                 | Busca una clave en el DRT con los criterios especificados en la [**estructura DE INFORMACIÓN DE BÚSQUEDA \_ \_ DE DRT.**](/windows/desktop/api/drt/ns-drt-drt_search_info)                                                                                                      |
| [**DrtContinueSearch**](/windows/desktop/api/drt/nf-drt-drtcontinuesearch)           | Continúa una búsqueda de DRT \_ SEARCH RETURN PATH para obtener una clave en el \_ \_ DRT. Esta función solo se usa cuando la **marca fIterative** se establece en **TRUE** en la estructura [**DE INFORMACIÓN DE BÚSQUEDA \_ \_ de DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) asociada. |
| [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)         | Recupera los resultados de la búsqueda.                                                                                                                                                                                         |
| [**DrtGetSearchResultSize**](/windows/desktop/api/drt/nf-drt-drtgetsearchresultsize) | Devuelve el tamaño del siguiente resultado de búsqueda disponible.                                                                                                                                                                   |
| [**DrtGetSearchPath**](/windows/desktop/api/drt/nf-drt-drtgetsearchpath)             | Devuelve una lista de nodos a los que se ha contactado durante la operación de búsqueda.                                                                                                                                                          |
| [**DrtGetSearchPathSize**](/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize)     | Devuelve el tamaño de la ruta de acceso de búsqueda, que representa el número de nodos utilizados en la operación de búsqueda.                                                                                                             |
| [**DrtEndSearch**](/windows/desktop/api/drt/nf-drt-drtendsearch)                     | Cancela una búsqueda de una clave en un DRT y, como resultado, se detiene la devolución de resultados a través de [**DRT \_ SEARCH \_ RESULT.**](/windows/desktop/api/drt/ns-drt-drt_search_result) Se puede llamar a esta API en cualquier momento después de emitir una búsqueda.              |



 

## <a name="instance-name-functions"></a>Funciones de nombre de instancia



| Función                                                 | Descripción                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**DrtGetInstanceName**](/windows/desktop/api/drt/nf-drt-drtgetinstancename)         | Obtiene el nombre asociado a una instancia de DRT.                    |
| [**DrtGetInstanceNameSize**](/windows/desktop/api/drt/nf-drt-drtgetinstancenamesize) | Devuelve el tamaño del nombre de instancia de tabla de enrutamiento distribuido. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumeraciones de tablas de enrutamiento distribuido](distributed-routing-table-enumerations.md)
</dt> <dt>

[Estructuras de tabla de enrutamiento distribuido](distributed-routing-table-structures.md)
</dt> <dt>

[Referencia de Table API enrutamiento distribuido](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



