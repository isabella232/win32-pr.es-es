---
title: CPROVCF. Cpp
description: En el componente de proveedor de ejemplo, un ejemplo de código del código de generador de clases de objeto de proveedor de ADs está en cprovcf.cpp.
ms.assetid: 53a4da74-3f36-4e6d-ae93-8d595680bcf3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3b77ea7fe1b1d6fe946b9a8b509be33c11f2a075ee658ee305f0f7ba2d2c6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023673"
---
# <a name="cprovcfcpp"></a>CPROVCF. Cpp

En el componente de proveedor de ejemplo, un ejemplo de código del código de generador de clases de objeto de proveedor de ADs está en cprovcf.cpp. El componente de proveedor nunca crea directamente una instancia de este objeto en ningún momento que no sea cuando el objeto se crea automáticamente durante las operaciones de enlace en [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) o la función interna del método Visual Basic **GetObject**. El método admitido se muestra en la tabla siguiente.



| Método                                  | Descripción                                                           |
|-----------------------------------------|-----------------------------------------------------------------------|
| **CSampleDSProviderCF::CreateInstance** | Crea una instancia del generador de clases para el objeto de proveedor ads. |



 

 

 




