---
description: Lo que se replica
ms.assetid: d1f0bc92-37bc-4de2-876a-e6b8b09da58d
title: Lo que se replica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2739cb0ff615ddc38f30a7aa9b0a572be5e28a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705315"
---
# <a name="what-gets-replicated"></a>Lo que se replica

## <a name="applications"></a>APLICACIONES

Todas las aplicaciones instaladas en el equipo de origen se replican, excepto las siguientes:

<dl> <dt>

<span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Elementos y dependencias de aplicaciones que no son COM +
</dt> <dd>

El administrador es responsable de replicar todo aquello del que depende una aplicación COM+ pero que no forma parte correctamente de la propia aplicación, como archivos de datos y archivos dll. COMREPL no replicará nada fuera de los elementos de la aplicación COM+.

</dd> <dt>

<span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>Aplicaciones preinstaladas de COM+
</dt> <dd>

Las aplicaciones que usa COM+ y que se instalan a través del programa de instalación de COM+ no se replican. Entre ellas, figuran:

-   Aplicación del sistema
-   Utilidades COM+
-   Agente de escucha de cola de mensajes con problemas de entrega COM+

</dd> <dt>

<span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Aplicaciones creadas por IIS
</dt> <dd>

Estas aplicaciones no se replican e incluyen lo siguiente:

-   Aplicaciones en proceso de IIS
-   Utilidades IIS
-   Todas las aplicaciones creadas para las raíces virtuales agrupadas o aisladas

</dd> </dl>

## <a name="computer-list"></a>Lista de equipos

Los equipos remotos nombrados en la carpeta **equipos** de la herramienta de administración de servicios de componentes no se replicarán desde el equipo de origen al de destino.

## <a name="properties"></a>Propiedades

Se replican las siguientes propiedades de la colección **LocalComputer** :

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

Las siguientes propiedades de la colección **LocalComputer** no se replican:

-   Descripción
-   ApplicationProxyRSN
-   IsRouter

Para obtener descripciones de las propiedades de la colección **LocalComputer** , vea [**LocalComputer**](localcomputer.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de archivos](file-management.md)
</dt> <dt>

[Registro e informes de errores](logging-and-error-reporting.md)
</dt> <dt>

[Fases de replicación](replication-phases.md)
</dt> <dt>

[Usar COMREPL](using-comrepl.md)
</dt> </dl>

 

 



