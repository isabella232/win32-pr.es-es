---
description: Al usar el servicio de eventos COM+, hay pasos que puede seguir para asegurarse de que la información confidencial contenida en un evento no se ve comprometida.
ms.assetid: 1f8faea0-afc2-4999-a962-d6fd10307d6c
title: Consideraciones de seguridad de eventos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f5c7dada980046627e9b778fd56e3e2727060
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000843"
---
# <a name="com-events-security-considerations"></a>Consideraciones de seguridad de eventos COM+

Al usar el servicio de eventos COM+, hay pasos que puede seguir para asegurarse de que la información confidencial contenida en un evento no se ve comprometida.

Los publicadores de eventos deben tener en cuenta que cualquier parte que pueda escribir en el catálogo de COM+ puede suscribirse a sus eventos. Por consiguiente, si la información contenida en un objeto de clase de eventos es confidencial, debe utilizar la herramienta de administración de servicios de componentes para comprobar que las comunicaciones con los suscriptores están cifradas para la aplicación que contiene los componentes de la clase de evento. (En la ficha **seguridad** de la hoja de propiedades de la aplicación com+, seleccione **privacidad de paquete** como el **nivel de autenticación para llamadas** ). Además, debe utilizar [filtros de eventos](filtering-events-in-com-.md) para asegurarse de que los eventos se entreguen solo a los suscriptores correspondientes.

Los suscriptores de eventos deberían tener en cuenta que un usuario malintencionado con acceso a la red y el conocimiento del objeto de la clase de evento podría crear eventos falsos. Por lo tanto, debe utilizar [la seguridad basada en roles](role-based-security-administration.md) para asegurarse de que los llamadores de los métodos del objeto de la clase de evento tienen las credenciales adecuadas para realizar las acciones descritas por su implementación.

Para ayudar a proteger a los publicadores y suscriptores, utilice el servicio de eventos COM+ en una red privada de hosts de confianza que está aislado de Internet por un firewall.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad de COM+](com--security.md)
</dt> <dt>

[Filtrado de eventos en COM+](filtering-events-in-com-.md)
</dt> <dt>

[Objeto de la clase de eventos COM+](the-com--event-class-object.md)
</dt> </dl>

 

 



