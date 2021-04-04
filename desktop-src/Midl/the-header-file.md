---
title: El archivo de encabezado
description: El archivo de encabezado contiene definiciones de todos los tipos de datos y operaciones declarados en el archivo IDL, así como todos los tipos de datos y las operaciones declaradas en los archivos incluidos con la Directiva \ include.
ms.assetid: 51789b42-e01c-4233-97da-5e0a044f596f
keywords:
- MIDL y RPC MIDL, interfaces, archivo de encabezado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61331d8bb72d322987c13d02b04632c95424e755
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076057"
---
# <a name="the-header-file"></a>El archivo de encabezado

El archivo de encabezado contiene definiciones de todos los tipos de datos y operaciones declarados en el archivo IDL, así como todos los tipos de datos y las operaciones declaradas en los archivos incluidos con la \# directiva Include. Los tipos de datos de los archivos importados con la Directiva de importación no se replican en el archivo de encabezado; en su lugar, el archivo de encabezado generado contiene una línea de inclusión en el archivo H generado a partir del archivo importado. El archivo de encabezado debe estar incluido en todos los módulos de aplicación que llaman a las operaciones definidas, implementan las operaciones definidas o manipulan los tipos definidos.

El compilador MIDL cambia [**/Header**](-header.md) y [**/out**](-out.md) afectan al archivo de encabezado.

 

 




