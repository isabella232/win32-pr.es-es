---
description: Al establecer esta directiva de sistema por usuario se especifica el orden en el que el instalador busca tres tipos de orígenes.
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: SearchOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfaab6ff8d4b40b966b5ab1785ddd5fd473316732833fc32be7102acaa7c4877
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041045"
---
# <a name="searchorder"></a>SearchOrder

Al establecer esta directiva de [sistema por](system-policy.md) usuario se especifica el orden en el que el instalador busca tres tipos de orígenes. Los tipos de orígenes son:

"n": red

"m": medios (CD-ROM o DVD)

"u": localizador uniforme de recursos (URL)

Por ejemplo, para buscar primero los orígenes de red, los orígenes de medios en segundo lugar y los orígenes de dirección URL, establezca esta directiva en un valor de "nmu". Para omitir la búsqueda de un tipo de origen determinado, deje fuera la letra correspondiente del valor.

Si SearchOrder no está establecido, el orden de búsqueda predeterminado es red, medios y, a continuación, dirección URL.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ DIRECTIVAS \_ DE** \\ **SOFTWARE DE** \\ **USUARIO** \\ **ACTUAL Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ SZ**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> </dl>

 

 



