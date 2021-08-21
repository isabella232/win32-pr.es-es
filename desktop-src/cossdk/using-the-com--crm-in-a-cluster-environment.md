---
description: Uso de COM+ CRM en un entorno de clúster
ms.assetid: 753461c5-880c-4df0-b552-b962dc06524f
title: Uso de COM+ CRM en un entorno de clúster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31a2d0800f98c9453e7d4454cdd59185dffb837649e391ebc415c965bee6ff80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499535"
---
# <a name="using-the-com-crm-in-a-cluster-environment"></a>Uso de COM+ CRM en un entorno de clúster

Al desarrollar CRM com+ para trabajar en entornos de clúster, el factor principal que se debe tener en cuenta es si a un CRM específico le importa en qué nodo del clúster está funcionando. Por ejemplo, si el recurso administrado por CRM es el registro o el sistema de archivos de la máquina, los cambios son específicos del nodo en el que se ejecuta la aplicación de servidor CRM en ese momento. En este caso, no sería conveniente realizar la conmutación por error de la aplicación de servidor CRM a otro nodo. En otro caso, donde CRM administra algún recurso común al clúster, resulta útil la conmutación por error de la aplicación de servidor CRM a otro nodo.

La ubicación predeterminada del directorio para los archivos de registro de CRM es el mismo directorio que el archivo de registro DTC. En los clústeres, el archivo de registro DTC se coloca en un disco compartido que se conmutación por error entre los nodos del clúster. Esto significa que el comportamiento predeterminado para las aplicaciones de servidor CRM es conmutar por error entre los nodos del clúster. Por lo tanto, si un CRM específico requiere el comportamiento alternativo de no realizar la con error entre nodos, se debe cambiar la ubicación del archivo de registro de CRM para esa aplicación de servidor CRM concreta.

Además, si se requiere la conmutación por error para la aplicación CRM, debe configurarse como una aplicación genérica en un grupo de clústeres. Su dependencia debe ser DTC.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de compensación Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



