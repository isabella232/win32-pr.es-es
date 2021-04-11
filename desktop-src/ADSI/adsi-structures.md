---
title: Estructuras ADSI
description: Active Directory interfaces de servicio (ADSI) definen y usan las estructuras que se muestran en la tabla siguiente.
ms.assetid: 3ee0e469-9932-4135-8798-27d318011786
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, referencia, estructuras
- ADSI de estructuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f35ba74f0334e8b66329d8f526266c315056af9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148741"
---
# <a name="adsi-structures"></a>Estructuras ADSI

Active Directory interfaces de servicio (ADSI) definen y usan las estructuras que se muestran en la tabla siguiente.



| Estructura                                                                      | Descripción                                                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**ADS \_ ATTR \_ Def**](/windows/desktop/api/Iads/ns-iads-ads_attr_def)<br/>                              | Describe un conjunto de definiciones de atributo de un objeto **attributeSchema** .<br/>                          |
| [**\_información de atributos de ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)<br/>                            | Contiene el valor de un atributo con nombre y especifica las operaciones para modificar el atributo.<br/>              |
| [**\_BACKLINK ADS**](/windows/win32/api/iads/ns-iads-ads_backlink)<br/>                               | Representa una representación ADSI del atributo de **vínculo hacia atrás** .<br/>                                   |
| [**\_lista CASEIGNORE \_ ADS**](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)<br/>                | Representa una representación ADSI del atributo de **lista de omisión de mayúsculas y minúsculas** .<br/>                            |
| [**ADS ( \_ clase) \_ Def**](/windows/desktop/api/Iads/ns-iads-ads_class_def)<br/>                            | Describe los datos de esquema de un objeto.<br/>                                                                |
| [**\_DN \_ de ADS con \_ binario**](/windows/win32/api/iads/ns-iads-ads_dn_with_binary)<br/>                 | Estructura definida por ADSI que asigna un nombre distintivo a un **GUID** del objeto.<br/>                     |
| [**\_DN \_ de ADS con \_ cadena**](/windows/win32/api/iads/ns-iads-ads_dn_with_string)<br/>                 | Estructura definida por ADSI que asigna un nombre distintivo de un objeto a un valor de cadena que no varía.<br/> |
| [**\_correo electrónico de ADS**](/windows/win32/api/iads/ns-iads-ads_email)<br/>                                     | Representa una representación ADSI del atributo de **correo electrónico** .<br/>                                       |
| [**\_FAXNUMBER ADS**](/windows/win32/api/iads/ns-iads-ads_faxnumber)<br/>                             | Representa una representación ADSI del atributo de **número de teléfono de fax** .<br/>                  |
| [**suspensión de anuncios \_**](/windows/win32/api/iads/ns-iads-ads_hold)<br/>                                       | Representa una representación ADSI del atributo **Hold** .<br/>                                        |
| [**\_NETADDRESS ADS**](/windows/win32/api/iads/ns-iads-ads_netaddress)<br/>                           | Representa una representación ADSI del atributo de **dirección de red** .<br/>                                 |
| [**descriptor de seguridad de ADS \_ NT \_ \_**](/windows/win32/api/iads/ns-iads-ads_nt_security_descriptor)<br/> | Describe un descriptor de seguridad.<br/>                                                                    |
| [**\_información del objeto ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_object_info)<br/>                        | Describe los datos del objeto de servicio de directorio.<br/>                                                            |
| [**\_lista de octetos de ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_octet_list)<br/>                          | Representa una representación ADSI del atributo de **lista de octetos** .<br/>                                  |
| [**\_cadena de octetos de ADS \_**](/windows/win32/api/iads/ns-iads-ads_octet_string)<br/>                      | Representa una representación ADSI del atributo de **cadena de octeto** .<br/>                                |
| [**Ruta de ADS \_**](/windows/win32/api/iads/ns-iads-ads_path)<br/>                                       | Representa una representación ADSI del atributo **path** .<br/>                                        |
| [**\_POSTALADDRESS ADS**](/windows/win32/api/iads/ns-iads-ads_postaladdress)<br/>                     | Representa una representación ADSI del atributo de **dirección postal** .<br/>                              |
| [**específico de los anuncios \_ \_**](/windows/win32/api/iads/ns-iads-ads_prov_specific)<br/>                    | Describe un tipo de datos específico del proveedor.<br/>                                                            |
| [**\_REPLICAPOINTER ADS**](/windows/win32/api/iads/ns-iads-ads_replicapointer)<br/>                   | Representa una representación ADSI del atributo de puntero de réplica.<br/>                                 |
| [**\_columna de búsqueda de anuncios \_**](/windows/desktop/api/Iads/ns-iads-ads_search_column)<br/>                    | Representa una columna resultante de una consulta de directorio.<br/>                                               |
| [**\_información de SEARCHPREF ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)<br/>                | Describe las preferencias de consulta.<br/>                                                                        |
| [**SORTKEY de ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_sortkey)<br/>                                 | Describe la clave de ordenación utilizada para ordenar una consulta.<br/>                                                    |
| [**marca de tiempo de ADS \_**](/windows/win32/api/iads/ns-iads-ads_timestamp)<br/>                             | Representa una representación ADSI del atributo **timestamp** .<br/>                                   |
| [**\_TYPEDNAME ADS**](/windows/win32/api/iads/ns-iads-ads_typedname)<br/>                             | Representa una representación ADSI del atributo de **nombre con tipo** .<br/>                                  |
| [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)<br/>                                        | Describe el valor de un tipo de datos ADSI.<br/>                                                           |
| [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv)<br/>                                         | Especifica que se debe usar la vista de lista virtual al devolver los resultados de la búsqueda del servidor.<br/>  |



 

 

 





