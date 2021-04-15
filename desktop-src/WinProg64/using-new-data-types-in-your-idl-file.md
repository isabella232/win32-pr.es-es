---
title: Usar nuevos tipos de datos en el archivo IDL
description: El archivo de encabezado Basetsd. h define los nuevos tipos de datos necesarios para escribir aplicaciones que se ejecutan en Windows de 32 y 64 bits.
ms.assetid: 99a3904b-9120-4d1d-bd8c-1eb299bd6b27
keywords:
- Archivo de encabezado Basetsd. h 64 programación de Windows de bits
- tipos de datos en el archivo IDL 64 programación de Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff1add2d70c99069911ac76ad168b7d31c3365f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714403"
---
# <a name="using-new-data-types-in-your-idl-file"></a>Usar nuevos tipos de datos en el archivo IDL

El archivo de encabezado Basetsd. h define los nuevos tipos de datos necesarios para escribir aplicaciones que se ejecutan en Windows de 32 y 64 bits. Para usar estos tipos de datos en las interfaces, importe Basetsd. h en el archivo IDL. No \# incluya el archivo o terminará con varias definiciones en tiempo de compilación.

Como alternativa, puede incluir o importar el archivo Basetsd. idl en el archivo IDL.

Para obtener más información sobre cómo agregar archivos de encabezado del sistema al archivo IDL, vea [importar archivos y bibliotecas de tipos](/windows/desktop/Midl/importing-files-and-type-libraries) e [importar archivos de encabezado del sistema](/windows/desktop/Midl/importing-system-header-files).

 

 