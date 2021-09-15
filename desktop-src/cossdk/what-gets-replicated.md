---
description: Qué se replica
ms.assetid: d1f0bc92-37bc-4de2-876a-e6b8b09da58d
title: Qué se replica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2739cb0ff615ddc38f30a7aa9b0a572be5e28a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465679"
---
# <a name="what-gets-replicated"></a>Qué se replica

## <a name="applications"></a>Aplicaciones

Todas las aplicaciones instaladas en el equipo de origen se replican, excepto lo siguiente:

<dl> <dt>

<span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Dependencias y elementos de aplicación que no son COM+
</dt> <dd>

El administrador es responsable de replicar todo lo que depende de una aplicación COM+, pero que no forma parte correctamente de la propia aplicación, como archivos de datos y archivos DLL. COMREPL no replicará nada fuera de los elementos de la aplicación COM+.

</dd> <dt>

<span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>Aplicaciones preinstaladas de COM+
</dt> <dd>

Las aplicaciones que com+ usa internamente y se instalan a través del programa de instalación de COM+, no se replican. que incluyen la siguiente información:

-   Aplicación del sistema
-   Utilidades com+
-   Agente de escucha de cola de mensajes no enviados de COM+ QC

</dd> <dt>

<span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Aplicaciones creadas por IIS
</dt> <dd>

Estas aplicaciones no se replican e incluyen lo siguiente:

-   Aplicaciones en proceso de IIS
-   Utilidades de IIS
-   Todas las aplicaciones creadas para raíces virtuales aisladas o agrupadas

</dd> </dl>

## <a name="computer-list"></a>Lista de equipos

Los equipos remotos denominados en la **carpeta Equipos** de la herramienta de administración servicios de componentes no se replicarán desde el equipo de origen al equipo de destino.

## <a name="properties"></a>Propiedades

Se replican las siguientes propiedades de la colección **LocalComputer:**

-   TransactionTimeout
-   ResourcePoolingEnabled
-   DCOMEnabled
-   DefaultAuthenticationLevel
-   DefaultImpersonationLevel
-   SecurityTrackingEnabled
-   CISEnabled
-   SecureReferencesEnabled
-   InternetPortsListed
-   DeafultToInternetPorts
-   Puertos
-   RpcProxyEnabled

Las siguientes **propiedades de la colección LocalComputer** no se replican:

-   Descripción
-   ApplicationProxyRSN
-   IsRouter

Para obtener descripciones de las propiedades de la colección **LocalComputer,** vea [**LocalComputer**](localcomputer.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de archivos](file-management.md)
</dt> <dt>

[Registro e informes de errores](logging-and-error-reporting.md)
</dt> <dt>

[Fases de replicación](replication-phases.md)
</dt> <dt>

[Uso de COMREPL](using-comrepl.md)
</dt> </dl>

 

 



