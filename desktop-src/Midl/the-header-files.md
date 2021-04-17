---
title: Archivos de encabezado
description: El archivo de encabezado de interfaz (Name. h) contiene definiciones de tipos y declaraciones de función basadas en la definición de interfaz en el archivo IDL actual, así como todos los tipos de datos y operaciones declarados en los archivos incluidos con la Directiva \ include.
ms.assetid: 81fac1fa-6bd7-4a3e-8aa6-5104d4b25b55
keywords:
- archivos de encabezado MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ae80877b88d8061769b0d6bd56c13469427fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665705"
---
# <a name="the-header-files"></a>Archivos de encabezado

El archivo de encabezado de interfaz (Name. h) contiene definiciones de tipos y declaraciones de función basadas en la definición de interfaz en el archivo IDL actual, así como todos los tipos de datos y operaciones declarados en los archivos incluidos con la \# directiva Include. Los tipos de datos de los archivos importados con la Directiva de importación no se replican en el archivo de encabezado; en su lugar, el archivo de encabezado generado contiene una línea de inclusión en el archivo H generado a partir del archivo importado.

Incluya este archivo en los archivos de origen para el archivo DLL de proxy y para las aplicaciones cliente que utilizan la interfaz.

El nombre predeterminado de un archivo de encabezado generado a partir de un archivo. idl es File. h. El modificador de compilador de MIDL [**/Header**](-header.md) invalida el nombre predeterminado del archivo de encabezado de interfaz.

 

 




