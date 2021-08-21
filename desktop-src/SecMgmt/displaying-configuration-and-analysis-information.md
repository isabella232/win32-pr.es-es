---
description: La extensión de complemento debe mostrar la información de configuración y análisis actual a los usuarios.
ms.assetid: 503bc283-c1cd-4258-a27e-4046553882fa
title: Mostrar información de configuración y análisis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33971f413058279aa840db4a61e529eb25ee7f317145a66bcb4474142a35c76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894788"
---
# <a name="displaying-configuration-and-analysis-information"></a>Mostrar información de configuración y análisis

La extensión de complemento debe mostrar la información de configuración y análisis actual a los usuarios.

Para mostrar información, el nodo de extensión del complemento de datos adjuntos debe extender los complementos de configuración de seguridad mediante el nodo Servicios . El nodo Servicios es el complemento MMC que administra los servicios instalados en el sistema.

Los tipos de nodo que se pueden extender son los siguientes:

-   Configuration Services NodeType={24a7f717-1f0c-11d1-affb-00c04fb984f9}
-   Inspection Services NodeType={678050c7-1ff8-11d1-affb-00c04fb984f9}

Cuando se expande el nodo Servicios, MMC notifica a todas las extensiones de complemento registradas. Cada complemento de datos adjuntos debe insertarse en el nodo Servicios y realizar las siguientes tareas:

-   Llame **a QueryInterface** para obtener un puntero a la [**interfaz ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) expuesta por los complementos de configuración de seguridad.
-   Llame a [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) para informar a los complementos de configuración de seguridad de que la extensión de complemento está cargada y establecer un contexto para las comunicaciones.
-   Llame [**a ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) para recuperar información de configuración de la base de datos. Este paso se puede realizar cuando la extensión de complemento se inicializa a sí misma o cuando el usuario abre su nodo.

Para obtener más información, vea [Agregar un nodo de extensión de complemento de datos adjuntos](adding-an-attachment-snap-in-extension-node.md).

 

 



