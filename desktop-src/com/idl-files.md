---
title: Archivos IDL
description: Archivos IDL
ms.assetid: 94a6752d-fcf3-47ce-ac3f-be1d1c9768e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc9a736bf9b9a77ec1cb655fb5c76e9e1c0d27e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904848"
---
# <a name="idl-files"></a>Archivos IDL

COM utiliza el Lenguaje de definición de interfaz de Microsoft (MIDL) para describir objetos COM. MIDL es una extensión de IDL para entornos de computación distribuida definidos por Open Software Foundation, desarrollado para definir interfaces para llamadas a procedimientos remotos en aplicaciones cliente/servidor tradicionales. MIDL incluye la mayoría de los atributos y las instrucciones del lenguaje de definición de objetos (ODL), el lenguaje que se usó originalmente para generar bibliotecas de tipos para la automatización OLE.

En C++ y Java, un desarrollador que crea un objeto COM crea un archivo IDL que el compilador MIDL procesa para crear una biblioteca de tipos o archivos de encabezado y proxy, o ambos. Una *biblioteca de tipos* es un archivo binario que describe el objeto com o las interfaces com, o ambos. Una biblioteca de tipos es la versión compilada del archivo IDL. Sin embargo, las bibliotecas de tipos solo admiten la semántica de ODL. En concreto, no pueden representar toda la información de un archivo IDL relacionado con atributos IDL como \[ [**el tamaño \_ es**](/windows/desktop/Midl/size-is) \] . Debe crear y usar archivos proxy para los archivos IDL afectados por la pérdida de información en la biblioteca de tipos.

En Visual Basic, un desarrollador que crea un objeto COM no crea un archivo IDL. En su lugar, Visual Basic recopila información mediante las propiedades de clase y proyecto y crea directamente la biblioteca de tipos.

 

 