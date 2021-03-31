---
description: Al establecer esta Directiva del sistema por usuario, se especifica el orden en el que el instalador busca tres tipos de orígenes.
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: SearchOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f486ee58eebd1a1bd1174f18e413785e5e3129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913665"
---
# <a name="searchorder"></a>SearchOrder

Al establecer esta [Directiva del sistema](system-policy.md) por usuario, se especifica el orden en el que el instalador busca tres tipos de orígenes. Los tipos de orígenes son:

"n": red

"m": medio (CD-ROM o DVD)

"u": localizador uniforme de recursos (URL)

Por ejemplo, para buscar primero los orígenes de red, los orígenes de medios segundo y los orígenes de direcciones URL, establezca esta directiva en un valor de "NMU". Para omitir la búsqueda de un tipo de origen determinado, deje la letra correspondiente del valor.

Si no se establece SearchOrder, el orden de búsqueda predeterminado es red, medios y dirección URL.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de usuario actual \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**Registro \_ SZ**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> </dl>

 

 



