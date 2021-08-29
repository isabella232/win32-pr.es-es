---
description: Al usar el servicio de eventos COM+, hay pasos que puede seguir para asegurarse de que cualquier información confidencial contenida en un evento no se ve comprometida.
ms.assetid: 1f8faea0-afc2-4999-a962-d6fd10307d6c
title: Consideraciones de seguridad de eventos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5cfd55d901d2583a7c570dcd378ab7750e15bd03adc61ad709c76e67076efae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096905"
---
# <a name="com-events-security-considerations"></a>Consideraciones de seguridad de eventos COM+

Al usar el servicio de eventos COM+, hay pasos que puede seguir para asegurarse de que cualquier información confidencial contenida en un evento no se ve comprometida.

Los publicadores de eventos deben tener en cuenta que cualquier entidad que pueda escribir en el catálogo de COM+ puede suscribirse a los eventos. Por lo tanto, si la información contenida en un objeto de clase de eventos es confidencial, debe usar la herramienta de administración servicios de componentes para comprobar que las comunicaciones con los suscriptores están cifradas para la aplicación que contiene los componentes de la clase de eventos. (En la **pestaña Seguridad de** la hoja de propiedades de la aplicación COM+, seleccione Privacidad **de** paquetes como nivel de autenticación **para llamadas).** Además, debe usar filtros [de eventos para](filtering-events-in-com-.md) ayudar a garantizar que los eventos solo se entregan a los suscriptores adecuados.

Los suscriptores de eventos deben tener en cuenta que una entidad malintencionada con acceso a la red y conocimiento del objeto de clase de eventos podría crear eventos falsos. Por lo [](role-based-security-administration.md) tanto, debe usar la seguridad basada en roles para ayudar a garantizar que los llamadores de los métodos del objeto de clase de eventos tienen las credenciales adecuadas para realizar las acciones descritas por la implementación.

Para ayudar a proteger a los publicadores y suscriptores, use el servicio eventos COM+ en una red privada de hosts de confianza aislados de Internet mediante un firewall.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad de COM+](com--security.md)
</dt> <dt>

[Filtrado de eventos en COM+](filtering-events-in-com-.md)
</dt> <dt>

[El objeto de clase de eventos COM+](the-com--event-class-object.md)
</dt> </dl>

 

 



