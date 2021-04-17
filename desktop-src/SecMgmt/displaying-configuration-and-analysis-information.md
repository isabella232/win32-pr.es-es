---
description: La extensión del complemento debe mostrar la información de configuración y análisis actual a los usuarios.
ms.assetid: 503bc283-c1cd-4258-a27e-4046553882fa
title: Mostrar información de configuración y análisis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc2f0d598ced5f789d9b417d79df591a71f82ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688027"
---
# <a name="displaying-configuration-and-analysis-information"></a>Mostrar información de configuración y análisis

La extensión del complemento debe mostrar la información de configuración y análisis actual a los usuarios.

Para mostrar información, el nodo de extensión del complemento de datos adjuntos debe extender los complementos de configuración de seguridad mediante el nodo servicios. El nodo servicios es el complemento MMC que administra los servicios instalados en el sistema.

Los tipos de nodo que se pueden extender son los siguientes:

-   NodeType de servicios de configuración = {24a7f717-1f0c-11D1-affb-00c04fb984f9}
-   NodeType de servicios de inspección = {678050c7-1ff8-11D1-affb-00c04fb984f9}

Cuando se expande el nodo servicios, MMC notifica a todas las extensiones de complemento registradas. Cada complemento de datos adjuntos debe insertarse en el nodo servicios y realizar las tareas siguientes:

-   Llame a **QueryInterface** para obtener un puntero a la interfaz [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) expuesta por los complementos de configuración de seguridad.
-   Llame a [**ISceSvcAttachmentData:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) para informar a los complementos de configuración de seguridad que la extensión del complemento está cargada y para establecer un contexto para las comunicaciones.
-   Llame a [**ISceSvcAttachmentData:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) para recuperar la información de configuración de la base de datos. Este paso se puede realizar cuando la extensión del complemento se inicializa o cuando el usuario abre su nodo.

Para obtener más información, vea [Agregar un nodo de extensión del complemento de datos adjuntos](adding-an-attachment-snap-in-extension-node.md).

 

 



