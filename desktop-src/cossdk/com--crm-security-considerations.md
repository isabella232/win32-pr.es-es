---
description: Consideraciones de seguridad de CRM de COM+
ms.assetid: e212c847-b43b-43be-b089-82336551b89a
title: Consideraciones de seguridad de CRM de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1052f9e8cf4f23dd80e2b4706b7e13c0f39a2aedd9b9a985da2d41101118467d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638735"
---
# <a name="com-crm-security-considerations"></a>Consideraciones de seguridad de CRM de COM+

Un archivo de registro de CRM podría contener información confidencial que debe protegerse. Por esta razón, si la aplicación de servidor se ejecuta con cualquier identidad que no sea Usuario interactivo cuando se crea por primera vez el archivo de registro de CRM, el archivo de registro crm solo está protegido por la seguridad para ese usuario. Esta característica solo está disponible en el sistema de archivos NTFS. Si posteriormente se cambia la identidad de la aplicación de servidor, la información de seguridad del archivo de registro de CRM no cambia automáticamente. Se puede cambiar manualmente mediante el uso de herramientas de Windows administración existentes. La alternativa es simplemente eliminar el archivo de registro de CRM cuando se encuentra en un estado limpio (lo que se espera después de un apagado controlado de la aplicación de servidor).

En un funcionamiento normal, COM+ crea el componente de compensador CRM y llama a la [**interfaz ICrmCompensator.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) Sin embargo, un usuario con privilegios para crear crm compensator puede llamar a la interfaz **ICrmCompensator** en momentos inadecuados, lo que posiblemente cause problemas de seguridad del sistema. Para ayudar a protegerse frente a estos problemas de seguridad, el administrador del sistema puede usar la seguridad basada en roles para restringir el componente Compensator de CRM solo a las identidades de las aplicaciones de servidor en las que se ejecuta. Si el componente se ejecuta en una aplicación de biblioteca, esto incluiría todas las identidades de las aplicaciones de servidor.

> [!Note]  
> A partir de Windows Server 2003, para ayudar a evitar la activación desde fuera de la aplicación de servidor, es posible garantizar aún más un sistema más seguro marcando el componente crm Compensator como privado.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de compensación Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



