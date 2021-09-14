---
title: El archivo de encabezado
description: El archivo de encabezado contiene definiciones de todos los tipos de datos y operaciones declarados en el archivo IDL, así como todos los tipos de datos y operaciones declarados en los archivos incluidos con la directiva \include.
ms.assetid: 51789b42-e01c-4233-97da-5e0a044f596f
keywords:
- MIDL y RPC MIDL, interfaces, archivo de encabezado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61331d8bb72d322987c13d02b04632c95424e755
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159358"
---
# <a name="the-header-file"></a>El archivo de encabezado

El archivo de encabezado contiene definiciones de todos los tipos de datos y operaciones declarados en el archivo IDL, así como de todos los tipos de datos y operaciones declarados en los archivos incluidos con la \# directiva include. Los tipos de datos de los archivos importados con la directiva import no se replican en el archivo de encabezado; en su lugar, el archivo de encabezado generado contiene una línea de include al archivo H generado a partir del archivo importado. Todos los módulos de aplicación que llaman a las operaciones definidas, implementan las operaciones definidas o manipulan los tipos definidos deben incluir el archivo de encabezado.

Los modificadores del compilador [**MIDL /header**](-header.md) [**y /out**](-out.md) afectan al archivo de encabezado.

 

 




