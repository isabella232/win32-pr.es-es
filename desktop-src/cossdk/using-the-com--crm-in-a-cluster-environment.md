---
description: Usar el CRM de COM+ en un entorno de clústeres
ms.assetid: 753461c5-880c-4df0-b552-b962dc06524f
title: Usar el CRM de COM+ en un entorno de clústeres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a05ff281748c35128349ef5d0d0f43d7beae86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360047"
---
# <a name="using-the-com-crm-in-a-cluster-environment"></a>Usar el CRM de COM+ en un entorno de clústeres

Al desarrollar CRMs de COM+ para trabajar en entornos de clústeres, el factor principal a tener en cuenta es si un CRM específico es el nodo del clúster en el que está trabajando. Por ejemplo, si el recurso administrado por CRM es el sistema de archivos del equipo o el registro, los cambios son específicos del nodo en el que se ejecuta la aplicación de servidor CRM. En este caso, no sería conveniente realizar la conmutación por error de la aplicación de servidor CRM a otro nodo. En un caso diferente, en el que el CRM administra algún recurso común al clúster, es útil la conmutación por error de la aplicación de servidor CRM a otro nodo.

La ubicación predeterminada del directorio para los archivos de registro de CRM es el mismo directorio que el archivo de registro de DTC. En los clústeres, el archivo de registro de DTC se coloca en un disco compartido que se conmuta por error entre los nodos del clúster. Esto significa que el comportamiento predeterminado de las aplicaciones de servidor CRM es la conmutación por error entre los nodos del clúster. Por lo tanto, si un CRM específico requiere el comportamiento alternativo de no realizar una conmutación por error entre los nodos, se debe cambiar la ubicación del archivo de registro de CRM para esa aplicación de servidor CRM concreta.

Además, si se requiere la conmutación por error para la aplicación CRM, debe configurarse como una aplicación genérica en un grupo de clústeres. Su dependencia debe ser DTC.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de Administrador de recursos de compensación de COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



