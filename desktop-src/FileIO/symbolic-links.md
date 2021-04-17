---
description: Un vínculo simbólico es un objeto del sistema de archivos que apunta a otro objeto del sistema de archivos. El objeto al que apunta se denomina destino.
ms.assetid: d6bf5df7-bc12-4dec-b116-95d9109f5eb4
title: Vínculos simbólicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f051beb7de0280ba42df782264cef385f8d01a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688285"
---
# <a name="symbolic-links"></a>Vínculos simbólicos

Un vínculo simbólico es un objeto del sistema de archivos que apunta a otro objeto del sistema de archivos. El objeto al que apunta se denomina destino.

Los vínculos simbólicos son transparentes para los usuarios; los vínculos aparecen como archivos o directorios normales y el usuario o la aplicación pueden actuar de la misma manera de igual forma.

Los vínculos simbólicos están diseñados para facilitar la migración y la compatibilidad de aplicaciones con sistemas operativos UNIX. Microsoft ha implementado sus vínculos simbólicos para que funcionen igual que los vínculos de UNIX.

Para obtener más información, vea los siguientes temas.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                             | Descripción                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Efectos simbólicos de los vínculos en las funciones del sistema de archivos](symbolic-link-effects-on-file-systems-functions.md)<br/> | Cómo afectan los vínculos simbólicos a las funciones de archivo estándar que usan nombres de ruta de acceso para especificar uno o varios archivos.<br/>                                        |
| [Consideraciones sobre la programación](symbolic-link-programming-considerations.md)<br/>                             | Consideraciones de programación para trabajar con vínculos simbólicos.<br/>                                                                                |
| [Crear vínculos simbólicos](creating-symbolic-links.md)<br/>                                                 | Cree vínculos simbólicos que usen una ruta de acceso absoluta o relativa mediante la función [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) .<br/> |



 

## <a name="supported-operating-systems"></a>Sistemas operativos compatibles

Los vínculos simbólicos están disponibles en NTFS a partir de Windows Vista.

 

 




