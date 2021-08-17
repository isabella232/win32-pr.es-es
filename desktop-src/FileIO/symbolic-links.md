---
description: Un vínculo simbólico es un objeto del sistema de archivos que apunta a otro objeto del sistema de archivos. El objeto al que se apunta se denomina destino.
ms.assetid: d6bf5df7-bc12-4dec-b116-95d9109f5eb4
title: Vínculos simbólicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 126897dc230b36f504ef17653daea32b1076d10870a3a22015462f3abec05448
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951034"
---
# <a name="symbolic-links"></a>Vínculos simbólicos

Un vínculo simbólico es un objeto del sistema de archivos que apunta a otro objeto del sistema de archivos. El objeto al que se apunta se denomina destino.

Los vínculos simbólicos son transparentes para los usuarios. Los vínculos aparecen como archivos o directorios normales y el usuario o la aplicación pueden actuar exactamente de la misma manera.

Los vínculos simbólicos están diseñados para facilitar la migración y la compatibilidad de aplicaciones con sistemas operativos UNIX. Microsoft ha implementado sus vínculos simbólicos para funcionar igual que UNIX vínculos.

Para obtener más información, vea los temas siguientes:

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                             | Descripción                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Efectos de vínculo simbólico en funciones de sistemas de archivos](symbolic-link-effects-on-file-systems-functions.md)<br/> | Cómo afectan los vínculos simbólicos a las funciones de archivo estándar que usan nombres de ruta de acceso para especificar uno o varios archivos.<br/>                                        |
| [Consideraciones sobre la programación](symbolic-link-programming-considerations.md)<br/>                             | Consideraciones de programación para trabajar con vínculos simbólicos.<br/>                                                                                |
| [Crear vínculos simbólicos](creating-symbolic-links.md)<br/>                                                 | Cree vínculos simbólicos que usen una ruta de acceso absoluta o relativa mediante la [**función CreateSymbolicLink.**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka)<br/> |



 

## <a name="supported-operating-systems"></a>Sistemas operativos compatibles

Los vínculos simbólicos están disponibles en NTFS a partir de Windows Vista.

 

 




