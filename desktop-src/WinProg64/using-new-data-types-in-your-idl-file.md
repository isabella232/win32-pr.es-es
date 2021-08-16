---
title: Usar nuevos tipos de datos en el archivo IDL
description: El archivo de encabezado Basetsd.h define los nuevos tipos de datos necesarios para escribir aplicaciones que se ejecutan en aplicaciones de 32 y 64 Windows.
ms.assetid: 99a3904b-9120-4d1d-bd8c-1eb299bd6b27
keywords:
- Archivo de encabezado Basetsd.h de 64 bits Windows programación
- tipos de datos en el archivo IDL de 64 bits Windows programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccb29ee654dc2ecc1459a4a3e8ba549e8f78a8af26a305725dbce90f469881b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993925"
---
# <a name="using-new-data-types-in-your-idl-file"></a>Usar nuevos tipos de datos en el archivo IDL

El archivo de encabezado Basetsd.h define los nuevos tipos de datos necesarios para escribir aplicaciones que se ejecutan en aplicaciones de 32 y 64 Windows. Para usar estos tipos de datos en las interfaces, importe Basetsd.h en el archivo IDL. No incluya el archivo o terminará con varias \# definiciones en tiempo de compilación.

Como alternativa, puede incluir o importar el archivo Basetsd.idl en el archivo IDL.

Para obtener más información sobre cómo agregar archivos de encabezado del sistema al archivo IDL, vea Importar archivos y [bibliotecas](/windows/desktop/Midl/importing-files-and-type-libraries) de tipos e [Importar archivos de encabezado del sistema](/windows/desktop/Midl/importing-system-header-files).

 

 