---
description: A continuación se indican las clases de COM+.
ms.assetid: 236725f6-16a3-4209-a9e3-a127c1d7243a
title: Clases COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626c3dfdae542b602cf27a8d8be5cb69dde5910f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153588"
---
# <a name="com-classes"></a>Clases COM+

A continuación se indican las clases de COM+.



| Clase                                                            | Descripción                                                                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppDomainHelper**](appdomainhelper.md)                       | Enlaza un objeto administrado a un dominio de aplicación, que es un entorno aislado donde se ejecutan las aplicaciones.                                                                                                                           |
| [**ClrAssemblyLocator**](clrassemblylocator.md)                 | Recupera información acerca de un ensamblado cuando se usa código administrado en el Common Language Runtime de .NET Framework.                                                                                                                          |
| [**CServiceConfig**](cserviceconfig.md)                         | Especifica y configura los servicios que deben estar activos en el dominio de servicio especificado al llamar a [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) o [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).                     |
| [**SecurityCallContext**](securitycallcontext.md)               | Proporciona acceso al contexto de seguridad de la llamada actual, que contiene información sobre los llamadores de un objeto.                                                                                                                           |
| [**SecurityCallers**](securitycallers.md)                       | Proporciona acceso a información sobre los llamadores individuales de una colección de llamadores. La colección representa la cadena de llamadas que finalizan con la llamada actual y cada llamador de la colección representa la identidad de un llamador. |
| [**SecurityIdentity**](securityidentity.md)                     | Proporciona acceso a una colección de información de seguridad que representa la identidad de un llamador. Con esta clase, puede encontrar información sobre un llamador determinado en una cadena de llamadores que forma parte del contexto de la llamada de seguridad.                 |
| [**SharedProperty**](sharedproperty.md)                         | Establece o recupera el valor de una propiedad compartida.                                                                                                                                                                                       |
| [**SharedPropertyGroup**](sharedpropertygroup.md)               | Crea y obtiene acceso a las propiedades compartidas de un grupo de propiedades compartidas.                                                                                                                                                                  |
| [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) | Crea grupos de propiedades compartidas y para obtener acceso a grupos de propiedades compartidas existentes.                                                                                                                                                 |
| [**TransactionContext**](transactioncontext.md)                 | Crea un objeto transaccional genérico que comienza una transacción.                                                                                                                                                                       |
| [**TransactionContextEx**](transactioncontextex.md)             | Crea un objeto transaccional genérico que comienza una transacción. Al llamar a los métodos de esta clase, puede crear el trabajo de varios objetos COM en una única transacción y confirmar o anular explícitamente la transacción.        |



 

 

 



