---
description: Establecer derechos administrativos para una partición
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: Establecer derechos administrativos para una partición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c421b37dd50fa21ee9cf146749ec00b0c91d98c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807358"
---
# <a name="setting-administrative-rights-for-a-partition"></a>Establecer derechos administrativos para una partición

Los usuarios a los que se ha asignado el rol de administrador de la aplicación del sistema COM+ pueden crear, modificar y eliminar particiones de COM+. En la herramienta administrativa Servicios de componentes, los roles administrativos se pueden asignar a los usuarios expandiendo la carpeta **roles** de la aplicación del sistema com+.

A partir de Windows Server 2003, la capacidad de autenticación para la aplicación del sistema COM+ incluye el valor EOAC \_ Disable \_ AAA. Este valor, que deshabilita las activaciones de activación como activador (AAA), se utiliza en la llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) al iniciar la aplicación del sistema. Establecer la capacidad de autenticación en EOAC \_ deshabilitar \_ AAA permite que una aplicación que se ejecuta en una cuenta con privilegios (como LocalSystem) ayude a evitar que se use su identidad para iniciar componentes que no son de confianza.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recopilación de métricas de partición](collecting-partition-metrics.md)
</dt> <dt>

[Configuración de la memoria caché de partición](configuring-the-partition-cache.md)
</dt> <dt>

[Agrupar aplicaciones en particiones](grouping-applications-into-partitions.md)
</dt> <dt>

[Administrar particiones locales](managing-local-partitions.md)
</dt> <dt>

[Administrar particiones en Active Directory](managing-partitions-within-active-directory.md)
</dt> </dl>

 

 
