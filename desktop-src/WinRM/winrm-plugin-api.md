---
title: API del complemento WinRM
description: La interfaz de programación de aplicaciones (API) del complemento WinRM proporciona funcionalidad que permite a un usuario escribir complementos mediante la implementación de determinadas API para operaciones y URI de recursos admitidos.
ms.assetid: d3e103c1-221b-441b-8bcb-883e3f2a4c1a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7359ed212e50b71343ce9a96832060e9ec8121cdf3e11f3f353698e1a4fa9dce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742783"
---
# <a name="winrm-plug-in-api"></a>API del complemento WinRM

Windows Los complementos de administración remota son bibliotecas nativas de vínculos dinámicos (DLL) que se unen y amplían la funcionalidad de WinRM. La interfaz de programación de aplicaciones (API) del complemento WinRM proporciona funcionalidad que permite [](windows-remote-management-glossary.md) a un usuario escribir complementos mediante la implementación de determinadas API para operaciones y URI de recursos admitidos. Una vez configurados los complementos para el servicio WinRM o Internet Information Services (IIS), se cargan en el host de WinRM o en el host de IIS, respectivamente. Las solicitudes remotas se enrutan a estos puntos de entrada del complemento para llevar a cabo operaciones.

La sección de referencia de la API del complemento WinRM contiene información detallada sobre los siguientes elementos de API:

-   [Puntos de entrada del complemento de autorización](authorization-plug-in-entry-points.md)
-   [Métodos de complemento de autorización](authorization-plug-in-methods.md)
-   [Puntos de entrada del complemento de operaciones](operations-plug-in-entry-points.md)
-   [Métodos de complemento de operaciones](operations-plug-in-methods.md)
-   [Estructuras](winrm-plug-in-api-structures.md)

 

 




