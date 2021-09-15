---
description: Aunque no se puede tener acceso a un contexto de&\# 160;recognizer&160;en dos subprocesos simultáneamente mediante la plataforma tablet PC, se puede llamar a la función AdviseInkChange en cualquier momento en \# cualquier subproceso.
ms.assetid: 2cd19819-08d0-418d-830b-2288a66ca0d0
title: Consideraciones sobre el subprocesamiento del reconocedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4297cc28e084bbb7c1c09593deb5babc2319ab43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467157"
---
# <a name="recognizer-threading-considerations"></a>Consideraciones sobre el subprocesamiento del reconocedor

Aunque la [plataforma](hrecocontext-handle.md) de Tablet PC no puede acceder simultáneamente a un contexto de reconocedor en dos subprocesos, se puede llamar a la función [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange) en cualquier momento en cualquier subproceso. Dado que la plataforma tablet PC no garantiza que solo haya un contexto de reconocedor a la vez, dos contextos de reconocedor independientes en subprocesos independientes pueden intentar acceder simultáneamente al [reconocedor.](hrecognizer-handle.md) Por lo tanto, las variables globales del motor de reconocimiento deben ser seguras para subprocesos.

Las listas de palabras son una implementación opcional que se usa para aumentar la precisión. Si el reconocedor implementa listas de palabras, debe ser segura para subprocesos. Para obtener más información sobre el uso de listas de palabras, vea [Using Application Dictionaries](using-application-dictionaries.md).

Para obtener más información sobre otras consideraciones de subprocesamiento, vea [Consideraciones sobre subprocesos de Tablet PC](tablet-pc-threading-considerations.md).

 

 



