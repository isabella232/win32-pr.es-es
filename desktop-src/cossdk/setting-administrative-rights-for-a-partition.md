---
description: Establecer derechos administrativos para una partición
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: Establecer derechos administrativos para una partición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33431c5beff76e015d28b6a7e886823620126f2ed9b84db68af9a8f3b8ac1d28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915828"
---
# <a name="setting-administrative-rights-for-a-partition"></a>Establecer derechos administrativos para una partición

Los usuarios asignados al rol administrador de la aplicación del sistema COM+ pueden crear, modificar y eliminar particiones COM+. Dentro de la herramienta administrativa Servicios de componentes, los roles administrativos se pueden asignar a los usuarios expandiendo la **carpeta Roles** de la aplicación del sistema COM+.

A partir Windows Server 2003, la funcionalidad de autenticación de la aplicación del sistema COM+ incluye el valor EOAC \_ DISABLE \_ AAA. Este valor, que deshabilita las activaciones de activación como activador (AAA), se usa en la llamada [**a CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) al iniciar la aplicación del sistema. Establecer la funcionalidad de autenticación en EOAC DISABLE AAA permite que una aplicación que se ejecuta con una cuenta con privilegios \_ (como LocalSystem) ayude a evitar que su identidad se utilice para iniciar componentes que no son de \_ confianza.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recopilación de métricas de partición](collecting-partition-metrics.md)
</dt> <dt>

[Configuración de la caché de particiones](configuring-the-partition-cache.md)
</dt> <dt>

[Agrupación de aplicaciones en particiones](grouping-applications-into-partitions.md)
</dt> <dt>

[Administración de particiones locales](managing-local-partitions.md)
</dt> <dt>

[Administración de particiones dentro de Active Directory](managing-partitions-within-active-directory.md)
</dt> </dl>

 

 
