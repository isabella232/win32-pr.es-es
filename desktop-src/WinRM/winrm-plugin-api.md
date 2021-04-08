---
title: API del complemento WinRM
description: La interfaz de programación de aplicaciones (API) de complementos de WinRM proporciona funcionalidad que permite a los usuarios escribir complementos mediante la implementación de ciertas API para los URI de recursos y las operaciones compatibles.
ms.assetid: d3e103c1-221b-441b-8bcb-883e3f2a4c1a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccc8920f7df788b4df355b0cbc23478e97111d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994385"
---
# <a name="winrm-plug-in-api"></a>API del complemento WinRM

Administración remota de Windows complementos son bibliotecas nativas de vínculos dinámicos (dll) que se conectan y amplían la funcionalidad de WinRM. La interfaz de programación de aplicaciones (API) de complementos de WinRM proporciona funcionalidad que permite a los usuarios escribir complementos mediante la implementación de ciertas API para los [*URI de recursos*](windows-remote-management-glossary.md) y las operaciones compatibles. Una vez configurados los complementos para el servicio WinRM o Internet Information Services (IIS), se cargan en el host de WinRM o en el host de IIS, respectivamente. Las solicitudes remotas se enrutan a estos puntos de entrada del complemento para llevar a cabo las operaciones.

La sección de referencia de la API del complemento WinRM contiene información detallada acerca de los siguientes elementos de la API:

-   [Puntos de entrada del complemento de autorización](authorization-plug-in-entry-points.md)
-   [Métodos de complemento de autorización](authorization-plug-in-methods.md)
-   [Puntos de entrada del complemento de operaciones](operations-plug-in-entry-points.md)
-   [Métodos del complemento de operaciones](operations-plug-in-methods.md)
-   [Estructuras](winrm-plug-in-api-structures.md)

 

 




