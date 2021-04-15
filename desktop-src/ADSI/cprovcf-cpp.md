---
title: CPROVCF. CPP
description: En el componente proveedor de ejemplo, un ejemplo de código del código del generador de clases de objetos del proveedor de ADs está en cprovcf. cpp.
ms.assetid: 53a4da74-3f36-4e6d-ae93-8d595680bcf3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d086cd79086f40bab6d898b844ed52fc0161bc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486570"
---
# <a name="cprovcfcpp"></a>CPROVCF. CPP

En el componente proveedor de ejemplo, un ejemplo de código del código del generador de clases de objetos del proveedor de ADs está en cprovcf. cpp. El componente de proveedor nunca crea directamente una instancia de este objeto en ningún momento distinto de cuando se crea automáticamente el objeto durante las operaciones de enlace en [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) o la función interna en el método Visual Basic **GetObject**. El método admitido se muestra en la tabla siguiente.



| Método                                  | Descripción                                                           |
|-----------------------------------------|-----------------------------------------------------------------------|
| **CSampleDSProviderCF:: CreateInstance** | Crea una instancia del generador de clases para el objeto de proveedor de ADS. |



 

 

 




