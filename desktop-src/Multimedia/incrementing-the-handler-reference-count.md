---
title: Incrementar el recuento de referencias de controlador
description: Incrementar el recuento de referencias de controlador
ms.assetid: 9e71ce1f-5805-4240-9dcc-7e71fbabfe7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a990f2570fca0057156a39a955930cca2d71858
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371689"
---
# <a name="incrementing-the-handler-reference-count"></a>Incrementar el recuento de referencias de controlador

El **método AddRef** incrementa el recuento de referencias del controlador de archivos o del controlador de secuencias.


```C++
STDMETHODIMP_(ULONG) CAVIFileCF::AddRef() 
{ 
    return ++m_refs; 
} 

```



 

 




