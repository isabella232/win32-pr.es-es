---
description: Aunque no se puede obtener acceso a un&\# 160; contexto del reconocedor&\# 160; en dos subprocesos simultáneamente mediante la plataforma de Tablet PC, se puede llamar a la función AdviseInkChange en cualquier momento en cualquier subproceso.
ms.assetid: 2cd19819-08d0-418d-830b-2288a66ca0d0
title: Consideraciones sobre los subprocesos del reconocedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4297cc28e084bbb7c1c09593deb5babc2319ab43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706775"
---
# <a name="recognizer-threading-considerations"></a>Consideraciones sobre los subprocesos del reconocedor

Aunque no se puede tener acceso a un [contexto de reconocedor](hrecocontext-handle.md) en dos subprocesos simultáneamente mediante la plataforma de Tablet PC, se puede llamar a la función [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange) en cualquier momento en cualquier subproceso. Dado que la plataforma de Tablet PC no garantiza que solo haya un contexto de reconocedor a la vez, dos contextos de reconocedor independientes en subprocesos independientes pueden intentar simultáneamente el acceso al [reconocedor](hrecognizer-handle.md). Por lo tanto, las variables globales del motor de reconocimiento deben ser seguras para subprocesos.

Las listas de palabras son una implementación opcional que se usa para aumentar la precisión. Si el reconocedor implementa listas de palabras, debe ser segura para la ejecución de subprocesos. Para obtener más información sobre el uso de las listas de palabras, vea [uso de diccionarios de aplicación](using-application-dictionaries.md).

Para obtener más información sobre otras consideraciones sobre los subprocesos, consulte [consideraciones de subprocesos de Tablet PC](tablet-pc-threading-considerations.md).

 

 



