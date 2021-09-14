---
description: Las siguientes son las clases COM+.
ms.assetid: 236725f6-16a3-4209-a9e3-a127c1d7243a
title: Clases COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626c3dfdae542b602cf27a8d8be5cb69dde5910f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072996"
---
# <a name="com-classes"></a>Clases COM+

Las siguientes son las clases COM+.



| Clase                                                            | Descripción                                                                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppDomainHelper**](appdomainhelper.md)                       | Enlaza un objeto administrado a un dominio de aplicación, que es un entorno aislado donde se ejecutan las aplicaciones.                                                                                                                           |
| [**ClrAssemblyLocator**](clrassemblylocator.md)                 | Recupera información sobre un ensamblado cuando se usa código administrado en la .NET Framework Common Language Runtime.                                                                                                                          |
| [**CServiceConfig**](cserviceconfig.md)                         | Especifica y configura los servicios que deben estar activos en el dominio de servicio especificado al llamar a [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) o [**CoEnterServiceDomain.**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)                     |
| [**SecurityCallContext**](securitycallcontext.md)               | Proporciona acceso al contexto de seguridad de la llamada actual, que contiene información sobre los llamadores de un objeto.                                                                                                                           |
| [**SecurityCallers**](securitycallers.md)                       | Proporciona acceso a información sobre los llamadores individuales de una colección de llamadores. La colección representa la cadena de llamadas que termina con la llamada actual y cada llamador de la colección representa la identidad de un llamador. |
| [**SecurityIdentity**](securityidentity.md)                     | Proporciona acceso a una colección de información de seguridad que representa la identidad de un autor de la llamada. Con esta clase, puede averiguar sobre un llamador determinado en una cadena de llamadores que forma parte del contexto de llamada de seguridad.                 |
| [**SharedProperty**](sharedproperty.md)                         | Establece o recupera el valor de una propiedad compartida.                                                                                                                                                                                       |
| [**SharedPropertyGroup**](sharedpropertygroup.md)               | Crea y accede a las propiedades compartidas en un grupo de propiedades compartidas.                                                                                                                                                                  |
| [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) | Crea grupos de propiedades compartidas y para obtener acceso a los grupos de propiedades compartidos existentes.                                                                                                                                                 |
| [**TransactionContext**](transactioncontext.md)                 | Crea un objeto transaccional genérico que comienza una transacción.                                                                                                                                                                       |
| [**TransactionContextEx**](transactioncontextex.md)             | Crea un objeto transaccional genérico que comienza una transacción. Al llamar a los métodos de esta clase, puede crear el trabajo de varios objetos COM en una sola transacción y confirmar o anular explícitamente la transacción.        |



 

 

 



