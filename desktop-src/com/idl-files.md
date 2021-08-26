---
title: Archivos IDL
description: Archivos IDL
ms.assetid: 94a6752d-fcf3-47ce-ac3f-be1d1c9768e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e2329d14ea844658bf9ad08927ddcef5067debed7a1c8a424c06d3c7adb8d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992905"
---
# <a name="idl-files"></a>Archivos IDL

COM usa el Lenguaje de definición de interfaz de Microsoft (MIDL) para describir objetos COM. MIDL es una extensión del IDL para entornos informáticos distribuidos definidos por Open Software Foundation, que se desarrolló para definir interfaces para llamadas a procedimientos remotos en aplicaciones cliente/servidor tradicionales. MIDL incluye la mayoría de los atributos e instrucciones del Lenguaje de definición de objetos (ODL), el lenguaje que se usó originalmente para generar bibliotecas de tipos para OLE Automation.

En C++ y Java, un desarrollador que crea un objeto COM crea un archivo IDL que el compilador MIDL procesa para crear una biblioteca de tipos o archivos de encabezado y proxy, o ambos. Una *biblioteca de* tipos es un archivo binario que describe el objeto COM o las interfaces COM, o ambos. Una biblioteca de tipos es la versión compilada del archivo IDL. Sin embargo, las bibliotecas de tipos solo admiten semántica de ODL. En concreto, no pueden representar toda la información de un archivo IDL relacionado con atributos IDL como \[ [**el tamaño \_ es**](/windows/desktop/Midl/size-is) \] . Debe crear y usar archivos proxy para los archivos IDL afectados por la pérdida de información en la biblioteca de tipos.

En Visual Basic, un desarrollador que crea un objeto COM no crea un archivo IDL. En su lugar, Visual Basic recopila información mediante propiedades de clase y proyecto y crea directamente la biblioteca de tipos.

 

 