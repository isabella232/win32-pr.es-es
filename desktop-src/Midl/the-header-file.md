---
title: El archivo de encabezado
description: El archivo de encabezado contiene definiciones de todos los tipos de datos y operaciones declaradas en el archivo IDL, así como todos los tipos de datos y operaciones declarados en los archivos incluidos con la directiva \include.
ms.assetid: 51789b42-e01c-4233-97da-5e0a044f596f
keywords:
- MIDL y RPC MIDL, interfaces, archivo de encabezado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd107bbf741f3259ac474d03a3ec1eba5c4ab8217df3ff6afa5ef45e7b4945a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582135"
---
# <a name="the-header-file"></a>El archivo de encabezado

El archivo de encabezado contiene definiciones de todos los tipos de datos y operaciones declaradas en el archivo IDL, así como todos los tipos de datos y las operaciones declaradas en los archivos incluidos con la \# directiva include. Los tipos de datos de los archivos importados con la directiva import no se replican en el archivo de encabezado; en su lugar, el archivo de encabezado generado contiene una línea include al archivo H generado a partir del archivo importado. Todos los módulos de aplicación que llaman a las operaciones definidas, implementan las operaciones definidas o manipulan los tipos definidos deben incluir el archivo de encabezado.

Los modificadores del compilador [**MIDL /header**](-header.md) [**y /out**](-out.md) afectan al archivo de encabezado.

 

 




